---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: ba44e397aa09834b1371fa9188527a056153017c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937107"
---
# <span data-ttu-id="6a975-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6a975-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="6a975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a975-102">SYNOPSIS</span></span>
<span data-ttu-id="6a975-103">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="6a975-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="6a975-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a975-104">SYNTAX</span></span>

### <span data-ttu-id="6a975-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a975-105">DefaultParameterSet (Default)</span></span>
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

### <span data-ttu-id="6a975-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a975-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="6a975-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a975-107">DESCRIPTION</span></span>
<span data-ttu-id="6a975-108">Das **Cmdlet New-AzVmssConfig** erstellt ein konfigurierbares vmSS-Objekt (Virtual Manager Scale Set).</span><span class="sxs-lookup"><span data-stu-id="6a975-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="6a975-109">Zum Konfigurieren des VMSS-Objekts sind weitere Cmdlets erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6a975-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="6a975-110">Diese Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="6a975-110">These cmdlets are:</span></span>
- <span data-ttu-id="6a975-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="6a975-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="6a975-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6a975-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="6a975-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a975-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="6a975-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6a975-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="6a975-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a975-115">EXAMPLES</span></span>

### <span data-ttu-id="6a975-116">Beispiel 1: Erstellen eines VMSS-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="6a975-116">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="6a975-117">In diesem Beispiel wird ein VMSS-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="6a975-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="6a975-118">Der erste Befehl verwendet das **Cmdlet New-AzVmssConfig** zum Erstellen eines VMSS-Konfigurationsobjekts und speichert das Ergebnis in der Variablen namens $VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a975-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="6a975-119">Der zweite Befehl verwendet das **Cmdlet New-AzVmss,** um einen VMSS zu erstellen, der das im ersten Befehl erstellte VMSS-Konfigurationsobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a975-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="6a975-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6a975-120">Example 2</span></span>

<span data-ttu-id="6a975-121">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="6a975-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="6a975-122">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="6a975-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="6a975-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6a975-123">PARAMETERS</span></span>

### <span data-ttu-id="6a975-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="6a975-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="6a975-125">Die Zeit, für die automatische Reparaturen aufgrund einer Zustandsänderung auf der VM angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="6a975-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="6a975-126">Die Nachfrist beginnt nach Abschluss der Zustandsänderung.</span><span class="sxs-lookup"><span data-stu-id="6a975-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="6a975-127">Dadurch können vorzeitige oder versehentliche Reparaturen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="6a975-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="6a975-128">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6a975-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="6a975-129">Die zulässige Mindestfrist beträgt 30 Minuten (PT30M), was ebenfalls der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="6a975-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="6a975-130">Die maximal zulässige Nachfrist beträgt 90 Minuten (PT90M).</span><span class="sxs-lookup"><span data-stu-id="6a975-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="6a975-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6a975-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="6a975-132">Legt fest, ob Betriebssystemupgrade automatisch auf Skalierungssatzinstanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="6a975-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="6a975-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6a975-133">-BootDiagnostic</span></span>
<span data-ttu-id="6a975-134">Gibt das Profil für die Startdiagnose des Skalierungssatzs für virtuelle Computer an.</span><span class="sxs-lookup"><span data-stu-id="6a975-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="6a975-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a975-135">-DefaultProfile</span></span>
<span data-ttu-id="6a975-136">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a975-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a975-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="6a975-137">-DisableAutoRollback</span></span>
<span data-ttu-id="6a975-138">Deaktivieren des automatischen Rollbacks für die Upgraderichtlinie für das automatische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="6a975-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="6a975-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="6a975-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="6a975-140">Ermöglicht automatische Reparaturen für den Skalierungssatz des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="6a975-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6a975-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="6a975-141">-EnableUltraSSD</span></span>
<span data-ttu-id="6a975-142">Ermöglicht eine Funktion, über eine oder mehrere verwaltete Datenträger mit UltraSSD_LRS Speicherkontotyp im Skalierungssatz des virtuellen Computers zu verfügen.</span><span class="sxs-lookup"><span data-stu-id="6a975-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="6a975-143">Verwaltete Datenträger mit Speicherkontotyp UltraSSD_LRS können einem VMSS nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6a975-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="6a975-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="6a975-144">-EncryptionAtHost</span></span>
<span data-ttu-id="6a975-145">Dieser Parameter aktiviert die Verschlüsselung für alle Datenträger, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst.</span><span class="sxs-lookup"><span data-stu-id="6a975-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="6a975-146">Standard: Die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6a975-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="6a975-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a975-147">-EvictionPolicy</span></span>
<span data-ttu-id="6a975-148">Gibt die Räumungsrichtlinie für die virtuellen Computer im Skalierungssatz an.</span><span class="sxs-lookup"><span data-stu-id="6a975-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="6a975-149">-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="6a975-149">-Extension</span></span>
<span data-ttu-id="6a975-150">Gibt das Erweiterungsinformationsobjekt für den VMSS an.</span><span class="sxs-lookup"><span data-stu-id="6a975-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="6a975-151">Sie können das **Cmdlet Add-AzVmssExtension** verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6a975-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="6a975-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="6a975-152">-HealthProbeId</span></span>
<span data-ttu-id="6a975-153">Gibt die ID eines Load Balancer-Prüfpunkts an, mit dem der Zustand einer Instanz im Skalierungssatz des virtuellen Computers bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="6a975-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="6a975-154">HealthProbeId ist in Form von "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="6a975-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="6a975-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6a975-155">-IdentityId</span></span>
<span data-ttu-id="6a975-156">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungssatz für virtuelle Computer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6a975-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="6a975-157">Die Benutzeridentitätsverweise werden ARM Ressourcen-ID im Formular "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6a975-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="6a975-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6a975-158">-IdentityType</span></span>
<span data-ttu-id="6a975-159">Gibt den Identitätstyp an, der für den Skalierungssatz des virtuellen Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6a975-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="6a975-160">Der Typ "SystemAssignedUserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Gruppe von benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="6a975-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="6a975-161">Mit dem Typ "Keine" werden alle Identitäten aus dem Skalierungssatz für virtuelle Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="6a975-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="6a975-162">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6a975-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a975-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="6a975-163">SystemAssigned</span></span>
- <span data-ttu-id="6a975-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="6a975-164">UserAssigned</span></span>
- <span data-ttu-id="6a975-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="6a975-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="6a975-166">Keine</span><span class="sxs-lookup"><span data-stu-id="6a975-166">None</span></span>

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

### <span data-ttu-id="6a975-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6a975-167">-LicenseType</span></span>
<span data-ttu-id="6a975-168">Geben Sie den Lizenztyp an, der für das Mitbringen Ihres eigenen Lizenzszenarios gilt.</span><span class="sxs-lookup"><span data-stu-id="6a975-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="6a975-169">-Location</span><span class="sxs-lookup"><span data-stu-id="6a975-169">-Location</span></span>
<span data-ttu-id="6a975-170">Gibt den Azure-Speicherort an, an dem der VMSS erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6a975-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="6a975-171">-MaxPreis</span><span class="sxs-lookup"><span data-stu-id="6a975-171">-MaxPrice</span></span>
<span data-ttu-id="6a975-172">Gibt den Höchstpreis an, den Sie für eine Spot-VM/VMSS zahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="6a975-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="6a975-173">Dieser Preis ist in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="6a975-173">This price is in US Dollars.</span></span> <span data-ttu-id="6a975-174">Dieser Preis wird mit dem aktuellen Spotpreis für die Vm-Größe verglichen.</span><span class="sxs-lookup"><span data-stu-id="6a975-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="6a975-175">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von Spot VM/VMSS verglichen, und der Vorgang ist nur erfolgreich, wenn der max.Preis größer als der aktuelle Spotpreis ist.</span><span class="sxs-lookup"><span data-stu-id="6a975-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="6a975-176">Der maxPrice wird auch zum Verdingen einer Spot-VM/VMSS verwendet, wenn der aktuelle Spotpreis nach der Erstellung von VM/VMSS über den maxPreis hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="6a975-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="6a975-177">Mögliche Werte sind: jeder Dezimalwert größer als Null.</span><span class="sxs-lookup"><span data-stu-id="6a975-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="6a975-178">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="6a975-178">Example: 0.01538.</span></span>  <span data-ttu-id="6a975-179">-1 gibt an, dass die Spot-VM/VMSS aus Preisgründen nicht entfernt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="6a975-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="6a975-180">Außerdem ist der standardmäßige Höchstpreis -1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6a975-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="6a975-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a975-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="6a975-182">Gibt das Netzwerkprofilobjekt an, das die Netzwerkeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="6a975-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="6a975-183">Sie können das **Cmdlet Add-AzVmssNetworkInterfaceConfiguration verwenden,** um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6a975-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="6a975-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="6a975-184">-OsProfile</span></span>
<span data-ttu-id="6a975-185">Gibt das Betriebssystemprofilobjekt an, das die Betriebssystemeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="6a975-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="6a975-186">Sie können das **Cmdlet Set-AzVmssOsProfile** verwenden, um dieses Objekt zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="6a975-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="6a975-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="6a975-187">-Overprovision</span></span>
<span data-ttu-id="6a975-188">Gibt an, ob das Cmdlet den VMSS überprovisioniert.</span><span class="sxs-lookup"><span data-stu-id="6a975-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="6a975-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="6a975-189">-PlanName</span></span>
<span data-ttu-id="6a975-190">Gibt den Plannamen an.</span><span class="sxs-lookup"><span data-stu-id="6a975-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="6a975-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="6a975-191">-PlanProduct</span></span>
<span data-ttu-id="6a975-192">Gibt das Planprodukt an.</span><span class="sxs-lookup"><span data-stu-id="6a975-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="6a975-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="6a975-193">-PlanPromotionCode</span></span>
<span data-ttu-id="6a975-194">Gibt den Code für die Planwerbung an.</span><span class="sxs-lookup"><span data-stu-id="6a975-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="6a975-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="6a975-195">-PlanPublisher</span></span>
<span data-ttu-id="6a975-196">Gibt den Planherausgeber an.</span><span class="sxs-lookup"><span data-stu-id="6a975-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="6a975-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="6a975-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="6a975-198">Fehlerdomänenanzahl für jede Platzierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6a975-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="6a975-199">-Priorität</span><span class="sxs-lookup"><span data-stu-id="6a975-199">-Priority</span></span>
<span data-ttu-id="6a975-200">Die Priorität für das virtuelle Machien im Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="6a975-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="6a975-201">Nur unterstützte Werte sind "Normal", "Spot" und "Niedrig".</span><span class="sxs-lookup"><span data-stu-id="6a975-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="6a975-202">"Regular" ist für einen normalen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="6a975-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="6a975-203">"Spot" ist für virtuelle Spotcomputer.</span><span class="sxs-lookup"><span data-stu-id="6a975-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="6a975-204">"Low" ist auch für virtuelle Spotcomputer, wird aber durch "Spot" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6a975-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="6a975-205">Verwenden Sie "Spot" statt "Niedrig".</span><span class="sxs-lookup"><span data-stu-id="6a975-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="6a975-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="6a975-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="6a975-207">Die Ressourcen-ID der Näherungsgruppe, die mit diesem Skalierungssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a975-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="6a975-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="6a975-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="6a975-209">Gibt die Richtlinie für das fortlaufende Upgrade an.</span><span class="sxs-lookup"><span data-stu-id="6a975-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="6a975-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="6a975-210">-ScaleInPolicy</span></span>
<span data-ttu-id="6a975-211">Die Regeln, die beim Skalieren in einem Skalierungssatz für virtuelle Computer befolgt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6a975-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="6a975-212">Mögliche Werte sind: "Standard", "OldestVM" und "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="6a975-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="6a975-213">"Standard", wenn ein Skalierungssatz für virtuelle Computer skaliert wird, wird der Skalierungssatz zuerst über Zonen verteilt, wenn es sich um einen zonalen Skalierungssatz handelt.</span><span class="sxs-lookup"><span data-stu-id="6a975-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="6a975-214">Anschließend wird er so weit wie möglich über Fehlerdomänen hinweg ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="6a975-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="6a975-215">Innerhalb jeder Fehlerdomäne sind die virtuellen Computer, die zum Entfernen ausgewählt wurden, die neuesten, die nicht vor Scale-In geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="6a975-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="6a975-216">"OldestVM", wenn ein Skalierungssatz für virtuelle Computer skaliert wird, werden die ältesten virtuellen Computer ausgewählt, die nicht vor Skalierung geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="6a975-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="6a975-217">Bei Skalierungssätzen virtueller Virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="6a975-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="6a975-218">In jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="6a975-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="6a975-219">Wenn ein Skalierungssatz für virtuelle Computer skaliert wird, werden die neuesten virtuellen Computer, die nicht vor Scale-In geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="6a975-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="6a975-220">Bei Skalierungssätzen virtueller Virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="6a975-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="6a975-221">In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="6a975-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="6a975-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6a975-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="6a975-223">Gibt die einzelne Platzierungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="6a975-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="6a975-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="6a975-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="6a975-225">Gibt an, dass die Erweiterungen nicht auf den zusätzlichen überprovisionierten VMs ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6a975-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="6a975-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6a975-226">-SkuCapacity</span></span>
<span data-ttu-id="6a975-227">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="6a975-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="6a975-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6a975-228">-SkuName</span></span>
<span data-ttu-id="6a975-229">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="6a975-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="6a975-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6a975-230">-SkuTier</span></span>
<span data-ttu-id="6a975-231">Gibt die Ebene von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="6a975-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="6a975-232">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6a975-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a975-233">Standard</span><span class="sxs-lookup"><span data-stu-id="6a975-233">Standard</span></span>
- <span data-ttu-id="6a975-234">Basic</span><span class="sxs-lookup"><span data-stu-id="6a975-234">Basic</span></span>

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

### <span data-ttu-id="6a975-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="6a975-235">-StorageProfile</span></span>
<span data-ttu-id="6a975-236">Gibt das Speicherprofilobjekt an, das die Datenträgereigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="6a975-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="6a975-237">Sie können das **Cmdlet Set-AzVmssStorageProfile** verwenden, um dieses Objekt zu legen.</span><span class="sxs-lookup"><span data-stu-id="6a975-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="6a975-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a975-238">-Tag</span></span>
<span data-ttu-id="6a975-239">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6a975-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a975-240">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6a975-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6a975-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6a975-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="6a975-242">Die konfigurierbare Dauer (in Minuten) eines virtuellen Computers, der gelöscht wird, muss das geplante Ereignis beenden möglicherweise genehmigen, bevor das Ereignis automatisch genehmigt wird (Zeitdauer).</span><span class="sxs-lookup"><span data-stu-id="6a975-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="6a975-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="6a975-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="6a975-244">Aktivieren der Ereignisse "Geplante Ereignisse beenden"</span><span class="sxs-lookup"><span data-stu-id="6a975-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="6a975-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="6a975-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="6a975-246">Gibt den Modus eines Upgrades auf virtuelle Computer im Skalierungssatz an.</span><span class="sxs-lookup"><span data-stu-id="6a975-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="6a975-247">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6a975-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a975-248">Automatisch</span><span class="sxs-lookup"><span data-stu-id="6a975-248">Automatic</span></span>
- <span data-ttu-id="6a975-249">Manuell</span><span class="sxs-lookup"><span data-stu-id="6a975-249">Manual</span></span>

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

### <span data-ttu-id="6a975-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="6a975-250">-Zone</span></span>
<span data-ttu-id="6a975-251">Gibt die Zonenliste für den Skalierungssatz für virtuelle Computer an.</span><span class="sxs-lookup"><span data-stu-id="6a975-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6a975-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="6a975-252">-ZoneBalance</span></span>
<span data-ttu-id="6a975-253">Ob die Verteilung von X-Zonen für den Fall, dass ein Zonenausfall vor sich geht, streng sogar für die Verteilung virtueller Computer erzwingen soll.</span><span class="sxs-lookup"><span data-stu-id="6a975-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="6a975-254">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6a975-254">-Confirm</span></span>
<span data-ttu-id="6a975-255">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a975-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a975-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a975-256">-WhatIf</span></span>
<span data-ttu-id="6a975-257">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a975-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a975-258">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a975-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a975-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a975-259">CommonParameters</span></span>
<span data-ttu-id="6a975-260">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a975-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a975-261">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a975-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a975-262">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a975-262">INPUTS</span></span>

### <span data-ttu-id="6a975-263">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a975-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6a975-264">System.String</span><span class="sxs-lookup"><span data-stu-id="6a975-264">System.String</span></span>

### <span data-ttu-id="6a975-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6a975-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6a975-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6a975-266">System.Int32</span></span>

### <span data-ttu-id="6a975-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6a975-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6a975-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="6a975-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="6a975-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6a975-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="6a975-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="6a975-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="6a975-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="6a975-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="6a975-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6a975-272">System.String[]</span></span>

### <span data-ttu-id="6a975-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="6a975-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="6a975-274">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6a975-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6a975-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6a975-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="6a975-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6a975-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="6a975-277">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a975-277">OUTPUTS</span></span>

### <span data-ttu-id="6a975-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6a975-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6a975-279">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6a975-279">NOTES</span></span>

## <span data-ttu-id="6a975-280">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6a975-280">RELATED LINKS</span></span>

[<span data-ttu-id="6a975-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="6a975-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="6a975-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6a975-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="6a975-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a975-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="6a975-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6a975-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="6a975-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6a975-285">New-AzVmss</span></span>](./New-AzVmss.md)
