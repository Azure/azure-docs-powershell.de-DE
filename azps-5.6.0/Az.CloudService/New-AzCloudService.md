---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 607ac4e9854f3871c4a9a0f2859c6f1fe555f392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934315"
---
# New-AzCloudService

## SYNOPSIS
Erstellen oder Aktualisieren eines Clouddiensts
Beachten Sie, dass einige Eigenschaften nur während der Erstellung des Clouddiensts festgelegt werden können.

## SYNTAX

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## BESCHREIBUNG
Erstellen oder Aktualisieren eines Clouddiensts
Beachten Sie, dass einige Eigenschaften nur während der Erstellung des Clouddiensts festgelegt werden können.

## BEISPIELE

### Beispiel 1: Erstellen eines neuen Clouddiensts mit einer einzelnen Rolle
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

Über einer Gruppe von Befehlen wird ein Clouddienst mit einer einzigen Rolle erstellt.

### Beispiel 2: Erstellen eines neuen Clouddiensts mit einer einzelnen Rolle und einer RDP-Erweiterung
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

Über einer Gruppe von Befehlen wird ein Clouddienst mit einer einzelnen Rolle und einer RDP-Erweiterung erstellt.

### Beispiel 3: Erstellen eines neuen Clouddiensts mit einer einzelnen Rolle und einem Zertifikat aus dem Schlüsseltresor
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

Über dem Befehlssatz wird ein Clouddienst mit einer einzelnen Rolle und einem Zertifikat aus dem Schlüsseltresor erstellt.

### Beispiel 4: Erstellen eines neuen Clouddiensts mit mehreren Rollen und Erweiterungen
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

Über dem Befehlssatz wird ein Clouddienst mit einer einzelnen Rolle und einem Zertifikat aus dem Schlüsseltresor erstellt.

## PARAMETER

### -AsJob
Ausführen des Befehls als Auftrag

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

### -Konfiguration
Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.

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

### -ConfigurationUrl
Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob-Dienst bezieht.
Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein. Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.

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

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionProfile
Beschreibt ein Clouddiensterweiterungsprofil.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu EXTENSIONPROFILE-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Ressourcenspeicherort.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name des Clouddiensts.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkProfile
Netzwerkprofil für den Clouddienst.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu #A0 und Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Asynchrones Ausführen des Befehls

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

### -OSProfile
Beschreibt das Betriebssystemprofil für den Clouddienst.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu OSPROFILE-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageUrl
Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob-Dienst bezieht.
Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein. Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.

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

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleProfile
Beschreibt das Rollenprofil für den Clouddienst.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu ROLLENPROFIL-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartCloudService
(Optional) Gibt an, ob der Clouddienst unmittelbar nach seiner Er erstellt werden soll.
Der Standardwert ist `true` . Ist false, wird das Dienstmodell weiterhin bereitgestellt, der Code wird jedoch nicht sofort ausgeführt.
Stattdessen wird der Dienst bis zum Aufrufen von Start eingeschaltet, zu dem der Dienst gestartet wird.
Für einen bereitgestellten Dienst fallen weiterhin Gebühren an, auch wenn er ausgeschaltet ist.

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

### -SubscriptionId
Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.
Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Ressourcentags.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeMode
Updatemodus für den Clouddienst.
Rolleninstanzen werden zugewiesen, um Domänen zu aktualisieren, wenn der Dienst bereitgestellt wird.
Updates können in jeder Updatedomäne manuell initiiert oder automatisch in allen Updatedomänen initiiert werden. Mögliche Werte sind \<br /\> \<br /\> **Auto** \<br /\> \<br /\> **Manual** \<br /\> \<br /\> **Simultaneous Wenn** nicht \<br /\> \<br /\> angegeben, ist der Standardwert Auto. Wenn auf Manuell festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden.
Wenn auf Auto festgelegt ist, wird das Update automatisch auf jede Updatedomäne in der Reihenfolge angewendet.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


EXTENSIONPROFILE <ICloudServiceExtensionProfile> : Beschreibt ein Clouddiensterweiterungsprofil.
  - `[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.
    - `[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform ein automatisches Upgrade von typeHandlerVersion auf höhere Nebenversionen durchführen kann, wenn sie verfügbar werden.
    - `[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.         Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.         Wenn forceUpdateTag nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.         Wenn sich weder forceUpdateTag noch eine der öffentlichen oder geschützten Einstellungen ändert, würde die Erweiterung zur Rolleninstanz mit derselben Sequenznummer fließen, und es liegt an der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.
    - `[Name <String>]`: Der Name der Erweiterung.
    - `[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.
    - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
    - `[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.
    - `[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung. Wenn keine Eigenschaft angegeben oder "*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.
    - `[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung. Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung. Für die XML-Erweiterung (z. B. RDP) ist dies die XML-Einstellung für die Erweiterung.
    - `[SourceVaultId <String>]`: Ressourcen-ID
    - `[Type <String>]`: Gibt den Typ der Erweiterung an.
    - `[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an. Gibt die Version der Erweiterung an. Wenn dieses Element nicht angegeben ist oder ein Sternchen (*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet. Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt. Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben werden, wird die spezifische Erweiterungsversion ausgewählt. Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.

NETWORKPROFILE <ICloudServiceNetworkProfile> : Netzwerkprofil für den Clouddienst.
  - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Load Balancer-Konfigurationen für den Clouddienst.
    - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP
      - `[Name <String>]`: 
      - `[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die vom Clouddienst verwiesen wird.
      - `[PublicIPAddressId <String>]`: Ressourcen-ID
      - `[SubnetId <String>]`: Ressourcen-ID
    - `[Name <String>]`: Ressourcenname
  - `[SwappableCloudService <ISubResource>]`: 
    - `[Id <String>]`: Ressourcen-ID

OSPROFILE <ICloudServiceOSProfile> : Beschreibt das Betriebssystemprofil für den Clouddienst.
  - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt eine Gruppe von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.
    - `[SourceVaultId <String>]`: Ressourcen-ID
    - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.
      - `[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als Geheimer in den Schlüsseltresor hochgeladen wurde.

ROLEPROFILE <ICloudServiceRoleProfile> : Beschreibt das Rollenprofil für den Clouddienst.
  - `[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.
    - `[Name <String>]`: Ressourcenname.
    - `[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.
    - `[SkuName <String>]`: Der Name der Sku. HINWEIS: Wenn die neue SKU auf der Hardware, auf der sich der Clouddienst derzeit befindet, nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten Sku zurück wechseln.
    - `[SkuTier <String>]`: Gibt die Ebene des Clouddiensts an. Mögliche Werte sind <br /><br /> **Standard** <br /><br /> **Basic**

## VERWANDTE LINKS

