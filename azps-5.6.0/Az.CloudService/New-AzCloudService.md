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
# <span data-ttu-id="e0143-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="e0143-101">New-AzCloudService</span></span>

## <span data-ttu-id="e0143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0143-102">SYNOPSIS</span></span>
<span data-ttu-id="e0143-103">Erstellen oder Aktualisieren eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="e0143-103">Create or update a cloud service.</span></span>
<span data-ttu-id="e0143-104">Beachten Sie, dass einige Eigenschaften nur während der Erstellung des Clouddiensts festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="e0143-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="e0143-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0143-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e0143-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0143-106">DESCRIPTION</span></span>
<span data-ttu-id="e0143-107">Erstellen oder Aktualisieren eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="e0143-107">Create or update a cloud service.</span></span>
<span data-ttu-id="e0143-108">Beachten Sie, dass einige Eigenschaften nur während der Erstellung des Clouddiensts festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="e0143-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="e0143-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0143-109">EXAMPLES</span></span>

### <span data-ttu-id="e0143-110">Beispiel 1: Erstellen eines neuen Clouddiensts mit einer einzelnen Rolle</span><span class="sxs-lookup"><span data-stu-id="e0143-110">Example 1: Create new cloud service with single role</span></span>
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

<span data-ttu-id="e0143-111">Über einer Gruppe von Befehlen wird ein Clouddienst mit einer einzigen Rolle erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0143-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="e0143-112">Beispiel 2: Erstellen eines neuen Clouddiensts mit einer einzelnen Rolle und einer RDP-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e0143-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
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

<span data-ttu-id="e0143-113">Über einer Gruppe von Befehlen wird ein Clouddienst mit einer einzelnen Rolle und einer RDP-Erweiterung erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0143-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="e0143-114">Beispiel 3: Erstellen eines neuen Clouddiensts mit einer einzelnen Rolle und einem Zertifikat aus dem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="e0143-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
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

<span data-ttu-id="e0143-115">Über dem Befehlssatz wird ein Clouddienst mit einer einzelnen Rolle und einem Zertifikat aus dem Schlüsseltresor erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0143-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="e0143-116">Beispiel 4: Erstellen eines neuen Clouddiensts mit mehreren Rollen und Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="e0143-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
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

<span data-ttu-id="e0143-117">Über dem Befehlssatz wird ein Clouddienst mit einer einzelnen Rolle und einem Zertifikat aus dem Schlüsseltresor erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0143-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="e0143-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e0143-118">PARAMETERS</span></span>

### <span data-ttu-id="e0143-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0143-119">-AsJob</span></span>
<span data-ttu-id="e0143-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e0143-120">Run the command as a job</span></span>

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

### <span data-ttu-id="e0143-121">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e0143-121">-Configuration</span></span>
<span data-ttu-id="e0143-122">Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="e0143-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

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

### <span data-ttu-id="e0143-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="e0143-123">-ConfigurationUrl</span></span>
<span data-ttu-id="e0143-124">Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="e0143-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="e0143-125">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein. Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0143-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="e0143-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0143-126">-DefaultProfile</span></span>
<span data-ttu-id="e0143-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0143-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0143-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="e0143-128">-ExtensionProfile</span></span>
<span data-ttu-id="e0143-129">Beschreibt ein Clouddiensterweiterungsprofil.</span><span class="sxs-lookup"><span data-stu-id="e0143-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="e0143-130">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu EXTENSIONPROFILE-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e0143-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0143-131">-Location</span><span class="sxs-lookup"><span data-stu-id="e0143-131">-Location</span></span>
<span data-ttu-id="e0143-132">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="e0143-132">Resource location.</span></span>

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

### <span data-ttu-id="e0143-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e0143-133">-Name</span></span>
<span data-ttu-id="e0143-134">Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="e0143-134">Name of the cloud service.</span></span>

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

### <span data-ttu-id="e0143-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0143-135">-NetworkProfile</span></span>
<span data-ttu-id="e0143-136">Netzwerkprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="e0143-137">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e0143-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0143-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e0143-138">-NoWait</span></span>
<span data-ttu-id="e0143-139">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e0143-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e0143-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="e0143-140">-OSProfile</span></span>
<span data-ttu-id="e0143-141">Beschreibt das Betriebssystemprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="e0143-142">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu OSPROFILE-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e0143-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0143-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="e0143-143">-PackageUrl</span></span>
<span data-ttu-id="e0143-144">Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="e0143-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="e0143-145">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein. Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0143-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="e0143-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0143-146">-ResourceGroupName</span></span>
<span data-ttu-id="e0143-147">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0143-147">Name of the resource group.</span></span>

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

### <span data-ttu-id="e0143-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="e0143-148">-RoleProfile</span></span>
<span data-ttu-id="e0143-149">Beschreibt das Rollenprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="e0143-150">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu ROLLENPROFIL-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e0143-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0143-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="e0143-151">-StartCloudService</span></span>
<span data-ttu-id="e0143-152">(Optional) Gibt an, ob der Clouddienst unmittelbar nach seiner Er erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0143-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="e0143-153">Der Standardwert ist `true` . Ist false, wird das Dienstmodell weiterhin bereitgestellt, der Code wird jedoch nicht sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0143-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="e0143-154">Stattdessen wird der Dienst bis zum Aufrufen von Start eingeschaltet, zu dem der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e0143-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="e0143-155">Für einen bereitgestellten Dienst fallen weiterhin Gebühren an, auch wenn er ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="e0143-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

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

### <span data-ttu-id="e0143-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0143-156">-SubscriptionId</span></span>
<span data-ttu-id="e0143-157">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e0143-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e0143-158">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="e0143-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e0143-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0143-159">-Tag</span></span>
<span data-ttu-id="e0143-160">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="e0143-160">Resource tags.</span></span>

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

### <span data-ttu-id="e0143-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e0143-161">-UpgradeMode</span></span>
<span data-ttu-id="e0143-162">Updatemodus für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="e0143-163">Rolleninstanzen werden zugewiesen, um Domänen zu aktualisieren, wenn der Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e0143-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="e0143-164">Updates können in jeder Updatedomäne manuell initiiert oder automatisch in allen Updatedomänen initiiert werden. Mögliche Werte sind \<br /\> \<br /\> **Auto** \<br /\> \<br /\> **Manual** \<br /\> \<br /\> **Simultaneous Wenn** nicht \<br /\> \<br /\> angegeben, ist der Standardwert Auto. Wenn auf Manuell festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="e0143-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="e0143-165">Wenn auf Auto festgelegt ist, wird das Update automatisch auf jede Updatedomäne in der Reihenfolge angewendet.</span><span class="sxs-lookup"><span data-stu-id="e0143-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

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

### <span data-ttu-id="e0143-166">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0143-166">-Confirm</span></span>
<span data-ttu-id="e0143-167">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0143-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0143-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0143-168">-WhatIf</span></span>
<span data-ttu-id="e0143-169">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0143-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0143-170">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0143-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0143-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0143-171">CommonParameters</span></span>
<span data-ttu-id="e0143-172">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0143-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0143-173">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0143-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0143-174">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0143-174">INPUTS</span></span>

## <span data-ttu-id="e0143-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0143-175">OUTPUTS</span></span>

### <span data-ttu-id="e0143-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="e0143-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="e0143-177">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e0143-177">NOTES</span></span>

<span data-ttu-id="e0143-178">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e0143-178">ALIASES</span></span>

<span data-ttu-id="e0143-179">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e0143-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0143-180">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="e0143-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0143-181">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0143-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0143-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile> : Beschreibt ein Clouddiensterweiterungsprofil.</span><span class="sxs-lookup"><span data-stu-id="e0143-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="e0143-183">`[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="e0143-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform ein automatisches Upgrade von typeHandlerVersion auf höhere Nebenversionen durchführen kann, wenn sie verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="e0143-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="e0143-185">`[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="e0143-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="e0143-186">Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e0143-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="e0143-187">Wenn forceUpdateTag nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="e0143-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="e0143-188">Wenn sich weder forceUpdateTag noch eine der öffentlichen oder geschützten Einstellungen ändert, würde die Erweiterung zur Rolleninstanz mit derselben Sequenznummer fließen, und es liegt an der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e0143-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="e0143-189">`[Name <String>]`: Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="e0143-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="e0143-190">`[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0143-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="e0143-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e0143-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="e0143-192">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="e0143-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="e0143-193">`[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="e0143-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="e0143-194">Wenn keine Eigenschaft angegeben oder "\*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.</span><span class="sxs-lookup"><span data-stu-id="e0143-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="e0143-195">`[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="e0143-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="e0143-196">Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="e0143-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="e0143-197">Für die XML-Erweiterung (z. B. RDP) ist dies die XML-Einstellung für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="e0143-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="e0143-198">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e0143-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="e0143-199">`[Type <String>]`: Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="e0143-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="e0143-200">`[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="e0143-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="e0143-201">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="e0143-201">Specifies the version of the extension.</span></span> <span data-ttu-id="e0143-202">Wenn dieses Element nicht angegeben ist oder ein Sternchen (\*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0143-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="e0143-203">Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e0143-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="e0143-204">Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben werden, wird die spezifische Erweiterungsversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e0143-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="e0143-205">Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0143-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="e0143-206">NETWORKPROFILE <ICloudServiceNetworkProfile> : Netzwerkprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="e0143-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Load Balancer-Konfigurationen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="e0143-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP</span><span class="sxs-lookup"><span data-stu-id="e0143-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="e0143-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e0143-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="e0143-210">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die vom Clouddienst verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e0143-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="e0143-211">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e0143-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="e0143-212">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e0143-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="e0143-213">`[Name <String>]`: Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="e0143-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="e0143-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="e0143-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="e0143-215">`[Id <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e0143-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="e0143-216">OSPROFILE <ICloudServiceOSProfile> : Beschreibt das Betriebssystemprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="e0143-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt eine Gruppe von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e0143-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="e0143-218">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e0143-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="e0143-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0143-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="e0143-220">`[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als Geheimer in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="e0143-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="e0143-221">ROLEPROFILE <ICloudServiceRoleProfile> : Beschreibt das Rollenprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="e0143-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e0143-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="e0143-223">`[Name <String>]`: Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e0143-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="e0143-224">`[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="e0143-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="e0143-225">`[SkuName <String>]`: Der Name der Sku.</span><span class="sxs-lookup"><span data-stu-id="e0143-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="e0143-226">HINWEIS: Wenn die neue SKU auf der Hardware, auf der sich der Clouddienst derzeit befindet, nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten Sku zurück wechseln.</span><span class="sxs-lookup"><span data-stu-id="e0143-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="e0143-227">`[SkuTier <String>]`: Gibt die Ebene des Clouddiensts an.</span><span class="sxs-lookup"><span data-stu-id="e0143-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="e0143-228">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="e0143-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="e0143-229">**Standard**</span><span class="sxs-lookup"><span data-stu-id="e0143-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="e0143-230">**Basic**</span><span class="sxs-lookup"><span data-stu-id="e0143-230">**Basic**</span></span>

## <span data-ttu-id="e0143-231">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e0143-231">RELATED LINKS</span></span>

