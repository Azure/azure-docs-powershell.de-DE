---
title: Verwenden von Azure-Dienstprinzipalen mit Azure PowerShell
description: Hier erfahren Sie, wie Sie mit Azure PowerShell Dienstprinzipale erstellen und verwenden.
ms.devlang: powershell
ms.topic: conceptual
ms.service: azure-powershell
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 1879fea883c796dae26e353adeab908c8acdb967
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012107"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell

Für automatisierte Tools, die Azure-Dienste verwenden, sollten stets eingeschränkte Berechtigungen festgelegt sein. Azure bietet Dienstprinzipale, damit Anwendungen nicht als Benutzer mit uneingeschränkten Berechtigungen angemeldet werden müssen.

Ein Azure-Dienstprinzipal ist eine Identität, die zur Verwendung mit Anwendungen, gehosteten Diensten und automatisierten Tools für den Zugriff auf Azure-Ressourcen erstellt wird. Dieser Zugriff wird durch die dem Dienstprinzipal zugewiesenen Rollen eingeschränkt. Dadurch können Sie steuern, auf welcher Ebene auf welche Ressourcen zugegriffen werden kann. Aus Sicherheitsgründen wird stets empfohlen, Dienstprinzipale mit automatisierten Tools zu verwenden, statt ihnen die Anmeldung mit einer Benutzeridentität zu erlauben.

In diesem Artikel wird Schritt für Schritt erläutert, wie Sie mit Azure PowerShell einen Dienstprinzipal erstellen, Informationen zu ihm abrufen und ihn zurücksetzen.

> [!WARNING]
> Wenn Sie mithilfe des Befehls [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) einen Dienstprinzipal erstellen, enthält die Ausgabe Anmeldeinformationen, die geschützt werden müssen. Verwenden Sie als Alternative ggf. [verwaltete Identitäten](/azure/active-directory/managed-identities-azure-resources/overview), um zu vermeiden, dass die Verwendung von Anmeldeinformationen erforderlich ist.
>
> [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) weist dem Dienstprinzipal standardmäßig auf Abonnementebene die Rolle [Mitwirkender](/azure/role-based-access-control/built-in-roles#contributor) zu. Um das Risiko eines kompromittierten Dienstprinzipals zu verringern, weisen Sie eine spezifischere Rolle zu, und schränken Sie den Bereich auf eine Ressource oder Ressourcengruppe ein. Weitere Informationen finden Sie unter [Schritte zum Hinzufügen einer Rollenzuweisung](/azure/role-based-access-control/role-assignments-steps).

## <a name="create-a-service-principal"></a>Erstellen eines Dienstprinzipals

Erstellen Sie mit dem Cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) einen Dienstprinzipal. Beim Erstellen eines Dienstprinzipals wählen Sie den Typ der von ihm verwendeten Anmeldeauthentifizierung aus.

> [!NOTE]
> Wenn Ihr Konto nicht über die Berechtigung zum Erstellen eines Dienstprinzipals verfügt, gibt `New-AzADServicePrincipal` eine Fehlermeldung mit dem Hinweis „Nicht genügend Berechtigungen zum Abschließen des Vorgangs“ zurück.
> Bitten Sie den Azure Active Directory-Administrator, einen Dienstprinzipal zu erstellen.

Für Dienstprinzipale stehen zwei Authentifizierungstypen zur Verfügung: Kennwortbasierte Authentifizierung und zertifikatbasierte Authentifizierung.

### <a name="password-based-authentication"></a>Kennwortbasierte Authentifizierung

> [!IMPORTANT]
> Die Standardrolle für einen Dienstprinzipal mit kennwortbasierter Authentifizierung ist **Mitwirkender**. Diese Rolle besitzt uneingeschränkte Berechtigungen für Lese- und Schreibvorgänge in einem Azure-Konto. Informationen zum Verwalten von Rollenzuweisungen finden Sie unter [Verwalten von Dienstprinzipalrollen](#manage-service-principal-roles).

Ohne weitere Authentifizierungsparameter wird die kennwortbasierte Authentifizierung mit einem für Sie erstellten zufälligen Kennwort verwendet. Diese Methode wird empfohlen, wenn Sie die kennwortbasierte Authentifizierung verwenden möchten.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Das zurückgegebene Objekt enthält den `Secret`-Member; dabei handelt es sich um ein `SecureString`-Element, in dem das generierte Kennwort enthalten ist. Achten Sie darauf, diesen Wert für die Authentifizierung beim Dienstprinzipal an einem sicheren Ort zu speichern. Der Wert _wird nicht_ in der Konsolenausgabe angezeigt. Wenn Sie das Kennwort verlieren, [setzen Sie die Anmeldeinformationen des Dienstprinzipals zurück](#reset-credentials).

Mit dem folgenden Code können Sie das Geheimnis exportieren:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

Für benutzerdefinierte Kennwörter akzeptiert das `-PasswordCredential`-Argument `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`-Objekte. Diese Objekte müssen gültige Werte für `StartDate` und `EndDate` haben und ein `Password`-Element in Klartext akzeptieren. Halten Sie sich beim Erstellen eines Kennworts unbedingt an die Vorgaben unter [Kennwortrichtlinien und -einschränkungen in Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).
Verwenden Sie kein unsicheres Kennwort, und verwenden Sie ein Kennwort nicht erneut.

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

Das von `New-AzADServicePrincipal` zurückgegebene Objekt enthält die Member `Id` und `DisplayName`, die jeweils für die Anmeldung beim Dienstprinzipal verwendet werden können.

> [!IMPORTANT]
> Das Anmelden bei einem Dienstprinzipal erfordert die ID des Mandanten, unter dem der Dienstprinzipal erstellt wurde. Führen Sie den folgenden Befehl _unmittelbar nach_ der Erstellung des Dienstprinzipals aus, um den aktiven Mandanten abzurufen:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a>Zertifikatbasierte Authentifizierung

> [!IMPORTANT]
> Beim Erstellen eines Dienstprinzipals mit zertifikatbasierter Authentifizierung wird keine Standardrolle zugewiesen. Informationen zum Verwalten von Rollenzuweisungen finden Sie unter [Verwalten von Dienstprinzipalrollen](#manage-service-principal-roles).

Dienstprinzipale mit zertifikatbasierter Authentifizierung werden mit dem Parameter `-CertValue` erstellt. Dieser Parameter nimmt eine Base64-codierte ASCII-Zeichenfolge des öffentlichen Zertifikats entgegen. Diese wird durch eine PEM-Datei oder eine textcodierte CRT- oder CER-Datei dargestellt. Binäre Codierungen des öffentlichen Zertifikats werden nicht unterstützt. Für diese Anweisungen wird davon ausgegangen, dass bereits ein Zertifikat verfügbar ist.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

Sie können auch den Parameter `-KeyCredential` verwenden, der `PSADKeyCredential`-Objekte entgegennimmt. Diese Objekte müssen gültige `StartDate`- und `EndDate`-Werte aufweisen, und der Member `CertValue` muss auf eine Base64-codierte ASCII-Zeichenfolge des öffentlichen Zertifikats festgelegt sein.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

Das von `New-AzADServicePrincipal` zurückgegebene Objekt enthält die Member `Id` und `DisplayName`, die jeweils für die Anmeldung beim Dienstprinzipal verwendet werden können. Clients benötigen für die Anmeldung beim Dienstprinzipal außerdem Zugriff auf den privaten Schlüssel des Zertifikats.

> [!IMPORTANT]
> Das Anmelden bei einem Dienstprinzipal erfordert die ID des Mandanten, unter dem der Dienstprinzipal erstellt wurde. Führen Sie den folgenden Befehl _unmittelbar nach_ der Erstellung des Dienstprinzipals aus, um den aktiven Mandanten abzurufen:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a>Abrufen eines vorhandenen Dienstprinzipals

Eine Liste der Dienstprinzipale für den aktiven Mandanten kann mit [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) abgerufen werden. Dieser Befehl gibt standardmäßig _alle_ Dienstprinzipale in einem Mandanten zurück. Für große Organisationen kann es lange dauern, bis Ergebnisse zurückgegeben werden. Stattdessen wird die Verwendung eines der optionalen serverseitigen Filterungsargumente empfohlen:

- `-DisplayNameBeginsWith` fordert Dienstprinzipale mit einem _Präfix_ an, das dem angegebenen Wert entspricht. Der Anzeigename eines Dienstprinzipals ist der Wert, der während der Erstellung mit `-DisplayName` festgelegt wird.
- `-DisplayName` fordert die _genaue Übereinstimmung_ eines Dienstprinzipalnamens an.

## <a name="manage-service-principal-roles"></a>Verwalten von Dienstprinzipalrollen

Für die Verwaltung von Rollenzuweisungen stehen in Azure PowerShell folgende Cmdlets zur Verfügung:

- [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
- [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
- [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Die Standardrolle für einen Dienstprinzipal mit kennwortbasierter Authentifizierung ist **Mitwirkender**. Diese Rolle besitzt uneingeschränkte Berechtigungen für Lese- und Schreibvorgänge in einem Azure-Konto. Die Rolle **Leser** ist stärker eingeschränkt und bietet schreibgeschützten Zugriff. Weitere Informationen zur rollenbasierten Zugriffssteuerung (Role-Based Access Control, RBAC) finden Sie unter [Rollenbasierte Zugriffssteuerung: Integrierte Rollen](/azure/active-directory/role-based-access-built-in-roles).

Das folgende Beispiel fügt die Rolle **Leser** hinzu und entfernt die Rolle **Mitwirkender**:

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> Cmdlets für die Rollenzuweisung akzeptieren die Objekt-ID des Dienstprinzipals nicht. Sie nehmen die zugeordnete Anwendungs-ID an, die zum Zeitpunkt der Erstellung generiert wird. Verwenden Sie `Get-AzADServicePrincipal` zum Abrufen der Anwendungs-ID für einen Dienstprinzipal.

> [!NOTE]
> Wenn Ihr Konto nicht über die Berechtigung zum Zuweisen einer Rolle verfügt, wird eine Fehlermeldung mit dem Hinweis angezeigt, dass Ihr Konto keine Berechtigung zum Ausführen der Aktion „Microsoft.Authorization/roleAssignments/write“ hat. Bitten Sie den Azure Active Directory-Administrator um die Verwaltung von Rollen.

Durch das Hinzufügen einer Rolle werden zuvor zugewiesene Berechtigungen _nicht_ eingeschränkt. Beim Einschränken der Berechtigungen eines Dienstprinzipals sollte die Rolle **Mitwirkender** entfernt werden.

Die Änderungen können durch Auflisten der zugewiesenen Rollen überprüft werden:

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>Anmelden mithilfe eines Dienstprinzipals

Testen Sie die Anmeldeinformationen und Berechtigungen des neuen Dienstprinzipals, indem Sie sich anmelden. Zur Anmeldung bei einem Dienstprinzipal benötigen Sie den `applicationId`-Wert, der ihm zugeordnet ist, und den Mandanten, unter dem er erstellt wurde.

So melden Sie sich mit einem Dienstprinzipal und einem Kennwort an:

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

Zertifikatbasierte Authentifizierung erfordert, dass Azure PowerShell Informationen von einem lokalen Zertifikatsspeicher basierend auf einem Fingerabdruck des Zertifikats abrufen kann.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

Anweisungen zum Importieren eines Zertifikats in einen für PowerShell zugänglichen Anmeldeinformationsspeicher finden Sie unter [Anmelden mit Azure PowerShell](authenticate-azureps.md#sp-signin).

## <a name="reset-credentials"></a>Zurücksetzen von Anmeldeinformation

Wenn Sie die Anmeldeinformationen für einen Dienstprinzipal vergessen, verwenden Sie [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential), um neue Anmeldeinformationen mit einem zufälligen Kennwort hinzuzufügen. Dieses Cmdlet unterstützt beim Zurücksetzen des Kennworts keine benutzerdefinierten Anmeldeinformationen.

> [!IMPORTANT]
> Vor dem Zuweisen von neuen Anmeldeinformationen empfiehlt es sich, vorhandene Anmeldeinformationen zu entfernen, um eine versehentliche Anmeldung damit zu verhindern. Verwenden Sie dazu das Cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a>Problembehandlung

Bei Anzeige der Fehlermeldung _„New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists.“_ stellen Sie sicher, dass noch kein Dienstprinzipal mit dem gleichen Namen vorhanden ist.

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Wenn der vorhandene Dienstprinzipal nicht mehr benötigt wird, können Sie ihn mit dem folgenden Beispiel entfernen.

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Dieser Fehler kann auch auftreten, wenn Sie zuvor einen Dienstprinzipal für eine Azure Active Directory-Anwendung erstellt haben. Wenn Sie den Dienstprinzipal entfernen, ist die Anwendung weiterhin verfügbar. Diese Anwendung verhindert, dass Sie einen anderen Dienstprinzipal mit demselben Namen erstellen.

Verwenden Sie das folgende Beispiel, um zu überprüfen, ob bereits eine Azure Active Directory-Anwendung mit demselben Namen vorhanden ist:

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

Wenn eine Anwendung mit demselben Namen vorhanden ist und nicht mehr benötigt wird, kann Sie mithilfe des folgenden Beispiels entfernt werden.

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

Wählen Sie andernfalls einen alternativen Namen für den neuen Dienstprinzipal aus, den Sie erstellen möchten.
