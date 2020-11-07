---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841103"
---
# Connect-AzAccount

## Synopsis
Herstellen einer Verbindung mit Azure mit einem authentifizierten Konto für die Verwendung mit Azure Resource Manager-Cmdlet-Anforderungen.

## Syntax

### UserWithSubscriptionId (Standard)
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Connect-AzAccount-Cmdlet stellt eine Verbindung zu Azure mit einem authentifizierten Konto für die Verwendung mit Azure Resource Manager-Cmdlet-Anforderungen her.
Sie können dieses authentifizierte Konto nur mit Azure Resource Manager-Cmdlets verwenden.
Verwenden Sie zum Hinzufügen eines authentifizierten Kontos zur Verwendung mit Dienst Verwaltungs-Cmdlets das Add-AzAccount oder das Import-AzPublishSettingsFile-Cmdlet.
Wenn für den aktuellen Benutzer kein Kontext gefunden wird, füllt dieser Befehl die Kontextliste des Benutzers mit einem Kontext für jedes Ihrer (ersten 25) Abonnements auf. Die Liste der für den Benutzer erstellten Kontexte kann durch Ausführen von "Get-AzContext-ListAvailable" gefunden werden. Um diesen Kontext zu überspringen, können Sie diesen Befehl mit dem Switch-Parameter "-SkipContextPopulation" ausführen.
Nachdem Sie dieses Cmdlet ausgeführt haben, können Sie die Verbindung mit einem Azure-Konto mithilfe von Disconnect-AzAccount trennen.

## Beispiele

### Beispiel 1: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem Azure-Konto
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her.
Zum Ausführen von Azure Resource Manager-Cmdlets mit diesem Konto müssen Sie an der Eingabeaufforderung Microsoft-Konto-oder Organisations-ID-Anmeldeinformationen angeben.
Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipal Authentifizierung verwenden.

### Beispiel 2: (nur Windows PowerShell 5,1) Herstellen einer Verbindung mit einem Azure-Konto mithilfe der Organisations-ID-Anmeldeinformationen
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Dieses Szenario funktioniert nur in Windows PowerShell 5,1. Mit dem ersten Befehl werden Benutzeranmeldeinformationen (Benutzername und Kennwort) aufgefordert, und Sie werden dann in der $Credential-Variablen gespeichert.
Der zweite Befehl stellt mithilfe der in $Credential gespeicherten Anmeldeinformationen eine Verbindung mit einem Azure-Konto her.
Dieses Konto authentifiziert sich beim Azure Resource Manager mit den Anmeldeinformationen für die Organisations-ID.
Sie können keine mehrstufigen Authentifizierungs-oder Microsoft-Kontoanmeldeinformationen verwenden, um Azure Resource Manager-Cmdlets mit diesem Konto auszuführen.

### Beispiel 3: Herstellen einer Verbindung mit einem Azure-Dienstprinzipal Konto
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Der erste Befehl ruft die Anmeldeinformationen des Dienst Prinzipals ab (Anwendungs-ID und Dienstprinzipal Schlüssel) und speichert Sie dann in der $Credential-Variablen.
Der zweite Befehl stellt eine Verbindung mit Azure mithilfe der Dienstprinzipal Anmeldeinformationen her, die in $Credential für den angegebenen Mandanten gespeichert sind.
Der ServicePrincipal-Parameter "Switch" gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.

### Beispiel 4: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem Konto für einen bestimmten Mandanten und ein Abonnement
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her und konfiguriert AzureRM PowerShell so, dass Cmdlets für den angegebenen Mandanten und das Abonnement standardmäßig ausgeführt werden.

### Beispiel 5: Hinzufügen eines Kontos mit der Anmeldung für die verwaltete Dienstidentität
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Dieser Befehl stellt eine Verbindung mit der verwalteten Dienstidentität der Hostumgebung her (Wenn beispielsweise auf einem VirtualMachine mit einer zugewiesenen verwalteten Dienstidentität ausgeführt wird, kann der Code mit dieser zugewiesenen Identität angemeldet werden)

### Beispiel 6: Hinzufügen eines Kontos mit der Anmeldung für die verwaltete Dienstidentität und ClientID
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Dieser Befehl stellt eine Verbindung mit der verwalteten Dienstidentität von "myUserAssignedIdentity" her, indem die dem virtuellen Computer zugewiesene Identität des Benutzers hinzugefügt und dann eine Verbindung mit dem ClientID der Benutzer zugewiesenen Identität hergestellt wird.
Weitere Informationen zum Konfigurieren von verwalteten Identitäten finden Sie hier: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .

### Beispiel 7: Hinzufügen eines Kontos mit der Anmeldung für die verwaltete Dienstidentität und ClientID
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Dieser Befehl stellt eine Verbindung mit der verwalteten Dienstidentität von "myUserAssignedIdentity" her, indem die dem virtuellen Computer zugewiesene Identität des Benutzers hinzugefügt und dann eine Verbindung mit der ID der Benutzer zugewiesenen Identität hergestellt wird.
Weitere Informationen zum Konfigurieren von verwalteten Identitäten finden Sie hier: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .

### Beispiel 8: Hinzufügen eines Kontos mithilfe von Zertifikaten
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

Dieser Befehl stellt mithilfe der zertifikatbasierten Dienstprinzipal Authentifizierung eine Verbindung mit einem Azure-Konto her. Der für die Authentifizierung verwendete Dienstprinzipal sollte mit dem angegebenen Zertifikat erstellt worden sein.

### Beispiel 9: Hinzufügen eines Kontos mithilfe der Access Token-Authentifizierung
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her, das in "Konto-Nr" angegeben ist, wobei Access Token und KeyVaultAccessToken bereitgestellt werden.

## Parameter

### -Access Token
Gibt ein Zugriffstoken an.

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
Konto-ID für Zugriffstoken in Access Token-Parametersatz. Konto-ID für verwalteten Dienst in ManagedService-Parametersatz. Kann eine Ressourcen-ID des verwalteten Diensts oder die zugehörige Client-ID sein. Wenn Sie die SystemAssigned-Identität verwenden möchten, lassen Sie dieses Feld leer.

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
SPN

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
Zertifikat Hash (Fingerabdruck)

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
Der Name des Standardkontexts aus dieser Anmeldung.  Nachdem Sie sich angemeldet haben, können Sie diesen Kontext mit diesem Namen auswählen.

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
Gibt ein PSCredential-Objekt an.
Wenn Sie weitere Informationen zum PSCredential-Objekt wünschen, geben Sie Get-Help Get-Credential ein.
Das PSCredential-Objekt enthält die Benutzer-ID und das Kennwort für die Anmeldeinformationen für die Organisations-ID oder die Anwendungs-ID und den Schlüssel für die Anmeldeinformationen des Dienst Prinzipals.

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
Umgebung mit dem Konto, bei dem Sie sich anmelden können

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
Überschreiben Sie den vorhandenen Kontext mit dem gleichen Namen (sofern vorhanden).

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
Access Token for Graph-Dienst

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
Melden Sie sich mit der verwalteten Dienstidentität in der aktuellen Umgebung an.

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
Access Token für keyvault-Dienst

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
Hostname für Managed Service-Anmeldung

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
Port Nummer für die Anmeldung des verwalteten Diensts

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
Secret, wird für einige Arten von Managed-Service-Anmeldungen verwendet.

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
Überprüfung für Zugriffstoken überspringen

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
Name oder ID des Abonnements

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
Optionaler Mandantenname oder ID

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
Verwenden der Gerätecode Authentifizierung anstelle eines Browsersteuerelements

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
