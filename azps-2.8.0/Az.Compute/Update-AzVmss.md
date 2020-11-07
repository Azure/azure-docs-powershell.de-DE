---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: c8a482c4d3021e1dd5de30582d2dad501a20ed41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651852"
---
# <span data-ttu-id="14924-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="14924-101">Update-AzVmss</span></span>

## <span data-ttu-id="14924-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14924-102">SYNOPSIS</span></span>
<span data-ttu-id="14924-103">Aktualisiert den Zustand eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="14924-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="14924-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14924-104">SYNTAX</span></span>

### <span data-ttu-id="14924-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="14924-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14924-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="14924-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-IdentityId <String[]>] -IdentityType <ResourceIdentityType> [-ImageReferenceId <String>]
 [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>]
 [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14924-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14924-107">DESCRIPTION</span></span>
<span data-ttu-id="14924-108">Das Cmdlet **Update-AzVmss** aktualisiert den Zustand eines virtuellen Computer-Skalierungs Satzes (VMSS) auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="14924-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="14924-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14924-109">EXAMPLES</span></span>

### <span data-ttu-id="14924-110">Beispiel 1: Aktualisieren Sie den Zustand eines VMSS auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="14924-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="14924-111">Dieser Befehl aktualisiert den Zustand des VMSS mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört, in den Zustand eines lokalen VMSS-Objekts $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="14924-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="14924-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="14924-112">PARAMETERS</span></span>

### <span data-ttu-id="14924-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14924-113">-AsJob</span></span>
<span data-ttu-id="14924-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="14924-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="14924-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="14924-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="14924-116">Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="14924-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="14924-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="14924-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="14924-118">Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="14924-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="14924-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="14924-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="14924-120">Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14924-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="14924-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="14924-121">-CustomData</span></span>
<span data-ttu-id="14924-122">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="14924-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="14924-123">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="14924-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="14924-124">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="14924-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="14924-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14924-125">-DefaultProfile</span></span>
<span data-ttu-id="14924-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14924-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14924-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="14924-127">-DisableAutoRollback</span></span>
<span data-ttu-id="14924-128">Deaktivieren des automatischen Rollbacks für die Richtlinie für das automatische OS-Upgrade</span><span class="sxs-lookup"><span data-stu-id="14924-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="14924-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="14924-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="14924-130">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung für Linux-Betriebssystem deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="14924-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="14924-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="14924-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="14924-132">Gibt an, ob die Windows-virtuellen Computer im VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="14924-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="14924-133">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="14924-133">-IdentityId</span></span>
<span data-ttu-id="14924-134">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="14924-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="14924-135">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="14924-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="14924-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="14924-136">-IdentityType</span></span>
<span data-ttu-id="14924-137">Gibt den Typ der Identität an, die für den Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14924-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="14924-138">Der Typ "SystemAssignedUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Gruppe von Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="14924-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="14924-139">Der Typ "None" entfernt alle Identitäten aus dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="14924-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="14924-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="14924-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14924-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="14924-141">SystemAssigned</span></span>
- <span data-ttu-id="14924-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="14924-142">UserAssigned</span></span>
- <span data-ttu-id="14924-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="14924-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="14924-144">Keine</span><span class="sxs-lookup"><span data-stu-id="14924-144">None</span></span>

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

### <span data-ttu-id="14924-145">-Imagereference-Nr</span><span class="sxs-lookup"><span data-stu-id="14924-145">-ImageReferenceId</span></span>
<span data-ttu-id="14924-146">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="14924-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="14924-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="14924-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="14924-148">Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="14924-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="14924-149">Verwenden Sie das Get-AzVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="14924-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="14924-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="14924-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="14924-151">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="14924-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="14924-152">Verwenden Sie zum Abrufen eines Verlegers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14924-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="14924-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="14924-153">-ImageReferenceSku</span></span>
<span data-ttu-id="14924-154">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="14924-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="14924-155">Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14924-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="14924-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="14924-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="14924-157">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="14924-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="14924-158">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="14924-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="14924-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="14924-159">-ImageUri</span></span>
<span data-ttu-id="14924-160">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="14924-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="14924-161">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.</span><span class="sxs-lookup"><span data-stu-id="14924-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="14924-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="14924-162">-LicenseType</span></span>
<span data-ttu-id="14924-163">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="14924-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="14924-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="14924-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="14924-165">Gibt den Speicher Kontotyp für verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="14924-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="14924-166">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="14924-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14924-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="14924-167">StandardLRS</span></span>
- <span data-ttu-id="14924-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="14924-168">PremiumLRS</span></span>

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

### <span data-ttu-id="14924-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="14924-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="14924-170">Der maximale Prozentsatz der virtuellen Computer Instanzen, die vom parallelen Upgrade in einem Batch gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="14924-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="14924-171">Da dies ein Maximum ist, können ungesunde Instanzen in früheren oder zukünftigen Batches dazu führen, dass der Prozentsatz der Instanzen in einem Batch verringert wird, um eine höhere Zuverlässigkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="14924-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="14924-172">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="14924-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="14924-173">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="14924-173">-MaxPrice</span></span>
<span data-ttu-id="14924-174">Gibt den Höchstpreis an, den Sie für eine VM-VMSS mit niedriger Priorität bezahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="14924-174">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="14924-175">Dieser Preis ist in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="14924-175">This price is in US Dollars.</span></span> <span data-ttu-id="14924-176">Dieser Preis wird mit dem aktuellen Preis für niedrige Priorität für die VM-Größe verglichen.</span><span class="sxs-lookup"><span data-stu-id="14924-176">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="14924-177">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM-VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der maxprice größer als der aktuelle Preis für niedrige Priorität ist.</span><span class="sxs-lookup"><span data-stu-id="14924-177">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="14924-178">Die maxprice wird auch zum Entfernen einer VM-VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis für niedrige Priorität über die maxprice nach der Erstellung von VM/VMSS hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="14924-178">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="14924-179">Mögliche Werte sind: beliebiger Dezimalwert größer als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="14924-179">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="14924-180">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="14924-180">Example: 0.01538.</span></span>  <span data-ttu-id="14924-181">-1 gibt an, dass die VM-VMSS mit niedriger Priorität aus Preisgründen nicht vertrieben werden sollte.</span><span class="sxs-lookup"><span data-stu-id="14924-181">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="14924-182">Außerdem ist der standardmäßige Höchstpreis-1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="14924-182">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="14924-183">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="14924-183">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="14924-184">Der maximale Prozentsatz der gesamten virtuellen Computer Instanzen im Skalierungs Satz, die gleichzeitig fehlerhaft sein können, entweder als Ergebnis eines Upgrades oder durch die Integritätsprüfung des virtuellen Computers in einem ungesunden Zustand, bevor das parallele Upgrade abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="14924-184">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="14924-185">Diese Einschränkung wird vor dem Starten eines Batches überprüft.</span><span class="sxs-lookup"><span data-stu-id="14924-185">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="14924-186">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="14924-186">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="14924-187">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="14924-187">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="14924-188">Der maximale Prozentsatz der aktualisierten virtuellen Computer Instanzen, die sich in einem fehlerhaften Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="14924-188">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="14924-189">Diese Überprüfung erfolgt, nachdem jeder Batch aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="14924-189">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="14924-190">Wenn dieser Prozentsatz jemals überschritten wird, wird das Rolling-Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="14924-190">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="14924-191">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="14924-191">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="14924-192">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="14924-192">-OsDiskCaching</span></span>
<span data-ttu-id="14924-193">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="14924-193">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="14924-194">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="14924-194">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14924-195">Keine</span><span class="sxs-lookup"><span data-stu-id="14924-195">None</span></span>
- <span data-ttu-id="14924-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="14924-196">ReadOnly</span></span>
- <span data-ttu-id="14924-197">ReadWrite der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="14924-197">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="14924-198">Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="14924-198">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="14924-199">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="14924-199">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="14924-200">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="14924-200">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="14924-201">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="14924-201">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="14924-202">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="14924-202">-Overprovision</span></span>
<span data-ttu-id="14924-203">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="14924-203">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="14924-204">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="14924-204">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="14924-205">Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.</span><span class="sxs-lookup"><span data-stu-id="14924-205">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="14924-206">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="14924-206">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="14924-207">Der Standardwert ist 0 Sekunden (PT0S).</span><span class="sxs-lookup"><span data-stu-id="14924-207">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="14924-208">-Planname</span><span class="sxs-lookup"><span data-stu-id="14924-208">-PlanName</span></span>
<span data-ttu-id="14924-209">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="14924-209">Specifies the plan name.</span></span>

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

### <span data-ttu-id="14924-210">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="14924-210">-PlanProduct</span></span>
<span data-ttu-id="14924-211">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="14924-211">Specifies the plan product.</span></span>

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

### <span data-ttu-id="14924-212">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="14924-212">-PlanPromotionCode</span></span>
<span data-ttu-id="14924-213">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="14924-213">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="14924-214">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="14924-214">-PlanPublisher</span></span>
<span data-ttu-id="14924-215">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="14924-215">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="14924-216">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="14924-216">-ProvisionVMAgent</span></span>
<span data-ttu-id="14924-217">Gibt an, ob der Virtual Machine-Agent auf den virtuellen Windows-Computern im VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="14924-217">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="14924-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14924-218">-ResourceGroupName</span></span>
<span data-ttu-id="14924-219">Gibt den Namen der Ressourcengruppe an, zu der der VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="14924-219">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="14924-220">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="14924-220">-SinglePlacementGroup</span></span>
<span data-ttu-id="14924-221">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="14924-221">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="14924-222">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="14924-222">-SkuCapacity</span></span>
<span data-ttu-id="14924-223">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="14924-223">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="14924-224">-SkuName</span><span class="sxs-lookup"><span data-stu-id="14924-224">-SkuName</span></span>
<span data-ttu-id="14924-225">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="14924-225">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="14924-226">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="14924-226">-SkuTier</span></span>
<span data-ttu-id="14924-227">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="14924-227">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="14924-228">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="14924-228">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14924-229">Standard</span><span class="sxs-lookup"><span data-stu-id="14924-229">Standard</span></span>
- <span data-ttu-id="14924-230">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="14924-230">Basic</span></span>

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

### <span data-ttu-id="14924-231">-Tag</span><span class="sxs-lookup"><span data-stu-id="14924-231">-Tag</span></span>
<span data-ttu-id="14924-232">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="14924-232">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="14924-233">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="14924-233">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="14924-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="14924-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="14924-235">Konfigurierbare Zeitdauer (in Minuten) ein gelöschter virtueller Computer muss möglicherweise das Terminate scheduled-Ereignis genehmigen, bevor das Ereignis automatisch genehmigt wird (Timeout).</span><span class="sxs-lookup"><span data-stu-id="14924-235">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="14924-236">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="14924-236">-TerminateScheduledEvents</span></span>
<span data-ttu-id="14924-237">Gibt an, ob das terminierte terminierte Ereignis aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="14924-237">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="14924-238">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="14924-238">-TimeZone</span></span>
<span data-ttu-id="14924-239">Gibt die Zeitzone für Windows-Betriebssysteme an.</span><span class="sxs-lookup"><span data-stu-id="14924-239">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="14924-240">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="14924-240">-UltraSSDEnabled</span></span>
<span data-ttu-id="14924-241">Das Flag, mit dem eine Funktion für einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem Skalierungs Satz der virtuellen Maschine aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="14924-241">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="14924-242">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können nur dann einem VMSS hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="14924-242">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="14924-243">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="14924-243">-UpgradePolicyMode</span></span>
<span data-ttu-id="14924-244">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="14924-244">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="14924-245">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="14924-245">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14924-246">Automatisch</span><span class="sxs-lookup"><span data-stu-id="14924-246">Automatic</span></span>
- <span data-ttu-id="14924-247">Manuell</span><span class="sxs-lookup"><span data-stu-id="14924-247">Manual</span></span>
- <span data-ttu-id="14924-248">Rollout</span><span class="sxs-lookup"><span data-stu-id="14924-248">Rolling</span></span>

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

### <span data-ttu-id="14924-249">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="14924-249">-VhdContainer</span></span>
<span data-ttu-id="14924-250">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14924-250">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="14924-251">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="14924-251">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="14924-252">Gibt ein lokales VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="14924-252">Specifies a local VMSS object.</span></span>
<span data-ttu-id="14924-253">Verwenden Sie das Get-AzVmss-Cmdlet, um ein VMSS-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="14924-253">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="14924-254">Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für die VMSS.</span><span class="sxs-lookup"><span data-stu-id="14924-254">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="14924-255">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="14924-255">-VMScaleSetName</span></span>
<span data-ttu-id="14924-256">Gibt den Namen des von diesem Cmdlet erstellten VMSS an.</span><span class="sxs-lookup"><span data-stu-id="14924-256">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="14924-257">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="14924-257">-Confirm</span></span>
<span data-ttu-id="14924-258">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14924-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14924-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14924-259">-WhatIf</span></span>
<span data-ttu-id="14924-260">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14924-260">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14924-261">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14924-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14924-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14924-262">CommonParameters</span></span>
<span data-ttu-id="14924-263">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14924-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14924-264">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14924-264">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14924-265">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14924-265">INPUTS</span></span>

### <span data-ttu-id="14924-266">System. String</span><span class="sxs-lookup"><span data-stu-id="14924-266">System.String</span></span>

### <span data-ttu-id="14924-267">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="14924-267">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="14924-268">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14924-268">System.Boolean</span></span>

## <span data-ttu-id="14924-269">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14924-269">OUTPUTS</span></span>

### <span data-ttu-id="14924-270">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="14924-270">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="14924-271">Notizen</span><span class="sxs-lookup"><span data-stu-id="14924-271">NOTES</span></span>

## <span data-ttu-id="14924-272">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14924-272">RELATED LINKS</span></span>

[<span data-ttu-id="14924-273">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="14924-273">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="14924-274">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="14924-274">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="14924-275">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="14924-275">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="14924-276">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="14924-276">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="14924-277">Satz-AzVmss</span><span class="sxs-lookup"><span data-stu-id="14924-277">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="14924-278">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="14924-278">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="14924-279">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="14924-279">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


