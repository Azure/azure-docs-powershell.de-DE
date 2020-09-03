---
title: Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell
description: Hier erfahren Sie, wie Sie mit Azure PowerShell einen Dienstprinzipal für Ihre App oder Ihren Dienst erstellen.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 76456b3d0e2a0c000488c0d7518845e5f56f2c75
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243326"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Wenn Sie Ihre App oder Ihren Dienst mit Azure PowerShell verwalten möchten, sollten Sie sie bzw. ihn nicht unter Ihren eigenen Anmeldeinformationen, sondern unter einem AAD-Dienstprinzipal (Azure Active Directory) ausführen. In diesem Artikel wird Schritt für Schritt erläutert, wie Sie einen Sicherheitsprinzipal mit Azure PowerShell erstellen.

> [!NOTE]
> Dienstprinzipale können auch über das Azure-Portal erstellt werden. Ausführlichere Informationen finden Sie unter [Erstellen einer Active Directory-Anwendung und eines Dienstprinzipals mit Ressourcenzugriff mithilfe des Portals](/azure/azure-resource-manager/resource-group-create-service-principal-portal).

## <a name="what-is-a-service-principal"></a>Was ist ein Dienstprinzipal?

Ein Azure-Dienstprinzipal ist eine Sicherheitsidentität, die durch von Benutzern erstellte Apps, Dienste und Automatisierungstools verwendet wird, um auf bestimmte Azure-Ressourcen zuzugreifen. Das Konzept lässt sich als Benutzeridentität (Benutzername und Kennwort oder Zertifikat) mit einer bestimmten Rolle und streng kontrollierten Berechtigungen beschreiben. Ein Dienstprinzipal sollte – im Gegensatz zu einer allgemeinen Benutzeridentität – nur für bestimmte Dinge zuständig sein. Wenn Sie ihr nur die Berechtigungen gewähren, die sie zum Ausführen ihrer Verwaltungsaufgaben benötigt, verbessert das die Sicherheit.

## <a name="verify-your-own-permission-level"></a>Überprüfen der eigenen Berechtigungsstufe

Zunächst einmal müssen Sie sowohl in der Azure Active Directory-Instanz als auch im Azure-Abonnement über ausreichende Berechtigungen verfügen. Sie müssen eine App in der Active Directory-Instanz erstellen und dem Dienstprinzipal eine Rolle zuweisen können.

Die einfachste Möglichkeit zum Überprüfen, ob Ihr Konto über die richtigen Berechtigungen verfügt, ist die Vorgehensweise über das Portal. Siehe [Überprüfen der erforderlichen Berechtigung im Portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Erstellen eines Dienstprinzipals für Ihre App

Nachdem Sie sich an Ihrem Azure-Konto angemeldet haben, können Sie den Dienstprinzipal erstellen. Ihre bereitgestellte App muss auf eine der folgenden Arten identifiziert werden:

* Mithilfe des eindeutigen Namens Ihrer bereitgestellten App („MyDemoWebApp“ in den folgenden Beispielen). Oder:
* Mithilfe der Anwendungs-ID (GUID, die Ihrer bereitgestellten App, Ihrem bereitgestellten Dienst oder Ihrem bereitgestellten Objekt zugeordnet ist)

### <a name="get-information-about-your-application"></a>Abrufen von Informationen zu Ihrer Anwendung

Mit dem Cmdlet `Get-AzureRmADApplication` können Sie Informationen zu Ihrer Anwendung erhalten.

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>Erstellen eines Dienstprinzipals für Ihre Anwendung

Das Cmdlet `New-AzureRmADServicePrincipal` dient zum Erstellen des Dienstprinzipals.

```azurepowershell-interactive
$servicePrincipal = New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

Sie können nun entweder direkt die Eigenschaft „$servicePrincipal.Secret“ in „Connect-AzureRmAccount“ verwenden (siehe „Anmelden mithilfe des Dienstprinzipals“ weiter unten) oder dieses SecureString-Element zur späteren Verwendung in eine Nur-Text-Zeichenfolge konvertieren:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a>Anmelden mithilfe des Dienstprinzipals

Nun können Sie sich als der neue Dienstprinzipal für die App anmelden. Verwenden Sie dabei den von Ihnen angegebenen Wert für *appId* und den automatisch generierten Wert für *password*. Außerdem benötigen Sie die Mandanten-ID für den Dienstprinzipal. Ihre Mandanten-ID wird angezeigt, wenn Sie sich mit Ihren persönlichen Anmeldeinformationen bei Azure anmelden. Verwenden Sie die folgenden Befehle, um sich mit einem Dienstprinzipal anzumelden:

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Nach einer erfolgreichen Anmeldung wird die folgende Ausgabe angezeigt:

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Glückwunsch! Die Anmeldeinformationen können zum Ausführen Ihrer App verwendet werden. Als Nächstes müssen Sie die Berechtigungen des Dienstprinzipals anpassen.

## <a name="managing-roles"></a>Verwalten von Rollen

> [!NOTE]
> Bei der rollenbasierten Zugriffssteuerung (Role-Based Access Control, RBAC) in Azure handelt es sich um ein Modell zum Definieren und Verwalten von Rollen für Benutzer- und Dienstprinzipale. Rollen sind bestimmte Berechtigungen zugeordnet, die bestimmen, welche Ressourcen ein Prinzipal lesen, aufrufen, schreiben oder verwalten kann. Weitere Informationen zu RBAC und Rollen finden Sie unter [ Integrierte Rollen](/azure/active-directory/role-based-access-built-in-roles).

Für die Verwaltung von Rollenzuweisungen stehen in Azure PowerShell folgende Cmdlets zur Verfügung:

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

Standardmäßig hat ein Dienstprinzipal die Rolle **Mitwirkender**. Je nachdem, in welchem Maß Ihrer App mit Azure Services interagiert, ist das unter Umständen nicht die beste Wahl, da diese Rolle über umfassende Berechtigungen verfügt.
Die Rolle **Leser** ist stärker eingeschränkt und bietet sich für Apps ohne Schreibzugriff an. Über das Azure-Portal können Sie Details zu rollenspezifischen Berechtigungen anzeigen oder benutzerdefinierte Berechtigungen erstellen.

Im folgenden Beispiel fügen wir unserem vorherigen Beispiel die Rolle **Leser** hinzu und löschen die Rolle **Mitwirkender**:

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

So zeigen Sie die derzeit zugewiesenen Rollen an:

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

Weitere Azure PowerShell-Cmdlets für die Rollenverwaltung:

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Ändern der Anmeldeinformationen des Sicherheitsprinzipals

Aus Sicherheitsgründen empfiehlt es sich, regelmäßig die Berechtigungen zu überprüfen und das Kennwort zu aktualisieren. Darüber hinaus sollten Sie auch die Sicherheitsanmeldeinformationen verwalten und ändern, wenn sich Ihre App verändert. Zum Ändern des Dienstprinzipalkennworts können wir beispielsweise ein neues Kennwort erstellen und das alte entfernen.

### <a name="add-a-new-password-for-the-service-principal"></a>Hinzufügen eines neuen Kennworts für den Dienstprinzipal

```azurepowershell-interactive
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Abrufen einer Liste mit Anmeldeinformationen für den Dienstprinzipal

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Entfernen des alten Kennworts für den Dienstprinzipal

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Überprüfen der Liste mit Anmeldeinformationen für den Dienstprinzipal

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a>Abrufen von Informationen zum Dienstprinzipal

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
