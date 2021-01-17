---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470814"
---
# <span data-ttu-id="052f0-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="052f0-101">Update-AzVmss</span></span>

## <span data-ttu-id="052f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="052f0-102">SYNOPSIS</span></span>
<span data-ttu-id="052f0-103">Aktualisiert den Zustand eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="052f0-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="052f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="052f0-104">SYNTAX</span></span>

### <span data-ttu-id="052f0-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="052f0-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052f0-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="052f0-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="052f0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="052f0-107">DESCRIPTION</span></span>
<span data-ttu-id="052f0-108">Das **Cmdlet "Update-AzVmss"** aktualisiert den Zustand eines Virtual Machine Scale Set (VMSS) auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="052f0-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="052f0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="052f0-109">EXAMPLES</span></span>

### <span data-ttu-id="052f0-110">Beispiel 1: Aktualisieren des Zustands eines VMSS auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="052f0-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="052f0-111">Mit diesem Befehl wird der Zustand der VMSS namens VMSS001 aktualisiert, die der Ressourcengruppe "Group001" zum Zustand eines lokalen VMSS-Objekts ($LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="052f0-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="052f0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="052f0-112">PARAMETERS</span></span>

### <span data-ttu-id="052f0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="052f0-113">-AsJob</span></span>
<span data-ttu-id="052f0-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="052f0-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="052f0-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="052f0-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="052f0-116">Legt fest, ob Betriebssystemupgrade automatisch auf Skalierungssatzinstanzen fortlaufend angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="052f0-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="052f0-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="052f0-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="052f0-118">Die Zeit, für die automatische Reparaturen aufgrund einer Zustandsänderung auf der VM angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="052f0-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="052f0-119">Die Nachfrist beginnt nach Abschluss der Zustandsänderung.</span><span class="sxs-lookup"><span data-stu-id="052f0-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="052f0-120">Dadurch können vorzeitig oder versehentliche Reparaturen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="052f0-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="052f0-121">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="052f0-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="052f0-122">Die zulässige Nachfrist beträgt 30 Minuten (PT30M), was auch der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="052f0-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="052f0-123">Die maximal zulässige Nachfrist beträgt 90 Minuten (PT90M).</span><span class="sxs-lookup"><span data-stu-id="052f0-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="052f0-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="052f0-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="052f0-125">Ob die Startdiagnose für den Skalierungssatz des virtuellen Computers aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="052f0-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="052f0-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="052f0-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="052f0-127">URI des Speicherkontos, das zum Platzieren der Konsolenausgabe und des Screenshots verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="052f0-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="052f0-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="052f0-128">-CustomData</span></span>
<span data-ttu-id="052f0-129">Gibt eine base-64-codierte Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="052f0-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="052f0-130">Dies wird in ein Binärarray decodiert, das als Datei auf dem virtuellen Computer gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="052f0-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="052f0-131">Die maximale Länge des Binärarrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="052f0-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="052f0-132">Informationen zur Verwendung von cloud-init für Ihre VM finden Sie unter "Verwenden von [cloud-init zum Anpassen einer Linux-VM während der Erstellung".](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="052f0-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="052f0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052f0-133">-DefaultProfile</span></span>
<span data-ttu-id="052f0-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="052f0-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="052f0-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="052f0-135">-DisableAutoRollback</span></span>
<span data-ttu-id="052f0-136">Deaktivieren des automatischen Rollbacks für die Upgraderichtlinie für das automatische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="052f0-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="052f0-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="052f0-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="052f0-138">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung für Linux OS deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="052f0-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="052f0-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="052f0-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="052f0-140">Aktivieren oder deaktivieren Sie automatische Reparaturen für den Skalierungssatz des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="052f0-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="052f0-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="052f0-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="052f0-142">Gibt an, ob die virtuellen Computer von Windows in VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="052f0-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="052f0-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="052f0-143">-EncryptionAtHost</span></span>
<span data-ttu-id="052f0-144">Dieser Parameter kann vom Benutzer in der Anforderung verwendet werden, um die Hostverschlüsselung für den Skalierungssatz des virtuellen Computers zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="052f0-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="052f0-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="052f0-145">-IdentityId</span></span>
<span data-ttu-id="052f0-146">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungssatz für den virtuellen Computer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="052f0-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="052f0-147">Die Benutzeridentitätsverweise werden ARM Ressourcen-ID im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' angegeben.</span><span class="sxs-lookup"><span data-stu-id="052f0-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="052f0-148">-IdentityType</span></span>
<span data-ttu-id="052f0-149">Gibt den Identitätstyp an, der für den Skalierungssatz des virtuellen Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="052f0-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="052f0-150">Der Typ "SystemAssignedUserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Gruppe von vom Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="052f0-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="052f0-151">Mit dem Typ "None" werden alle Identitäten aus dem Skalierungssatz des virtuellen Computers entfernt.</span><span class="sxs-lookup"><span data-stu-id="052f0-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="052f0-152">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="052f0-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="052f0-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="052f0-153">SystemAssigned</span></span>
- <span data-ttu-id="052f0-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="052f0-154">UserAssigned</span></span>
- <span data-ttu-id="052f0-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="052f0-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="052f0-156">Keine</span><span class="sxs-lookup"><span data-stu-id="052f0-156">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="052f0-157">-ImageReferenceId</span></span>
<span data-ttu-id="052f0-158">Gibt die Bildverweis-ID an.</span><span class="sxs-lookup"><span data-stu-id="052f0-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="052f0-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="052f0-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="052f0-160">Gibt den Typ des Virtual Machine Image (VMImage)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="052f0-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="052f0-161">Um ein Bildangebot zu erhalten, verwenden Sie das Get-AzVMImageOffer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052f0-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="052f0-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="052f0-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="052f0-163">Gibt den Namen eines Herausgebers eines VMImages an.</span><span class="sxs-lookup"><span data-stu-id="052f0-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="052f0-164">Verwenden Sie zum Abrufen eines Herausgebers das Get-AzVMImagePublisher Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052f0-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="052f0-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="052f0-165">-ImageReferenceSku</span></span>
<span data-ttu-id="052f0-166">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="052f0-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="052f0-167">Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052f0-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="052f0-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="052f0-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="052f0-169">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="052f0-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="052f0-170">Wenn Sie die neueste Version verwenden möchten, geben Sie den Wert "Neueste Version" anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="052f0-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="052f0-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="052f0-171">-ImageUri</span></span>
<span data-ttu-id="052f0-172">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="052f0-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="052f0-173">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerabbilds.</span><span class="sxs-lookup"><span data-stu-id="052f0-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="052f0-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="052f0-174">-LicenseType</span></span>
<span data-ttu-id="052f0-175">Geben Sie den Lizenztyp an, mit dem Sie Ihr eigenes Lizenzszenario erstellen können.</span><span class="sxs-lookup"><span data-stu-id="052f0-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="052f0-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="052f0-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="052f0-177">Gibt den Speicherkontotyp für verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="052f0-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="052f0-178">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="052f0-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="052f0-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="052f0-179">StandardLRS</span></span>
- <span data-ttu-id="052f0-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="052f0-180">PremiumLRS</span></span>

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

### <span data-ttu-id="052f0-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="052f0-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="052f0-182">Der maximale Prozentwert der gesamten Instanzen virtueller Computer, die gleichzeitig durch das Rollup in einem Batch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="052f0-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="052f0-183">Da dies eine maximale Anzahl fehlerhafter Instanzen in vorherigen oder zukünftigen Batches ist, kann dies dazu führen, dass der Prozentsatz der Instanzen in einem Batch abgenommen wird, um eine höhere Zuverlässigkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="052f0-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="052f0-184">Wenn der Wert nicht angegeben wird, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="052f0-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="052f0-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="052f0-185">-MaxPrice</span></span>
<span data-ttu-id="052f0-186">Gibt den maximal zulässigen Preis für eine VM/VMSS mit niedriger Priorität an.</span><span class="sxs-lookup"><span data-stu-id="052f0-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="052f0-187">Dieser Preis wird in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="052f0-187">This price is in US Dollars.</span></span> <span data-ttu-id="052f0-188">Dieser Preis wird mit dem aktuellen Preis mit niedriger Priorität für die Größe der VM verglichen.</span><span class="sxs-lookup"><span data-stu-id="052f0-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="052f0-189">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM/VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der "maxPrice" größer als der aktuelle Preis mit niedriger Priorität ist.</span><span class="sxs-lookup"><span data-stu-id="052f0-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="052f0-190">Der "maxPrice" wird auch zum Entfernung einer VM/VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis mit niedriger Priorität nach der Erstellung von VM/VMSS über den maxPrice hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="052f0-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="052f0-191">Mögliche Werte sind: beliebige Dezimalwerte größer als Null.</span><span class="sxs-lookup"><span data-stu-id="052f0-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="052f0-192">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="052f0-192">Example: 0.01538.</span></span>  <span data-ttu-id="052f0-193">-1 gibt an, dass die VM/VMSS mit niedriger Priorität aus Preisgründen nicht entfernt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="052f0-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="052f0-194">Außerdem beträgt der standardmäßige maximaler Preis -1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="052f0-194">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="052f0-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="052f0-196">Der maximale Prozentsatz der gesamten Instanzen des virtuellen Computers in dem Skalierungssatz, der gleichzeitig fehlerhaft sein kann, entweder als Ergebnis des Upgrades oder durch Die Integritätsprüfungen des virtuellen Computers in einem fehlerhaften Zustand vor dem Abbruch des Rollups.</span><span class="sxs-lookup"><span data-stu-id="052f0-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="052f0-197">Diese Einschränkung wird vor dem Starten eines Batches überprüft.</span><span class="sxs-lookup"><span data-stu-id="052f0-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="052f0-198">Wenn der Wert nicht angegeben wird, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="052f0-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="052f0-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="052f0-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="052f0-200">Der maximale Prozentsatz der aktualisierten Instanzen virtueller Computer, für die ein fehlerhafter Zustand gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="052f0-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="052f0-201">Diese Überprüfung wird ausgeführt, nachdem für jeden Batch ein Upgrade ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="052f0-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="052f0-202">Wenn dieser Prozentsatz jemals überschritten wird, wird das fortlaufende Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="052f0-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="052f0-203">Wenn der Wert nicht angegeben wird, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="052f0-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="052f0-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="052f0-204">-OsDiskCaching</span></span>
<span data-ttu-id="052f0-205">Gibt den Cachemodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="052f0-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="052f0-206">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="052f0-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="052f0-207">Keine</span><span class="sxs-lookup"><span data-stu-id="052f0-207">None</span></span>
- <span data-ttu-id="052f0-208">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="052f0-208">ReadOnly</span></span>
- <span data-ttu-id="052f0-209">ReadWrite Der Standardwert ist "ReadWrite".</span><span class="sxs-lookup"><span data-stu-id="052f0-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="052f0-210">Wenn Sie den Zwischenspeicherungswert ändern, wird der virtuelle Computer vom Cmdlet neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="052f0-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="052f0-211">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="052f0-211">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="052f0-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="052f0-213">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="052f0-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="052f0-214">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="052f0-214">-Overprovision</span></span>
<span data-ttu-id="052f0-215">Gibt an, ob das Cmdlet die VMSS übergibt.</span><span class="sxs-lookup"><span data-stu-id="052f0-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="052f0-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="052f0-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="052f0-217">Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.</span><span class="sxs-lookup"><span data-stu-id="052f0-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="052f0-218">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="052f0-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="052f0-219">Der Standardwert ist 0 Sekunden (PT0S).</span><span class="sxs-lookup"><span data-stu-id="052f0-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="052f0-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="052f0-220">-PlanName</span></span>
<span data-ttu-id="052f0-221">Gibt den Plannamen an.</span><span class="sxs-lookup"><span data-stu-id="052f0-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="052f0-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="052f0-222">-PlanProduct</span></span>
<span data-ttu-id="052f0-223">Gibt das Planprodukt an.</span><span class="sxs-lookup"><span data-stu-id="052f0-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="052f0-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="052f0-224">-PlanPromotionCode</span></span>
<span data-ttu-id="052f0-225">Gibt den Promotionscode für den Plan an.</span><span class="sxs-lookup"><span data-stu-id="052f0-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="052f0-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="052f0-226">-PlanPublisher</span></span>
<span data-ttu-id="052f0-227">Gibt den Planherausgeber an.</span><span class="sxs-lookup"><span data-stu-id="052f0-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="052f0-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="052f0-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="052f0-229">Gibt an, ob der Agent für virtuelle Computer auf den virtuellen Computern von Windows auf der VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="052f0-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="052f0-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="052f0-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="052f0-231">Die Ressourcen-ID der Näherungsplatzierungsgruppe, die für diesen Skalierungssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="052f0-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="052f0-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="052f0-232">-ResourceGroupName</span></span>
<span data-ttu-id="052f0-233">Gibt den Namen der Ressourcengruppe an, zu der VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="052f0-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="052f0-234">-ScaleInPolicy</span></span>
<span data-ttu-id="052f0-235">Die Regeln, die beim Skalieren in einem Skalierungssatz für einen virtuellen Computer zu beachten sind.</span><span class="sxs-lookup"><span data-stu-id="052f0-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="052f0-236">Mögliche Werte: "Default", "OldestVM" und "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="052f0-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="052f0-237">Wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen, wenn es sich um einen standardmäßigen Skalierungssatz handelt.</span><span class="sxs-lookup"><span data-stu-id="052f0-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="052f0-238">Anschließend wird sie so weit wie möglich über Fehlerdomänen hinweg ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="052f0-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="052f0-239">Innerhalb jeder Fault Domain sind die zum Entfernen ausgewählten virtuellen Computer die neuesten Computer, die nicht vor "scale-in" geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="052f0-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="052f0-240">"OldestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor "scale-in" geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="052f0-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="052f0-241">Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="052f0-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="052f0-242">Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="052f0-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="052f0-243">"NewestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die neuesten virtuellen Computer, die nicht vor scale-in geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="052f0-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="052f0-244">Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="052f0-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="052f0-245">In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="052f0-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="052f0-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="052f0-247">Gibt die einzelne Platzierungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="052f0-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="052f0-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="052f0-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="052f0-249">Gibt an, dass die Erweiterungen nicht für die zusätzlichen überprovisionierten VMs ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="052f0-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="052f0-250">-Sku1</span><span class="sxs-lookup"><span data-stu-id="052f0-250">-SkuCapacity</span></span>
<span data-ttu-id="052f0-251">Gibt die Anzahl der Instanzen in der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="052f0-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="052f0-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="052f0-252">-SkuName</span></span>
<span data-ttu-id="052f0-253">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="052f0-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="052f0-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="052f0-254">-SkuTier</span></span>
<span data-ttu-id="052f0-255">Gibt die Stufe von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="052f0-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="052f0-256">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="052f0-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="052f0-257">Standard</span><span class="sxs-lookup"><span data-stu-id="052f0-257">Standard</span></span>
- <span data-ttu-id="052f0-258">Standard</span><span class="sxs-lookup"><span data-stu-id="052f0-258">Basic</span></span>

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

### <span data-ttu-id="052f0-259">-Tag</span><span class="sxs-lookup"><span data-stu-id="052f0-259">-Tag</span></span>
<span data-ttu-id="052f0-260">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="052f0-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="052f0-261">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="052f0-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="052f0-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="052f0-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="052f0-263">Eine konfigurierbare Dauer (in Minuten) für einen gelöschten virtuellen Computer muss potenziell das Ereignis "Terminiertes Ereignis beenden" genehmigen, bevor das Ereignis automatisch genehmigt (Timed out) wird.</span><span class="sxs-lookup"><span data-stu-id="052f0-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="052f0-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="052f0-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="052f0-265">Gibt an, ob das Ereignis "Termingerecht beenden" aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="052f0-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-266">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="052f0-266">-TimeZone</span></span>
<span data-ttu-id="052f0-267">Gibt die Zeitzone für das Windows-Betriebssystem an.</span><span class="sxs-lookup"><span data-stu-id="052f0-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="052f0-268">z. B. \" Pacific Standard \" Time.</span><span class="sxs-lookup"><span data-stu-id="052f0-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="052f0-269">Mögliche Werte können als [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) zeitzonen verwendet werden, die von ["TimeZoneInfo.GetSystemTimeZones" zurückgegeben werden.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="052f0-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="052f0-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="052f0-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="052f0-271">Das Kennzeichen, mit dem eine Funktion aktiviert oder deaktiviert wird, um eine oder mehrere verwaltete Datenträger mit UltraSSD_LRS Speicherkontotyp auf dem Skalierungssatz des virtuellen Computers zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="052f0-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="052f0-272">Verwaltete Datenträger mit speicherkontotyp UltraSSD_LRS können einem VMSS nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="052f0-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="052f0-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="052f0-274">Der Modus für ein Upgrade auf virtuelle Computer wurde im Skalierungssatz angegeben.</span><span class="sxs-lookup"><span data-stu-id="052f0-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="052f0-275">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="052f0-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="052f0-276">Automatisch</span><span class="sxs-lookup"><span data-stu-id="052f0-276">Automatic</span></span>
- <span data-ttu-id="052f0-277">Manuell</span><span class="sxs-lookup"><span data-stu-id="052f0-277">Manual</span></span>
- <span data-ttu-id="052f0-278">Rollen</span><span class="sxs-lookup"><span data-stu-id="052f0-278">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="052f0-279">-VhdContainer</span></span>
<span data-ttu-id="052f0-280">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für die VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="052f0-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="052f0-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="052f0-282">Gibt ein lokales VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="052f0-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="052f0-283">Verwenden Sie zum Abrufen eines VMSS-Objekts das Get-AzVmss-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052f0-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="052f0-284">Dieses Objekt des virtuellen Computers enthält den aktualisierten Zustand für die VMSS.</span><span class="sxs-lookup"><span data-stu-id="052f0-284">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="052f0-285">-VMScaleSetName</span></span>
<span data-ttu-id="052f0-286">Gibt den Namen der VMSS an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="052f0-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052f0-287">-Confirm</span><span class="sxs-lookup"><span data-stu-id="052f0-287">-Confirm</span></span>
<span data-ttu-id="052f0-288">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="052f0-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="052f0-289">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="052f0-289">-WhatIf</span></span>
<span data-ttu-id="052f0-290">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="052f0-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="052f0-291">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="052f0-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="052f0-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052f0-292">CommonParameters</span></span>
<span data-ttu-id="052f0-293">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="052f0-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052f0-294">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="052f0-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052f0-295">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="052f0-295">INPUTS</span></span>

### <span data-ttu-id="052f0-296">System.String</span><span class="sxs-lookup"><span data-stu-id="052f0-296">System.String</span></span>

### <span data-ttu-id="052f0-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="052f0-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="052f0-298">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="052f0-298">System.Boolean</span></span>

## <span data-ttu-id="052f0-299">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="052f0-299">OUTPUTS</span></span>

### <span data-ttu-id="052f0-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="052f0-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="052f0-301">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="052f0-301">NOTES</span></span>

## <span data-ttu-id="052f0-302">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="052f0-302">RELATED LINKS</span></span>

[<span data-ttu-id="052f0-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="052f0-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="052f0-304">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="052f0-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="052f0-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="052f0-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="052f0-306">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="052f0-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="052f0-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="052f0-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="052f0-308">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="052f0-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="052f0-309">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="052f0-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


