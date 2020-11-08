---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: bf8fa8c4b7d1d08cdb6d0c2c348f5c97a2788a4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004793"
---
# <span data-ttu-id="93987-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="93987-101">Update-AzVmss</span></span>

## <span data-ttu-id="93987-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93987-102">SYNOPSIS</span></span>
<span data-ttu-id="93987-103">Aktualisiert den Zustand eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="93987-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="93987-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93987-104">SYNTAX</span></span>

### <span data-ttu-id="93987-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="93987-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93987-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="93987-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93987-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93987-107">DESCRIPTION</span></span>
<span data-ttu-id="93987-108">Das Cmdlet **Update-AzVmss** aktualisiert den Zustand eines virtuellen Computer-Skalierungs Satzes (VMSS) auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="93987-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="93987-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93987-109">EXAMPLES</span></span>

### <span data-ttu-id="93987-110">Beispiel 1: Aktualisieren Sie den Zustand eines VMSS auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="93987-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="93987-111">Dieser Befehl aktualisiert den Zustand des VMSS mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört, in den Zustand eines lokalen VMSS-Objekts $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="93987-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="93987-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="93987-112">PARAMETERS</span></span>

### <span data-ttu-id="93987-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93987-113">-AsJob</span></span>
<span data-ttu-id="93987-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="93987-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="93987-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="93987-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="93987-116">Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="93987-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="93987-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="93987-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="93987-118">Die Zeitdauer, für die automatische Reparaturen aufgrund einer Zustandsänderung auf VM angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="93987-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="93987-119">Die Kulanzzeit beginnt, nachdem die Zustandsänderung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="93987-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="93987-120">Auf diese Weise können vorzeitige oder unbeabsichtigte Reparaturen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="93987-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="93987-121">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="93987-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="93987-122">Der Standardwert ist 5 Minuten (PT5M).</span><span class="sxs-lookup"><span data-stu-id="93987-122">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="93987-123">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="93987-123">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="93987-124">Der Prozentsatz (Kapazität des scaleset) virtueller Computer, der gleichzeitig repariert wird.</span><span class="sxs-lookup"><span data-stu-id="93987-124">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="93987-125">Der Standardwert ist 20%.</span><span class="sxs-lookup"><span data-stu-id="93987-125">The default value is 20%.</span></span>

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

### <span data-ttu-id="93987-126">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="93987-126">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="93987-127">Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="93987-127">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="93987-128">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="93987-128">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="93987-129">Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="93987-129">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="93987-130">-CustomData</span><span class="sxs-lookup"><span data-stu-id="93987-130">-CustomData</span></span>
<span data-ttu-id="93987-131">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="93987-131">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="93987-132">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="93987-132">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="93987-133">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="93987-133">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="93987-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93987-134">-DefaultProfile</span></span>
<span data-ttu-id="93987-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93987-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93987-136">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="93987-136">-DisableAutoRollback</span></span>
<span data-ttu-id="93987-137">Deaktivieren des automatischen Rollbacks für die Richtlinie für das automatische OS-Upgrade</span><span class="sxs-lookup"><span data-stu-id="93987-137">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="93987-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="93987-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="93987-139">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung für Linux-Betriebssystem deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="93987-139">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="93987-140">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="93987-140">-EnableAutomaticRepair</span></span>
<span data-ttu-id="93987-141">Aktivieren oder deaktivieren Sie automatische Reparaturen auf dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="93987-141">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="93987-142">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="93987-142">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="93987-143">Gibt an, ob die Windows-virtuellen Computer im VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="93987-143">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="93987-144">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="93987-144">-IdentityId</span></span>
<span data-ttu-id="93987-145">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="93987-145">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="93987-146">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="93987-146">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="93987-147">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="93987-147">-IdentityType</span></span>
<span data-ttu-id="93987-148">Gibt den Typ der Identität an, die für den Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93987-148">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="93987-149">Der Typ "SystemAssignedUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Gruppe von Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="93987-149">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="93987-150">Der Typ "None" entfernt alle Identitäten aus dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="93987-150">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="93987-151">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93987-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93987-152">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="93987-152">SystemAssigned</span></span>
- <span data-ttu-id="93987-153">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="93987-153">UserAssigned</span></span>
- <span data-ttu-id="93987-154">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="93987-154">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="93987-155">Keine</span><span class="sxs-lookup"><span data-stu-id="93987-155">None</span></span>

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

### <span data-ttu-id="93987-156">-Imagereference-Nr</span><span class="sxs-lookup"><span data-stu-id="93987-156">-ImageReferenceId</span></span>
<span data-ttu-id="93987-157">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="93987-157">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="93987-158">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="93987-158">-ImageReferenceOffer</span></span>
<span data-ttu-id="93987-159">Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="93987-159">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="93987-160">Verwenden Sie das Get-AzVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93987-160">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="93987-161">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="93987-161">-ImageReferencePublisher</span></span>
<span data-ttu-id="93987-162">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="93987-162">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="93987-163">Verwenden Sie zum Abrufen eines Verlegers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93987-163">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="93987-164">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="93987-164">-ImageReferenceSku</span></span>
<span data-ttu-id="93987-165">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="93987-165">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="93987-166">Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93987-166">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="93987-167">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="93987-167">-ImageReferenceVersion</span></span>
<span data-ttu-id="93987-168">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="93987-168">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="93987-169">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="93987-169">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="93987-170">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="93987-170">-ImageUri</span></span>
<span data-ttu-id="93987-171">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="93987-171">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="93987-172">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.</span><span class="sxs-lookup"><span data-stu-id="93987-172">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="93987-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="93987-173">-LicenseType</span></span>
<span data-ttu-id="93987-174">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="93987-174">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="93987-175">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="93987-175">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="93987-176">Gibt den Speicher Kontotyp für verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="93987-176">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="93987-177">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93987-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93987-178">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="93987-178">StandardLRS</span></span>
- <span data-ttu-id="93987-179">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="93987-179">PremiumLRS</span></span>

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

### <span data-ttu-id="93987-180">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="93987-180">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="93987-181">Der maximale Prozentsatz der virtuellen Computer Instanzen, die vom parallelen Upgrade in einem Batch gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="93987-181">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="93987-182">Da dies ein Maximum ist, können ungesunde Instanzen in früheren oder zukünftigen Batches dazu führen, dass der Prozentsatz der Instanzen in einem Batch verringert wird, um eine höhere Zuverlässigkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="93987-182">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="93987-183">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="93987-183">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="93987-184">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="93987-184">-MaxPrice</span></span>
<span data-ttu-id="93987-185">Gibt den Höchstpreis an, den Sie für eine VM-VMSS mit niedriger Priorität bezahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="93987-185">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="93987-186">Dieser Preis ist in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="93987-186">This price is in US Dollars.</span></span> <span data-ttu-id="93987-187">Dieser Preis wird mit dem aktuellen Preis für niedrige Priorität für die VM-Größe verglichen.</span><span class="sxs-lookup"><span data-stu-id="93987-187">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="93987-188">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM-VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der maxprice größer als der aktuelle Preis für niedrige Priorität ist.</span><span class="sxs-lookup"><span data-stu-id="93987-188">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="93987-189">Die maxprice wird auch zum Entfernen einer VM-VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis für niedrige Priorität über die maxprice nach der Erstellung von VM/VMSS hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="93987-189">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="93987-190">Mögliche Werte sind: beliebiger Dezimalwert größer als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="93987-190">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="93987-191">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="93987-191">Example: 0.01538.</span></span>  <span data-ttu-id="93987-192">-1 gibt an, dass die VM-VMSS mit niedriger Priorität aus Preisgründen nicht vertrieben werden sollte.</span><span class="sxs-lookup"><span data-stu-id="93987-192">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="93987-193">Außerdem ist der standardmäßige Höchstpreis-1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="93987-193">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="93987-194">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="93987-194">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="93987-195">Der maximale Prozentsatz der gesamten virtuellen Computer Instanzen im Skalierungs Satz, die gleichzeitig fehlerhaft sein können, entweder als Ergebnis eines Upgrades oder durch die Integritätsprüfung des virtuellen Computers in einem ungesunden Zustand, bevor das parallele Upgrade abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="93987-195">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="93987-196">Diese Einschränkung wird vor dem Starten eines Batches überprüft.</span><span class="sxs-lookup"><span data-stu-id="93987-196">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="93987-197">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="93987-197">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="93987-198">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="93987-198">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="93987-199">Der maximale Prozentsatz der aktualisierten virtuellen Computer Instanzen, die sich in einem fehlerhaften Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="93987-199">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="93987-200">Diese Überprüfung erfolgt, nachdem jeder Batch aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="93987-200">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="93987-201">Wenn dieser Prozentsatz jemals überschritten wird, wird das Rolling-Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="93987-201">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="93987-202">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="93987-202">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="93987-203">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="93987-203">-OsDiskCaching</span></span>
<span data-ttu-id="93987-204">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="93987-204">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="93987-205">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93987-205">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93987-206">Keine</span><span class="sxs-lookup"><span data-stu-id="93987-206">None</span></span>
- <span data-ttu-id="93987-207">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="93987-207">ReadOnly</span></span>
- <span data-ttu-id="93987-208">ReadWrite der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="93987-208">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="93987-209">Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="93987-209">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="93987-210">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="93987-210">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="93987-211">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="93987-211">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="93987-212">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="93987-212">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="93987-213">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="93987-213">-Overprovision</span></span>
<span data-ttu-id="93987-214">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="93987-214">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="93987-215">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="93987-215">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="93987-216">Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.</span><span class="sxs-lookup"><span data-stu-id="93987-216">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="93987-217">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="93987-217">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="93987-218">Der Standardwert ist 0 Sekunden (PT0S).</span><span class="sxs-lookup"><span data-stu-id="93987-218">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="93987-219">-Planname</span><span class="sxs-lookup"><span data-stu-id="93987-219">-PlanName</span></span>
<span data-ttu-id="93987-220">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="93987-220">Specifies the plan name.</span></span>

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

### <span data-ttu-id="93987-221">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="93987-221">-PlanProduct</span></span>
<span data-ttu-id="93987-222">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="93987-222">Specifies the plan product.</span></span>

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

### <span data-ttu-id="93987-223">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="93987-223">-PlanPromotionCode</span></span>
<span data-ttu-id="93987-224">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="93987-224">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="93987-225">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="93987-225">-PlanPublisher</span></span>
<span data-ttu-id="93987-226">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="93987-226">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="93987-227">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="93987-227">-ProvisionVMAgent</span></span>
<span data-ttu-id="93987-228">Gibt an, ob der Virtual Machine-Agent auf den virtuellen Windows-Computern im VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="93987-228">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="93987-229">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="93987-229">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="93987-230">Die Ressourcen-ID der für diesen Skalierungs Satz zu verwendenden Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="93987-230">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="93987-231">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93987-231">-ResourceGroupName</span></span>
<span data-ttu-id="93987-232">Gibt den Namen der Ressourcengruppe an, zu der der VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="93987-232">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="93987-233">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="93987-233">-ScaleInPolicy</span></span>
<span data-ttu-id="93987-234">Die Regeln, die beim Skalieren in einem Skalierungs Satz einer virtuellen Maschine befolgt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="93987-234">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="93987-235">Mögliche Werte sind: "Standard", "OldestVM" und "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="93987-235">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="93987-236">"Standard" Wenn der Skalierungs Satz einer virtuellen Maschine skaliert wird, wird der Skalierungs Satz zunächst zonenübergreifend ausbalanciert, wenn es sich um einen Zonal-Skalierungs Satz handelt.</span><span class="sxs-lookup"><span data-stu-id="93987-236">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="93987-237">In diesem Fall werden die fehlerdomänen so weit wie möglich ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="93987-237">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="93987-238">Innerhalb jeder fehlerdomäne sind die für die Entfernung ausgewählten virtuellen Computer die neuesten, die nicht vor dem Skalieren geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="93987-238">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="93987-239">"OldestVM" Wenn ein Skalierungs Satz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="93987-239">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="93987-240">Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="93987-240">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="93987-241">Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="93987-241">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="93987-242">"NewestVM" Wenn ein Skalierungs Satz für virtuelle Maschinen skaliert wird, werden die neuesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="93987-242">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="93987-243">Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="93987-243">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="93987-244">In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="93987-244">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="93987-245">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="93987-245">-SinglePlacementGroup</span></span>
<span data-ttu-id="93987-246">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="93987-246">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="93987-247">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="93987-247">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="93987-248">Gibt an, dass die Erweiterungen nicht auf den zusätzlichen überlegten VMS ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="93987-248">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="93987-249">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="93987-249">-SkuCapacity</span></span>
<span data-ttu-id="93987-250">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="93987-250">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="93987-251">-SkuName</span><span class="sxs-lookup"><span data-stu-id="93987-251">-SkuName</span></span>
<span data-ttu-id="93987-252">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="93987-252">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="93987-253">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="93987-253">-SkuTier</span></span>
<span data-ttu-id="93987-254">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="93987-254">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="93987-255">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93987-255">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93987-256">Standard</span><span class="sxs-lookup"><span data-stu-id="93987-256">Standard</span></span>
- <span data-ttu-id="93987-257">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="93987-257">Basic</span></span>

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

### <span data-ttu-id="93987-258">-Tag</span><span class="sxs-lookup"><span data-stu-id="93987-258">-Tag</span></span>
<span data-ttu-id="93987-259">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="93987-259">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="93987-260">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="93987-260">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="93987-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="93987-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="93987-262">Konfigurierbare Zeitdauer (in Minuten) ein gelöschter virtueller Computer muss möglicherweise das Terminate scheduled-Ereignis genehmigen, bevor das Ereignis automatisch genehmigt wird (Timeout).</span><span class="sxs-lookup"><span data-stu-id="93987-262">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="93987-263">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="93987-263">-TerminateScheduledEvents</span></span>
<span data-ttu-id="93987-264">Gibt an, ob das terminierte terminierte Ereignis aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="93987-264">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="93987-265">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="93987-265">-TimeZone</span></span>
<span data-ttu-id="93987-266">Gibt die Zeitzone für Windows-Betriebssysteme an.</span><span class="sxs-lookup"><span data-stu-id="93987-266">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="93987-267">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="93987-267">-UltraSSDEnabled</span></span>
<span data-ttu-id="93987-268">Das Flag, mit dem eine Funktion für einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem Skalierungs Satz der virtuellen Maschine aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="93987-268">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="93987-269">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können nur dann einem VMSS hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="93987-269">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="93987-270">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="93987-270">-UpgradePolicyMode</span></span>
<span data-ttu-id="93987-271">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="93987-271">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="93987-272">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93987-272">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93987-273">Automatisch</span><span class="sxs-lookup"><span data-stu-id="93987-273">Automatic</span></span>
- <span data-ttu-id="93987-274">Manuell</span><span class="sxs-lookup"><span data-stu-id="93987-274">Manual</span></span>
- <span data-ttu-id="93987-275">Rollout</span><span class="sxs-lookup"><span data-stu-id="93987-275">Rolling</span></span>

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

### <span data-ttu-id="93987-276">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="93987-276">-VhdContainer</span></span>
<span data-ttu-id="93987-277">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93987-277">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="93987-278">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="93987-278">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="93987-279">Gibt ein lokales VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="93987-279">Specifies a local VMSS object.</span></span>
<span data-ttu-id="93987-280">Verwenden Sie das Get-AzVmss-Cmdlet, um ein VMSS-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93987-280">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="93987-281">Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für die VMSS.</span><span class="sxs-lookup"><span data-stu-id="93987-281">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="93987-282">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="93987-282">-VMScaleSetName</span></span>
<span data-ttu-id="93987-283">Gibt den Namen des von diesem Cmdlet erstellten VMSS an.</span><span class="sxs-lookup"><span data-stu-id="93987-283">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="93987-284">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="93987-284">-Confirm</span></span>
<span data-ttu-id="93987-285">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93987-285">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93987-286">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93987-286">-WhatIf</span></span>
<span data-ttu-id="93987-287">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93987-287">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93987-288">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93987-288">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93987-289">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93987-289">CommonParameters</span></span>
<span data-ttu-id="93987-290">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93987-290">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93987-291">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93987-291">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93987-292">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93987-292">INPUTS</span></span>

### <span data-ttu-id="93987-293">System. String</span><span class="sxs-lookup"><span data-stu-id="93987-293">System.String</span></span>

### <span data-ttu-id="93987-294">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="93987-294">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="93987-295">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93987-295">System.Boolean</span></span>

## <span data-ttu-id="93987-296">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93987-296">OUTPUTS</span></span>

### <span data-ttu-id="93987-297">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="93987-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="93987-298">Notizen</span><span class="sxs-lookup"><span data-stu-id="93987-298">NOTES</span></span>

## <span data-ttu-id="93987-299">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93987-299">RELATED LINKS</span></span>

[<span data-ttu-id="93987-300">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="93987-300">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="93987-301">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="93987-301">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="93987-302">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="93987-302">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="93987-303">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="93987-303">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="93987-304">Satz-AzVmss</span><span class="sxs-lookup"><span data-stu-id="93987-304">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="93987-305">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="93987-305">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="93987-306">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="93987-306">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


