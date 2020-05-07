---
title: Anmelden mit Azure PowerShell
description: Es wird beschrieben, wie Sie sich mit Azure PowerShell als Benutzer, per Dienstprinzipal oder mit verwalteten Identitäten für Azure-Ressourcen anmelden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 464d7efa640f1d1ffd1c34bfbe6cf13cbe5202b6
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "68863239"
---
# <a name="sign-in-with-azure-powershell"></a>Anmelden mit Azure PowerShell

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell unterstützt mehrere Authentifizierungsmethoden. Die einfachste Möglichkeit ist die interaktive Anmeldung über die Befehlszeile.

## <a name="sign-in-interactively"></a>Interaktives Anmelden

Verwenden Sie für die interaktive Anmeldung das Cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).

```azurepowershell-interactive
Connect-AzureRmAccount
```

Wenn Sie dieses Cmdlet ausführen, wird ein Dialogfeld angezeigt, in dem Sie zur Eingabe Ihrer E-Mail-Adresse und Ihres Kennworts für Ihr Azure-Konto aufgefordert werden. Diese Authentifizierung gilt jeweils für die aktuelle PowerShell-Sitzung.

> [!IMPORTANT]
> Ab Azure PowerShell 6.3.0 werden Ihre Anmeldeinformationen in mehreren PowerShell-Sitzungen gemeinsam verwendet, solange Sie bei Windows angemeldet bleiben. Weitere Informationen finden Sie im Artikel zu [beständigen Anmeldeinformationen](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Anmelden mit einem Dienstprinzipal

Dienstprinzipale sind nicht interaktive Azure-Konten. Wie bei anderen Benutzerkonten auch, werden die Berechtigungen mit Azure Active Directory verwaltet. Indem für einen Dienstprinzipal nur die benötigten Berechtigungen gewährt werden, bleibt die Sicherheit Ihrer Automatisierungsskripts gewahrt.

Informationen zur Erstellung eines Dienstprinzipals für die Verwendung mit PowerShell finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](create-azure-service-principal-azureps.md).

Verwenden Sie für die Anmeldung mit einem Dienstprinzipal das Cmdlet `-ServicePrincipal` mit dem Argument `Connect-AzureRmAccount`. Sie benötigen auch die Anmeldeinformationen des Dienstprinzipals und die dem Dienstprinzipal zugeordnete Mandanten-ID. Verwenden Sie das Cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential), um die Anmeldeinformationen des Dienstprinzipals als entsprechendes Objekt abzurufen. Dieses Cmdlet zeigt ein Dialogfeld für die Eingabe der Benutzer-ID und des Kennworts des Dienstprinzipals an.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Anmelden mit einer verwalteten Azure-Dienstidentität

Verwaltete Identitäten für Azure-Ressourcen ist eine Funktion von Azure Active Directory. Sie können den Dienstprinzipal einer verwalteten Identität für die Anmeldung verwenden und ein App-exklusives Zugriffstoken für den Zugriff auf andere Ressourcen beziehen. Verwaltete Identitäten stehen nur für virtuelle Computer zur Verfügung, die in einer Azure-Cloud ausgeführt werden.

Weitere Informationen zu verwalteten Identitäten für Azure-Ressourcen finden Sie unter [Verwenden von verwalteten Identitäten für Azure-Ressourcen auf einem virtuellen Azure-Computer zum Abrufen eines Zugriffstokens](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>Anmelden als Cloud Solution Provider (CSP)

Eine Anmeldung als [(Cloud Solution Provider, CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/) erfordert die Verwendung von `-TenantId`. In der Regel kann dieser Parameter entweder als Mandanten-ID oder als Domänenname angegeben werden. Für die CSP-Anmeldung muss jedoch eine **Mandanten-ID** bereitgestellt werden.

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Anmelden bei einer anderen Cloud

Azure-Clouddienste verfügen über Umgebungen, die jeweils mit den regionalen Bestimmungen zum Umgang mit Daten konform sind.
Legen Sie die Umgebung für Konten in einer regionalen Cloud fest, wenn Sie sich mit dem Argument `-Environment` anmelden.
Beispiel für den Fall, dass sich Ihr Konto in der Cloud in China befindet:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Mit dem folgenden Befehl wird eine Liste mit den verfügbaren Umgebungen abgerufen:

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Weitere Informationen zum Verwalten des rollenbasierten Zugriffs in Azure

Weitere Informationen zur Authentifizierung und Abonnementverwaltung in Azure finden Sie unter [Verwalten von Konten, Abonnements und Administratorrollen](/azure/active-directory/role-based-access-control-configure).

Azure PowerShell-Cmdlets für die Rollenverwaltung:

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
