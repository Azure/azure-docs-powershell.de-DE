---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009323"
---
# <span data-ttu-id="ba159-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ba159-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="ba159-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba159-102">SYNOPSIS</span></span>
<span data-ttu-id="ba159-103">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ba159-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="ba159-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba159-104">SYNTAX</span></span>

### <span data-ttu-id="ba159-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba159-105">DefaultParameterSet (Default)</span></span>
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

### <span data-ttu-id="ba159-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba159-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="ba159-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba159-107">DESCRIPTION</span></span>
<span data-ttu-id="ba159-108">Das Cmdlet **New-AzVmssConfig** erstellt ein konfigurierbares lokales Virtual Manager-Skalierungs Satz Objekt (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ba159-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="ba159-109">Zum Konfigurieren des VMSS-Objekts sind andere Cmdlets erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba159-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="ba159-110">Diese Cmdlets lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba159-110">These cmdlets are:</span></span>
- <span data-ttu-id="ba159-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ba159-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="ba159-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ba159-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="ba159-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba159-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="ba159-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ba159-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="ba159-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba159-115">EXAMPLES</span></span>

### <span data-ttu-id="ba159-116">Beispiel 1: Erstellen eines VMSS-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="ba159-116">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="ba159-117">In diesem Beispiel wird ein VMSS-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="ba159-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="ba159-118">Der erste Befehl verwendet das Cmdlet **New-AzVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ba159-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="ba159-119">Der zweite Befehl verwendet das Cmdlet **New-AzVmss** zum Erstellen eines VMSS, das das im ersten Befehl erstellte VMSS-Konfigurationsobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba159-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="ba159-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ba159-120">Example 2</span></span>

<span data-ttu-id="ba159-121">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ba159-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="ba159-122">automatisch</span><span class="sxs-lookup"><span data-stu-id="ba159-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="ba159-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba159-123">PARAMETERS</span></span>

### <span data-ttu-id="ba159-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="ba159-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="ba159-125">Die Zeitdauer, für die automatische Reparaturen aufgrund einer Zustandsänderung auf VM angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="ba159-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="ba159-126">Die Kulanzzeit beginnt, nachdem die Zustandsänderung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ba159-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="ba159-127">Auf diese Weise können vorzeitige oder unbeabsichtigte Reparaturen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="ba159-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="ba159-128">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba159-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="ba159-129">Die zulässige Mindestfrist beträgt 30 Minuten (PT30M), was auch der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="ba159-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="ba159-130">Die maximal zulässige Kulanzzeit beträgt 90 Minuten (PT90M).</span><span class="sxs-lookup"><span data-stu-id="ba159-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="ba159-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ba159-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="ba159-132">Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ba159-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="ba159-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ba159-133">-BootDiagnostic</span></span>
<span data-ttu-id="ba159-134">Gibt das Start Diagnose Profil für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ba159-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="ba159-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba159-135">-DefaultProfile</span></span>
<span data-ttu-id="ba159-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba159-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba159-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="ba159-137">-DisableAutoRollback</span></span>
<span data-ttu-id="ba159-138">Deaktivieren des automatischen Rollbacks für die Richtlinie für das automatische OS-Upgrade</span><span class="sxs-lookup"><span data-stu-id="ba159-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="ba159-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="ba159-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="ba159-140">Aktiviert automatische Reparaturen auf dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="ba159-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ba159-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="ba159-141">-EnableUltraSSD</span></span>
<span data-ttu-id="ba159-142">Aktiviert eine Funktion, die einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem Skalierungs Satz der virtuellen Maschine besitzt.</span><span class="sxs-lookup"><span data-stu-id="ba159-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="ba159-143">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können nur dann einem VMSS hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ba159-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="ba159-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="ba159-144">-EncryptionAtHost</span></span>
<span data-ttu-id="ba159-145">Mit diesem Parameter wird die Verschlüsselung für alle Datenträger einschließlich des Ressourcen/Temp-Datenträgers am Host selbst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba159-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="ba159-146">Standard: die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba159-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="ba159-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba159-147">-EvictionPolicy</span></span>
<span data-ttu-id="ba159-148">Gibt die Räumungs Richtlinie für die virtuellen Computer in der Skalierungs Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="ba159-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="ba159-149">-Extension</span><span class="sxs-lookup"><span data-stu-id="ba159-149">-Extension</span></span>
<span data-ttu-id="ba159-150">Gibt das Erweiterungs Informationsobjekt für die VMSS an.</span><span class="sxs-lookup"><span data-stu-id="ba159-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="ba159-151">Sie können das **Add-AzVmssExtension-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ba159-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ba159-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="ba159-152">-HealthProbeId</span></span>
<span data-ttu-id="ba159-153">Gibt die ID eines Load Balancer-Prüfpunkts an, der zum Ermitteln des Zustands einer Instanz im Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba159-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="ba159-154">HealthProbeId ist in Form von "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Network/loadBalancers/{loadBalancerName}/Probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="ba159-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="ba159-155">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="ba159-155">-IdentityId</span></span>
<span data-ttu-id="ba159-156">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ba159-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ba159-157">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="ba159-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ba159-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ba159-158">-IdentityType</span></span>
<span data-ttu-id="ba159-159">Gibt den Typ der Identität an, die für den Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba159-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="ba159-160">Der Typ "SystemAssignedUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Gruppe von Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="ba159-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="ba159-161">Der Typ "None" entfernt alle Identitäten aus dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="ba159-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="ba159-162">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba159-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba159-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ba159-163">SystemAssigned</span></span>
- <span data-ttu-id="ba159-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="ba159-164">UserAssigned</span></span>
- <span data-ttu-id="ba159-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="ba159-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="ba159-166">Keine</span><span class="sxs-lookup"><span data-stu-id="ba159-166">None</span></span>

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

### <span data-ttu-id="ba159-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ba159-167">-LicenseType</span></span>
<span data-ttu-id="ba159-168">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="ba159-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ba159-169">-Standort</span><span class="sxs-lookup"><span data-stu-id="ba159-169">-Location</span></span>
<span data-ttu-id="ba159-170">Gibt die Azure-Position an, an der die VMSS erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ba159-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="ba159-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="ba159-171">-MaxPrice</span></span>
<span data-ttu-id="ba159-172">Gibt den Höchstbetrag an, den Sie für einen Spot-VM-VMSS bezahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="ba159-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="ba159-173">Dieser Preis ist in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba159-173">This price is in US Dollars.</span></span> <span data-ttu-id="ba159-174">Dieser Preis wird mit dem aktuellen Spotpreis für die VM-Größe verglichen.</span><span class="sxs-lookup"><span data-stu-id="ba159-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="ba159-175">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von Spot VM/VMSS verglichen, und der Vorgang ist nur erfolgreich, wenn der maxprice größer als der aktuelle Spotpreis ist.</span><span class="sxs-lookup"><span data-stu-id="ba159-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="ba159-176">Der maxprice wird auch für die Räumung eines Spot-VM-VMSS verwendet, wenn der aktuelle Spotpreis nach der Erstellung von VM/VMSS über die maxprice hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="ba159-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="ba159-177">Mögliche Werte sind: beliebiger Dezimalwert größer als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ba159-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="ba159-178">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="ba159-178">Example: 0.01538.</span></span>  <span data-ttu-id="ba159-179">-1 gibt an, dass der Spot VM/VMSS aus Preisgründen nicht entfernt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="ba159-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="ba159-180">Außerdem ist der standardmäßige Höchstpreis-1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ba159-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="ba159-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba159-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="ba159-182">Gibt das Netzwerkprofil Objekt an, das die Netzwerkeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="ba159-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="ba159-183">Sie können das **Add-AzVmssNetworkInterfaceConfiguration-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ba159-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ba159-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="ba159-184">-OsProfile</span></span>
<span data-ttu-id="ba159-185">Gibt das Betriebssystem-Profilobjekt an, das die Betriebssystemeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="ba159-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="ba159-186">Sie können das Cmdlet " **Satz-AzVmssOsProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="ba159-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ba159-187">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="ba159-187">-Overprovision</span></span>
<span data-ttu-id="ba159-188">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba159-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="ba159-189">-Planname</span><span class="sxs-lookup"><span data-stu-id="ba159-189">-PlanName</span></span>
<span data-ttu-id="ba159-190">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="ba159-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="ba159-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ba159-191">-PlanProduct</span></span>
<span data-ttu-id="ba159-192">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="ba159-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="ba159-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="ba159-193">-PlanPromotionCode</span></span>
<span data-ttu-id="ba159-194">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="ba159-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="ba159-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ba159-195">-PlanPublisher</span></span>
<span data-ttu-id="ba159-196">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="ba159-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="ba159-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="ba159-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="ba159-198">Anzahl der fehlerdomänen für jede Placement-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ba159-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="ba159-199">-Priorität</span><span class="sxs-lookup"><span data-stu-id="ba159-199">-Priority</span></span>
<span data-ttu-id="ba159-200">Die Priorität für das virtuelle machien in der Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ba159-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="ba159-201">Nur Unterstützte Werte sind "Normal", "Spot" und "Low".</span><span class="sxs-lookup"><span data-stu-id="ba159-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="ba159-202">"Normal" ist für normalen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ba159-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="ba159-203">"Spot" ist für Spot Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="ba159-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="ba159-204">"Low" ist auch für Spot Virtual Machine, wird aber durch "Spot" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ba159-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="ba159-205">Bitte verwenden Sie "Spot" anstelle von "Low".</span><span class="sxs-lookup"><span data-stu-id="ba159-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="ba159-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ba159-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="ba159-207">Die Ressourcen-ID der für diesen Skalierungs Satz zu verwendenden Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ba159-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="ba159-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ba159-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="ba159-209">Gibt die Richtlinie zum parallelen Upgrade an.</span><span class="sxs-lookup"><span data-stu-id="ba159-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="ba159-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="ba159-210">-ScaleInPolicy</span></span>
<span data-ttu-id="ba159-211">Die Regeln, die beim Skalieren in einem Skalierungs Satz einer virtuellen Maschine befolgt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ba159-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="ba159-212">Mögliche Werte sind: "Standard", "OldestVM" und "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="ba159-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="ba159-213">"Standard" Wenn der Skalierungs Satz einer virtuellen Maschine skaliert wird, wird der Skalierungs Satz zunächst zonenübergreifend ausbalanciert, wenn es sich um einen Zonal-Skalierungs Satz handelt.</span><span class="sxs-lookup"><span data-stu-id="ba159-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="ba159-214">In diesem Fall werden die fehlerdomänen so weit wie möglich ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="ba159-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="ba159-215">Innerhalb jeder fehlerdomäne sind die für die Entfernung ausgewählten virtuellen Computer die neuesten, die nicht vor dem Skalieren geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="ba159-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="ba159-216">"OldestVM" Wenn ein Skalierungs Satz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ba159-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ba159-217">Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="ba159-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ba159-218">Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ba159-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="ba159-219">"NewestVM" Wenn ein Skalierungs Satz für virtuelle Maschinen skaliert wird, werden die neuesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ba159-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ba159-220">Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="ba159-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ba159-221">In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ba159-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="ba159-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ba159-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="ba159-223">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="ba159-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="ba159-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="ba159-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="ba159-225">Gibt an, dass die Erweiterungen nicht auf den zusätzlichen überlegten VMS ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ba159-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="ba159-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ba159-226">-SkuCapacity</span></span>
<span data-ttu-id="ba159-227">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="ba159-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="ba159-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ba159-228">-SkuName</span></span>
<span data-ttu-id="ba159-229">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="ba159-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="ba159-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ba159-230">-SkuTier</span></span>
<span data-ttu-id="ba159-231">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="ba159-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="ba159-232">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba159-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba159-233">Standard</span><span class="sxs-lookup"><span data-stu-id="ba159-233">Standard</span></span>
- <span data-ttu-id="ba159-234">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="ba159-234">Basic</span></span>

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

### <span data-ttu-id="ba159-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="ba159-235">-StorageProfile</span></span>
<span data-ttu-id="ba159-236">Gibt das Speicherprofil Objekt an, das die Datenträgereigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="ba159-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="ba159-237">Sie können das Cmdlet " **Satz-AzVmssStorageProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="ba159-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ba159-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="ba159-238">-Tag</span></span>
<span data-ttu-id="ba159-239">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="ba159-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ba159-240">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="ba159-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ba159-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ba159-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="ba159-242">Konfigurierbare Zeitdauer (in Minuten) ein gelöschter virtueller Computer muss möglicherweise das Terminate scheduled-Ereignis genehmigen, bevor das Ereignis automatisch genehmigt wird (Timeout).</span><span class="sxs-lookup"><span data-stu-id="ba159-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="ba159-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="ba159-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="ba159-244">Aktivieren der terminierten Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ba159-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="ba159-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ba159-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="ba159-246">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba159-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="ba159-247">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba159-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba159-248">Automatisch</span><span class="sxs-lookup"><span data-stu-id="ba159-248">Automatic</span></span>
- <span data-ttu-id="ba159-249">Manuell</span><span class="sxs-lookup"><span data-stu-id="ba159-249">Manual</span></span>

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

### <span data-ttu-id="ba159-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="ba159-250">-Zone</span></span>
<span data-ttu-id="ba159-251">Gibt die Zonenliste für den Skalierungs Satz der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="ba159-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ba159-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="ba159-252">-ZoneBalance</span></span>
<span data-ttu-id="ba159-253">Ob eine strikte selbst Verteilung der virtuellen Computer über x-Zonen erzwungen werden soll, wenn ein Zonen Ausfall vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ba159-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="ba159-254">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba159-254">-Confirm</span></span>
<span data-ttu-id="ba159-255">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba159-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba159-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba159-256">-WhatIf</span></span>
<span data-ttu-id="ba159-257">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba159-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba159-258">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba159-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba159-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba159-259">CommonParameters</span></span>
<span data-ttu-id="ba159-260">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba159-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba159-261">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba159-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba159-262">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba159-262">INPUTS</span></span>

### <span data-ttu-id="ba159-263">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ba159-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ba159-264">System. String</span><span class="sxs-lookup"><span data-stu-id="ba159-264">System.String</span></span>

### <span data-ttu-id="ba159-265">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ba159-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ba159-266">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ba159-266">System.Int32</span></span>

### <span data-ttu-id="ba159-267">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ba159-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ba159-268">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="ba159-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="ba159-269">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ba159-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="ba159-270">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="ba159-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="ba159-271">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="ba159-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="ba159-272">System. String []</span><span class="sxs-lookup"><span data-stu-id="ba159-272">System.String[]</span></span>

### <span data-ttu-id="ba159-273">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ba159-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="ba159-274">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="ba159-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ba159-275">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ba159-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="ba159-276">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ba159-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ba159-277">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba159-277">OUTPUTS</span></span>

### <span data-ttu-id="ba159-278">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ba159-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ba159-279">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba159-279">NOTES</span></span>

## <span data-ttu-id="ba159-280">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba159-280">RELATED LINKS</span></span>

[<span data-ttu-id="ba159-281">Satz-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ba159-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="ba159-282">Satz-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ba159-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="ba159-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba159-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="ba159-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ba159-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="ba159-285">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba159-285">New-AzVmss</span></span>](./New-AzVmss.md)
