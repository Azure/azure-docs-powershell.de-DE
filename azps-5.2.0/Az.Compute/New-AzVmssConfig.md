---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372628"
---
# <span data-ttu-id="4dc39-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4dc39-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="4dc39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc39-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc39-103">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="4dc39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dc39-104">SYNTAX</span></span>

### <span data-ttu-id="4dc39-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4dc39-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc39-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dc39-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4dc39-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4dc39-107">DESCRIPTION</span></span>
<span data-ttu-id="4dc39-108">Das **Cmdlet "New-AzVmssConfig"** erstellt ein konfigurierbares lokales Virtual Manager Scale Set (VMSS)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="4dc39-109">Weitere Cmdlets sind zum Konfigurieren des VMSS-Objekts erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4dc39-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="4dc39-110">Diese Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="4dc39-110">These cmdlets are:</span></span>
- <span data-ttu-id="4dc39-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="4dc39-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="4dc39-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="4dc39-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="4dc39-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4dc39-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="4dc39-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4dc39-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="4dc39-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4dc39-115">EXAMPLES</span></span>

### <span data-ttu-id="4dc39-116">Beispiel 1: Erstellen eines VMSS-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="4dc39-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="4dc39-117">In diesem Beispiel wird ein VMSS-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="4dc39-118">Der erste Befehl verwendet das **Cmdlet "New-AzVmssConfig",** um ein VMSS-Konfigurationsobjekt zu erstellen, und speichert das Ergebnis in der Variablen namens $VMSS.</span><span class="sxs-lookup"><span data-stu-id="4dc39-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="4dc39-119">Der zweite Befehl verwendet das **Cmdlet "New-AzVmss",** um ein VMSS zu erstellen, das das im ersten Befehl erstellte VMSS-Konfigurationsobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="4dc39-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="4dc39-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4dc39-120">Example 2</span></span>

<span data-ttu-id="4dc39-121">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="4dc39-122">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="4dc39-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="4dc39-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dc39-123">PARAMETERS</span></span>

### <span data-ttu-id="4dc39-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="4dc39-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="4dc39-125">Die Zeit, für die automatische Reparaturen aufgrund einer Zustandsänderung auf vm angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="4dc39-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="4dc39-126">Die Nachfrist beginnt nach Abschluss der Zustandsänderung.</span><span class="sxs-lookup"><span data-stu-id="4dc39-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="4dc39-127">Dadurch können vorzeitig oder versehentliche Reparaturen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="4dc39-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="4dc39-128">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4dc39-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="4dc39-129">Die zulässige Nachfrist beträgt 30 Minuten (PT30M), was auch der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="4dc39-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="4dc39-130">Die maximal zulässige Nachfrist beträgt 90 Minuten (PT90M).</span><span class="sxs-lookup"><span data-stu-id="4dc39-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="4dc39-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="4dc39-132">Legt fest, ob Betriebssystemupgrade automatisch auf Skalierungssatzinstanzen fortlaufend angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="4dc39-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="4dc39-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4dc39-133">-BootDiagnostic</span></span>
<span data-ttu-id="4dc39-134">Gibt das Profil der Startdiagnose für den Skalierungssatz des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc39-135">-DefaultProfile</span></span>
<span data-ttu-id="4dc39-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dc39-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dc39-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="4dc39-137">-DisableAutoRollback</span></span>
<span data-ttu-id="4dc39-138">Deaktivieren des automatischen Rollbacks für die Upgraderichtlinie für das automatische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="4dc39-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="4dc39-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="4dc39-140">Ermöglicht automatische Reparaturen für den Skalierungssatz des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="4dc39-140">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="4dc39-141">-EnableUltraSSD</span></span>
<span data-ttu-id="4dc39-142">Ermöglicht es einer Funktion, eine oder mehrere verwaltete Datenträger mit UltraSSD_LRS Speicherkontotyp auf dem Skalierungssatz des virtuellen Computers zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4dc39-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="4dc39-143">Verwaltete Datenträger mit speicherkontotyp UltraSSD_LRS können einem VMSS nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4dc39-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="4dc39-144">-EncryptionAtHost</span></span>
<span data-ttu-id="4dc39-145">Dieser Parameter aktiviert die Verschlüsselung für alle Datenträger, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst.</span><span class="sxs-lookup"><span data-stu-id="4dc39-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="4dc39-146">Standard: Die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dc39-147">-EvictionPolicy</span></span>
<span data-ttu-id="4dc39-148">Gibt die Entfernungsrichtlinie für die virtuellen Computer im Skalierungssatz an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-149">-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="4dc39-149">-Extension</span></span>
<span data-ttu-id="4dc39-150">Gibt das Erweiterungsinformationsobjekt für die VMSS an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="4dc39-151">Sie können das **Cmdlet "Add-AzVmssExtension"** verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4dc39-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="4dc39-152">-HealthProbeId</span></span>
<span data-ttu-id="4dc39-153">Gibt die ID einer Lastenausgleichssonde an, mit der die Integrität einer Instanz im Skalierungssatz des virtuellen Computers ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4dc39-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="4dc39-154">HealthProbeId liegt in Form von '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}' vor.</span><span class="sxs-lookup"><span data-stu-id="4dc39-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="4dc39-155">-IdentityId</span></span>
<span data-ttu-id="4dc39-156">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungssatz für den virtuellen Computer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4dc39-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="4dc39-157">Die Benutzeridentitätsverweise werden ARM Ressourcen-ID im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' angegeben.</span><span class="sxs-lookup"><span data-stu-id="4dc39-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4dc39-158">-IdentityType</span></span>
<span data-ttu-id="4dc39-159">Gibt den Identitätstyp an, der für den Skalierungssatz des virtuellen Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4dc39-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="4dc39-160">Der Typ "SystemAssignedUserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Gruppe von vom Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="4dc39-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="4dc39-161">Mit dem Typ "None" werden alle Identitäten aus dem Skalierungssatz des virtuellen Computers entfernt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="4dc39-162">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4dc39-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dc39-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="4dc39-163">SystemAssigned</span></span>
- <span data-ttu-id="4dc39-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="4dc39-164">UserAssigned</span></span>
- <span data-ttu-id="4dc39-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="4dc39-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="4dc39-166">Keine</span><span class="sxs-lookup"><span data-stu-id="4dc39-166">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4dc39-167">-LicenseType</span></span>
<span data-ttu-id="4dc39-168">Geben Sie den Lizenztyp an, mit dem Sie Ihr eigenes Lizenzszenario erstellen können.</span><span class="sxs-lookup"><span data-stu-id="4dc39-168">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-169">-Location</span><span class="sxs-lookup"><span data-stu-id="4dc39-169">-Location</span></span>
<span data-ttu-id="4dc39-170">Gibt den Azure-Speicherort an, an dem der VMSS erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4dc39-170">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="4dc39-171">-MaxPrice</span></span>
<span data-ttu-id="4dc39-172">Gibt den maximal zulässigen Preis für eine Spot VM/VMSS an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="4dc39-173">Dieser Preis wird in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="4dc39-173">This price is in US Dollars.</span></span> <span data-ttu-id="4dc39-174">Dieser Preis wird mit dem aktuellen Spotpreis für die Größe der VM verglichen.</span><span class="sxs-lookup"><span data-stu-id="4dc39-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="4dc39-175">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von Spot VM/VMSS verglichen, und der Vorgang ist nur erfolgreich, wenn der max.Preis höher als der aktuelle Spotpreis ist.</span><span class="sxs-lookup"><span data-stu-id="4dc39-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="4dc39-176">Der maxPrice wird auch zum Entfernung einer Spot VM/VMSS verwendet, wenn der aktuelle Spotpreis nach der Erstellung von VM/VMSS über den maxPrice hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="4dc39-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="4dc39-177">Mögliche Werte sind: beliebige Dezimalwerte größer als Null.</span><span class="sxs-lookup"><span data-stu-id="4dc39-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="4dc39-178">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="4dc39-178">Example: 0.01538.</span></span>  <span data-ttu-id="4dc39-179">-1 gibt an, dass die Spot VM/VMSS aus Preisgründen nicht entfernt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="4dc39-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="4dc39-180">Außerdem beträgt der standardmäßige maximaler Preis -1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4dc39-180">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4dc39-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="4dc39-182">Gibt das Netzwerkprofilobjekt an, das die Netzwerkeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="4dc39-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="4dc39-183">Sie können das **Cmdlet "Add-AzVmssNetworkInterfaceConfiguration"** verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4dc39-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="4dc39-184">-OsProfile</span></span>
<span data-ttu-id="4dc39-185">Gibt das Betriebssystemprofilobjekt an, das die Betriebssystemeigenschaften für die KONFIGURATION der VMSS enthält.</span><span class="sxs-lookup"><span data-stu-id="4dc39-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="4dc39-186">Sie können dieses Objekt mithilfe des **Cmdlets "Set-AzVmssOsProfile"** festlegen.</span><span class="sxs-lookup"><span data-stu-id="4dc39-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="4dc39-187">-Overprovision</span></span>
<span data-ttu-id="4dc39-188">Gibt an, ob das Cmdlet die VMSS übergibt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="4dc39-189">-PlanName</span></span>
<span data-ttu-id="4dc39-190">Gibt den Plannamen an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-190">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="4dc39-191">-PlanProduct</span></span>
<span data-ttu-id="4dc39-192">Gibt das Planprodukt an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-192">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="4dc39-193">-PlanPromotionCode</span></span>
<span data-ttu-id="4dc39-194">Gibt den Promotionscode für den Plan an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-194">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4dc39-195">-PlanPublisher</span></span>
<span data-ttu-id="4dc39-196">Gibt den Planherausgeber an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-196">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="4dc39-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="4dc39-198">Anzahl der Fehlerdomänen für jede Platzierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4dc39-198">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-199">-Priority</span><span class="sxs-lookup"><span data-stu-id="4dc39-199">-Priority</span></span>
<span data-ttu-id="4dc39-200">Die Priorität für die virtuellen "anderen" im Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="4dc39-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="4dc39-201">Nur unterstützte Werte sind "Regular", "Spot" und "Low".</span><span class="sxs-lookup"><span data-stu-id="4dc39-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="4dc39-202">"Regular" ist für normale virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="4dc39-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="4dc39-203">"Spot" ist für virtuelle Spotcomputer.</span><span class="sxs-lookup"><span data-stu-id="4dc39-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="4dc39-204">"Low" ist auch für virtuelle Spotcomputer, wird aber durch "Spot" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="4dc39-205">Verwenden Sie "Spot" anstelle von "Niedrig".</span><span class="sxs-lookup"><span data-stu-id="4dc39-205">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4dc39-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="4dc39-207">Die Ressourcen-ID der Näherungsplatzierungsgruppe, die für diesen Skalierungssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4dc39-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="4dc39-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="4dc39-209">Gibt die Rollupgraderichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-209">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="4dc39-210">-ScaleInPolicy</span></span>
<span data-ttu-id="4dc39-211">Die Regeln, die beim Skalieren in einem Skalierungssatz für einen virtuellen Computer zu beachten sind.</span><span class="sxs-lookup"><span data-stu-id="4dc39-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="4dc39-212">Mögliche Werte: "Default", "OldestVM" und "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="4dc39-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="4dc39-213">Wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen, wenn es sich um einen standardmäßigen Skalierungssatz handelt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="4dc39-214">Anschließend wird sie so weit wie möglich über Fehlerdomänen hinweg ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="4dc39-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="4dc39-215">Innerhalb jeder Fault Domain sind die zum Entfernen ausgewählten virtuellen Computer die neuesten Computer, die nicht vor "scale-in" geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="4dc39-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="4dc39-216">"OldestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor "scale-in" geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="4dc39-217">Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="4dc39-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="4dc39-218">Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="4dc39-219">"NewestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die neuesten virtuellen Computer, die nicht vor scale-in geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="4dc39-220">Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="4dc39-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="4dc39-221">In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4dc39-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="4dc39-223">Gibt die einzelne Platzierungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-223">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="4dc39-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="4dc39-225">Gibt an, dass die Erweiterungen nicht für die zusätzlichen überprovisionierten VMs ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4dc39-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="4dc39-226">-Sku1</span><span class="sxs-lookup"><span data-stu-id="4dc39-226">-SkuCapacity</span></span>
<span data-ttu-id="4dc39-227">Gibt die Anzahl der Instanzen in der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-227">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4dc39-228">-SkuName</span></span>
<span data-ttu-id="4dc39-229">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-229">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4dc39-230">-SkuTier</span></span>
<span data-ttu-id="4dc39-231">Gibt die Stufe von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="4dc39-232">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4dc39-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dc39-233">Standard</span><span class="sxs-lookup"><span data-stu-id="4dc39-233">Standard</span></span>
- <span data-ttu-id="4dc39-234">Standard</span><span class="sxs-lookup"><span data-stu-id="4dc39-234">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="4dc39-235">-StorageProfile</span></span>
<span data-ttu-id="4dc39-236">Gibt das Speicherprofilobjekt an, das die Datenträgereigenschaften für die KONFIGURATION der VMSS enthält.</span><span class="sxs-lookup"><span data-stu-id="4dc39-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="4dc39-237">Sie können dieses Objekt mithilfe des **Cmdlets "Set-AzVmssStorageProfile"** festlegen.</span><span class="sxs-lookup"><span data-stu-id="4dc39-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="4dc39-238">-Tag</span></span>
<span data-ttu-id="4dc39-239">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4dc39-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4dc39-240">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="4dc39-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4dc39-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="4dc39-242">Eine konfigurierbare Dauer (in Minuten) für einen gelöschten virtuellen Computer muss potenziell das Ereignis "Terminiertes Ereignis beenden" genehmigen, bevor das Ereignis automatisch genehmigt (Timed out) wird.</span><span class="sxs-lookup"><span data-stu-id="4dc39-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="4dc39-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="4dc39-244">Aktivieren der Ereignisse "Termin planmäßig beenden"</span><span class="sxs-lookup"><span data-stu-id="4dc39-244">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="4dc39-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="4dc39-246">Der Modus für ein Upgrade auf virtuelle Computer wurde im Skalierungssatz angegeben.</span><span class="sxs-lookup"><span data-stu-id="4dc39-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="4dc39-247">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4dc39-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dc39-248">Automatisch</span><span class="sxs-lookup"><span data-stu-id="4dc39-248">Automatic</span></span>
- <span data-ttu-id="4dc39-249">Manuell</span><span class="sxs-lookup"><span data-stu-id="4dc39-249">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="4dc39-250">-Zone</span></span>
<span data-ttu-id="4dc39-251">Gibt die Zonenliste für den Skalierungssatz des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="4dc39-251">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc39-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="4dc39-252">-ZoneBalance</span></span>
<span data-ttu-id="4dc39-253">Ob sie für den Fall, dass es zu einem Zonenausfall kommt, ausschließlich eine X-Zone-übergreifende Virtual Machine-Verteilung erzwingen soll.</span><span class="sxs-lookup"><span data-stu-id="4dc39-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="4dc39-254">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dc39-254">-Confirm</span></span>
<span data-ttu-id="4dc39-255">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4dc39-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc39-256">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4dc39-256">-WhatIf</span></span>
<span data-ttu-id="4dc39-257">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4dc39-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dc39-258">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4dc39-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc39-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc39-259">CommonParameters</span></span>
<span data-ttu-id="4dc39-260">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc39-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc39-261">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dc39-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc39-262">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4dc39-262">INPUTS</span></span>

### <span data-ttu-id="4dc39-263">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4dc39-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4dc39-264">System.String</span><span class="sxs-lookup"><span data-stu-id="4dc39-264">System.String</span></span>

### <span data-ttu-id="4dc39-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4dc39-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4dc39-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4dc39-266">System.Int32</span></span>

### <span data-ttu-id="4dc39-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4dc39-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="4dc39-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="4dc39-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="4dc39-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="4dc39-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="4dc39-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="4dc39-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="4dc39-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="4dc39-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="4dc39-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4dc39-272">System.String[]</span></span>

### <span data-ttu-id="4dc39-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="4dc39-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="4dc39-274">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4dc39-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4dc39-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4dc39-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="4dc39-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4dc39-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="4dc39-277">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4dc39-277">OUTPUTS</span></span>

### <span data-ttu-id="4dc39-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4dc39-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4dc39-279">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4dc39-279">NOTES</span></span>

## <span data-ttu-id="4dc39-280">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4dc39-280">RELATED LINKS</span></span>

[<span data-ttu-id="4dc39-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="4dc39-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="4dc39-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="4dc39-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="4dc39-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4dc39-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="4dc39-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4dc39-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="4dc39-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4dc39-285">New-AzVmss</span></span>](./New-AzVmss.md)
