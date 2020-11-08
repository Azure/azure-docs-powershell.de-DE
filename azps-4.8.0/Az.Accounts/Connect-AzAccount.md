---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 073a70077eabbdf20d72874b22c11b7f0dae2844
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166639"
---
# Connect-AzAccount

## Synopsis
Stellen Sie eine Verbindung mit Azure mit einem authentifizierten Konto für die Verwendung mit Cmdlets aus den AZ PowerShell-Modulen her.

## Syntax

### UserWithSubscriptionId (Standard)
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung

Das `Connect-AzAccount` Cmdlet stellt eine Verbindung zu Azure mit einem authentifizierten Konto für die Verwendung mit Cmdlets aus den AZ PowerShell-Modulen her. Sie können dieses authentifizierte Konto nur mit Azure-Ressourcen-Manager-Anforderungen verwenden. Verwenden Sie zum Hinzufügen eines authentifizierten Kontos zur Verwendung mit der Dienstverwaltung das `Add-AzureAccount` Cmdlet aus dem Azure PowerShell-Modul. Wenn für den aktuellen Benutzer kein Kontext gefunden wird, wird die Kontextliste des Benutzers mit einem Kontext für jedes der ersten 25 Abonnements aufgefüllt.
Die Liste der für den Benutzer erstellten Kontexte kann durch Ausführen gefunden werden `Get-AzContext -ListAvailable` . Um diesen Kontext zu überspringen, geben Sie den **SkipContextPopulation** -Schalterparameter an. Nachdem Sie dieses Cmdlet ausgeführt haben, können Sie die Verbindung mit einem Azure-Konto mithilfe von beenden `Disconnect-AzAccount` .

## Beispiele

### Beispiel 1: Herstellen einer Verbindung mit einem Azure-Konto

In diesem Beispiel wird eine Verbindung mit einem Azure-Konto hergestellt. Sie müssen ein Microsoft-Konto oder Organisations-ID-Anmeldeinformationen angeben. Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipal Authentifizierung verwenden.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 2: (nur Windows PowerShell 5,1) Herstellen einer Verbindung mit Azure mithilfe der Organisations-ID-Anmeldeinformationen

Dieses Szenario funktioniert nur in Windows PowerShell 5,1. Der erste Befehl fordert Benutzeranmeldeinformationen an und speichert Sie in der `$Credential` Variablen. Der zweite Befehl stellt eine Verbindung mit einem Azure-Konto unter Verwendung der in gespeicherten Anmeldeinformationen her `$Credential` . Dieses Konto authentifiziert sich bei Azure mithilfe der Anmeldeinformationen für die Organisations-ID.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 3: Herstellen einer Verbindung mit Azure mithilfe eines Dienstprinzipal Kontos

Der erste Befehl fordert die Anmeldeinformationen des Dienst Prinzipals an und speichert Sie in der `$Credential` Variablen. Geben Sie die Anwendungs-ID für den Benutzernamen und den Dienstprinzipal Schlüssel als Kennwort ein, wenn Sie dazu aufgefordert werden. Der zweite Befehl verbindet den angegebenen Azure-Mandanten mit den Dienstprinzipal Anmeldeinformationen, die in der Variablen gespeichert sind `$Credential` . Der **ServicePrincipal** -Parameter "Switch" gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 4: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem bestimmten Mandanten und einem Abonnement

In diesem Beispiel wird eine Verbindung mit einem Azure-Konto mit dem angegebenen Mandanten und Abonnement hergestellt.

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 5: Herstellen einer Verbindung mit einer verwalteten Dienstidentität

In diesem Beispiel wird die Verbindung mit der Managed Service Identity (MSI) der Hostumgebung hergestellt. Sie können sich beispielsweise von einem virtuellen Computer mit einer zugewiesenen MSI-Nummer bei Azure anmelden.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 6: Herstellen einer Verbindung mit der Anmelde-und ClientID der Managed Service Identity

In diesem Beispiel wird eine Verbindung mit der verwalteten Dienstidentität von **myUserAssignedIdentity** hergestellt. Sie fügt dem virtuellen Computer die dem Benutzer zugewiesene Identität hinzu und stellt dann eine Verbindung mit dem ClientID der Benutzer zugewiesenen Identität her. Weitere Informationen finden Sie unter [Konfigurieren von verwalteten Identitäten für Azure-Ressourcen auf einem Azure-VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 7: Herstellen einer Verbindung mit Zertifikaten

In diesem Beispiel wird eine Verbindung mit einem Azure-Konto mithilfe der zertifikatbasierten Dienstprinzipal Authentifizierung hergestellt.
Der für die Authentifizierung verwendete Dienstprinzipal muss mit dem angegebenen Zertifikat erstellt werden. Weitere Informationen zum Erstellen von selbstsignierten Zertifikaten und Zuweisen von Berechtigungen finden Sie unter [Verwenden von Azure PowerShell zum Erstellen eines Dienst Prinzipals mit einem Zertifikat](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## Parameter

### -Access Token

Gibt ein Zugriffstoken an.

> [!CAUTION]
> Zugriffstoken sind eine Art von Anmeldeinformationen. Sie sollten die entsprechenden Sicherheitsvorkehrungen treffen, um diese vertraulich zu behandeln. Zugriffstokens auch Timeout und können verhindern, dass lange ausgeführte Aufgaben abgeschlossen werden.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konto-Nr

Konto-ID für Zugriffstoken in **Access Token** -Parametersatz. Konto-ID für verwalteten Dienst in **ManagedService** -Parametersatz. Kann eine Ressourcen-ID des verwalteten Diensts oder die zugehörige Client-ID sein.
Wenn Sie die dem System zugewiesene Identität verwenden möchten, lassen Sie dieses Feld leer.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

Anwendungs-ID des Dienst Prinzipals.

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint

Zertifikat Hash oder Fingerabdruck

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contextname

Der Name des standardmäßigen Azure-Kontexts für diesen Anmeldenamen. Weitere Informationen zu Azure-Kontexten finden Sie unter [Azure PowerShell-Kontextobjekte](/powershell/azure/context-persistence).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Anmeldeinformationen

Gibt ein **PSCredential** -Objekt an. Wenn Sie weitere Informationen zum **PSCredential** -Objekt wünschen, geben Sie `Get-Help Get-Credential` . Das **PSCredential** -Objekt enthält die Benutzer-ID und das Kennwort für die Anmeldeinformationen für die Organisations-ID oder die Anwendungs-ID und den Schlüssel für die Anmeldeinformationen des Dienst Prinzipals.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile

Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Umgebung

Umgebung, die das Azure-Konto enthält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Überschreiben Sie den vorhandenen Kontext mit demselben Namen ohne Aufforderung.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken

Access Token for Graph-Dienst.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

Melden Sie sich mit einer verwalteten Dienstidentität an.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultAccessToken

Access Token für keyvault-Dienst.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceHostName

Hostname für den verwalteten Dienst

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServicePort

Port Nummer für den verwalteten Dienst

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceSecret

Token für die Anmeldung des verwalteten Diensts.

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxContextPopulation

Maximale Abonnementnummer zum Auffüllen von Kontexten nach der Anmeldung. Der Standardwert ist 25. Wenn Sie alle Abonnements für Kontexte auffüllen möchten, setzen Sie auf-1.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope

Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal

Gibt an, dass sich dieses Konto durch die Bereitstellung von Dienstprinzipal Anmeldeinformationen authentifiziert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipContextPopulation

Überspringt die Kontext Auffüllung, wenn keine Zusammenhänge gefunden werden.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipValidation

Überprüfung für Zugriffstoken überspringen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement

Name oder ID des Abonnements.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Mandant

Optionaler Mandantenname oder ID.

> [!NOTE]
> Aufgrund von Einschränkungen der aktuellen API müssen Sie beim Herstellen einer Verbindung mit einem Business-to-Business (B2B)-Konto eine Mandanten-ID anstelle eines Mandantennamens verwenden.

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDeviceAuthentication

Verwenden Sie die Gerätecode Authentifizierung anstelle eines Browsersteuerelements. Dies ist der Standard Authentifizierungstyp für PowerShell ab Version 6.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen

Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. profile. Models. Core. PSAzureProfile

## Notizen

## Verwandte Links
