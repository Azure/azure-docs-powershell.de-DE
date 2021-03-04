---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: dcf4e78e9b6e467961eb05dd141396e426dfe5e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943227"
---
# Connect-AzAccount

## SYNOPSIS
Stellen Sie eine Verbindung mit Azure mit einem authentifizierten Konto zur Verwendung mit Cmdlets aus den Az-PowerShell-Modulen bereit.

## SYNTAX

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

## BESCHREIBUNG

Das Cmdlet stellt eine Verbindung mit Azure mit einem authentifizierten Konto zur Verwendung mit `Connect-AzAccount` Cmdlets aus den Az-PowerShell-Modulen bereit. Sie können dieses authentifizierte Konto nur mit Azure Resource Manager-Anforderungen verwenden. Zum Hinzufügen eines authentifizierten Kontos für die Verwendung mit der Dienstverwaltung verwenden Sie das `Add-AzureAccount` Cmdlet aus dem Azure PowerShell-Modul. Wenn für den aktuellen Benutzer kein Kontext gefunden wird, wird die Kontextliste des Benutzers mit einem Kontext für jedes seiner ersten 25 Abonnements gefüllt.
Die Liste der kontextbezogenen Kontexte, die für den Benutzer erstellt wurden, finden Sie unter `Get-AzContext -ListAvailable` Ausführen von . Um diese Kontextgesamtheit zu überspringen, geben Sie den **Switchparameter SkipContextPopulation** an. Nachdem Sie dieses Cmdlet ausgeführt haben, können Sie die Verbindung mit einem Azure-Konto mithilfe von `Disconnect-AzAccount` trennen.

## BEISPIELE

### Beispiel 1: Herstellen einer Verbindung mit einem Azure-Konto

In diesem Beispiel wird eine Verbindung mit einem Azure-Konto hergestellt. Sie müssen anmeldeinformationen für ein Microsoft-Konto oder eine Organisations-ID angeben. Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipalauthentifizierung verwenden.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 2: (nur Windows PowerShell 5.1) Herstellen einer Verbindung mit Azure mithilfe von Organisations-ID-Anmeldeinformationen

Dieses Szenario funktioniert nur in Windows PowerShell 5.1. Der erste Befehl fordert Benutzeranmeldeinformationen auf und speichert sie in der `$Credential` Variablen. Der zweite Befehl stellt eine Verbindung mit einem Azure-Konto mithilfe der in gespeicherten Anmeldeinformationen `$Credential` bereit. Dieses Konto authentifiziert sich bei Azure mithilfe von Organisations-ID-Anmeldeinformationen.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 3: Herstellen einer Verbindung mit Azure mithilfe eines Dienstprinzipalkontos

Der erste Befehl fordert die Anmeldeinformationen des Dienstprinzipals an und speichert sie in der `$Credential` Variablen. Geben Sie ihre Anwendungs-ID für den geheimen Benutzernamen und dienstprinzipal als Kennwort ein, wenn Sie dazu aufgefordert werden. Der zweite Befehl verbindet den angegebenen Azure-Mandanten mithilfe der Dienstprinzipalanmeldeinformationen, die in der Variablen gespeichert `$Credential` sind. Der **Parameter ServicePrincipal** switch gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 4: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem bestimmten Mandanten und Abonnement

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

In diesem Beispiel wird eine Verbindung mithilfe der Managed Service Identity (MSI) der Hostumgebung hergestellt. Beispielsweise melden Sie sich von einem virtuellen Computer mit einem zugewiesenen MSI bei Azure an.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Beispiel 6: Herstellen einer Verbindung mit der Anmeldung für verwaltete Dienstidentität und ClientId

In diesem Beispiel wird eine Verbindung mit der Verwalteten **Dienstidentität von myUserAssignedIdentity hergestellt.** Es fügt dem virtuellen Computer die dem Benutzer zugewiesene Identität hinzu, und stellt dann eine Verbindung mit der ClientId der zugewiesenen Identität des Benutzers ein. Weitere Informationen finden Sie unter [Konfigurieren verwalteter Identitäten für Azure-Ressourcen auf einer Azure-VM.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)

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

In diesem Beispiel wird eine Verbindung mit einem Azure-Konto mithilfe der zertifikatbasierten Dienstprinzipalauthentifizierung hergestellt.
Der für die Authentifizierung verwendete Dienstprinzipal muss mit dem angegebenen Zertifikat erstellt werden. Weitere Informationen zum Erstellen eines selbst signierten Zertifikats und zum Zuweisen von Berechtigungen finden Sie unter Verwenden von [Azure PowerShell](/azure/active-directory/develop/howto-authenticate-service-principal-powershell) zum Erstellen eines Dienstprinzipals mit einem Zertifikat.

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

## PARAMETER

### -AccessToken

Gibt ein Zugriffstoken an.

> [!CAUTION]
> Zugriffstoken sind eine Art von Anmeldeinformationen. Sie sollten die entsprechenden Sicherheitsvorkehrungen treffen, um sie vertraulich zu halten. Zugriffstoken timeoutn ebenfalls und können verhindern, dass Aufgaben mit langer Ausführungszeit abgeschlossen werden.

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

### -AccountId

Konto-ID für Zugriffstoken im **AccessToken-Parametersatz.** Konto-ID für verwalteten Dienst im **ManagedService-Parametersatz.** Kann eine verwaltete Dienstressourcen-ID oder die zugeordnete Client-ID sein.
Wenn Sie die vom System zugewiesene Identität verwenden möchten, lassen Sie dieses Feld leer.

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

Anwendungs-ID des Dienstprinzipals.

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

Zertifikathash oder Fingerabdruck.

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

### -ContextName

Name des standardmäßigen Azure-Kontexts für diese Anmeldung. Weitere Informationen zu Azure-Kontexten finden Sie unter [Azure PowerShell-Kontextobjekte.](/powershell/azure/context-persistence)

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

### -Anmeldeinformationen

Gibt ein **PSCredential-Objekt** an. Weitere Informationen zum **PSCredential-Objekt** finden Sie unter `Get-Help Get-Credential` . Das **PSCredential-Objekt** stellt die Benutzer-ID und das Kennwort für Organisations-ID-Anmeldeinformationen oder die Anwendungs-ID und den Geheimschutz für Dienstprinzipalanmeldeinformationen zur Verfügung.

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

Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Erzwingen

Überschreiben Sie den vorhandenen Kontext ohne Aufforderung mit demselben Namen.

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

AccessToken für Graph Service.

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

Melden Sie sich mit einer Verwalteten Dienstidentität an.

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

AccessToken für KeyVault Service.

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

Veraltet. Wenn Sie benutzerdefinierte MSI-Endpunkte verwenden möchten, legen Sie die Umgebungsvariable MSI_ENDPOINT fest, z. B. " http://localhost:50342/oauth2/token ". Hostname für den verwalteten Dienst.

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

Veraltet. Wenn Sie benutzerdefinierte MSI-Endpunkte verwenden möchten, legen Sie die Umgebungsvariable MSI_ENDPOINT fest, z. B. " http://localhost:50342/oauth2/token ". Portnummer für den verwalteten Dienst.

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

Veraltet. Wenn Sie angepasste MSI-Geheimtipps verwenden möchten, legen Sie die Umgebungsvariablen MSI_SECRET. Token für die Anmeldung für verwaltete Dienste.

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

Maximale Abonnementnummer zum Auffüllen von Kontexten nach der Anmeldung. Der Standardwert ist 25. Um alle Abonnements in Kontexte zu füllen, legen Sie auf -1 festgelegt.

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

Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.

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

Gibt an, dass sich dieses Konto durch Bereitstellen von Dienstprinzipalanmeldeinformationen authentifiziert.

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

Überspringt die Kontextgesamtheit, wenn keine Kontexte gefunden werden.

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

Überspringen sie die Überprüfung für das Zugriffstoken.

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

Abonnementname oder ID.

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

Optionaler Mandantname oder ID.

> [!NOTE]
> Aufgrund von Einschränkungen der aktuellen API müssen Sie eine Mandanten-ID anstelle eines Mandantennamens verwenden, wenn Sie eine Verbindung mit einem Business-to-Business (B2B)-Konto herstellen.

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

Verwenden Sie die Gerätecodeauthentifizierung anstelle eines Browsersteuerelements.

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

Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile

## NOTIZEN

## VERWANDTE LINKS
