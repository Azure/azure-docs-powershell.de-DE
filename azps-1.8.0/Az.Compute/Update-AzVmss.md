---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 6fe6f6345f9208a524e1162fb317b88c450f3909
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661400"
---
# <span data-ttu-id="88aa6-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88aa6-101">Update-AzVmss</span></span>

## <span data-ttu-id="88aa6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="88aa6-103">Aktualisiert den Zustand eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="88aa6-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="88aa6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88aa6-104">SYNTAX</span></span>

### <span data-ttu-id="88aa6-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="88aa6-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>] [-SkuTier <String>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>] [-PlanPublisher <String>]
 [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>] [-DisableAutoRollback <Boolean>]
 [-TimeZone <String>] [-PlanPromotionCode <String>] [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>]
 [-VhdContainer <String[]>] [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-SkuName <String>] [-ImageReferenceVersion <String>]
 [-PauseTimeBetweenBatches <String>] [-ImageUri <String>] [-PlanName <String>] [-PlanProduct <String>]
 [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>] [-CustomData <String>] [-LicenseType <String>]
 [-OsDiskCaching <CachingTypes>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88aa6-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="88aa6-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 -IdentityType <ResourceIdentityType> [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SkuTier <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>]
 [-PlanPublisher <String>] [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>]
 [-DisableAutoRollback <Boolean>] [-TimeZone <String>] [-PlanPromotionCode <String>]
 [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>] [-VhdContainer <String[]>]
 [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-SkuName <String>] [-ImageReferenceVersion <String>] [-PauseTimeBetweenBatches <String>] [-ImageUri <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>]
 [-CustomData <String>] [-LicenseType <String>] [-OsDiskCaching <CachingTypes>] [-IdentityId <String[]>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88aa6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88aa6-107">DESCRIPTION</span></span>
<span data-ttu-id="88aa6-108">Das Cmdlet **Update-AzVmss** aktualisiert den Zustand eines virtuellen Computer-Skalierungs Satzes (VMSS) auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="88aa6-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="88aa6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88aa6-109">EXAMPLES</span></span>

### <span data-ttu-id="88aa6-110">Beispiel 1: Aktualisieren Sie den Zustand eines VMSS auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="88aa6-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="88aa6-111">Dieser Befehl aktualisiert den Zustand des VMSS mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört, in den Zustand eines lokalen VMSS-Objekts $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="88aa6-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="88aa6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="88aa6-112">PARAMETERS</span></span>

### <span data-ttu-id="88aa6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88aa6-113">-AsJob</span></span>
<span data-ttu-id="88aa6-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="88aa6-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="88aa6-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="88aa6-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="88aa6-116">Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="88aa6-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="88aa6-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="88aa6-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="88aa6-118">Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="88aa6-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="88aa6-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="88aa6-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="88aa6-120">Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="88aa6-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="88aa6-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="88aa6-121">-CustomData</span></span>
<span data-ttu-id="88aa6-122">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="88aa6-123">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="88aa6-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="88aa6-124">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="88aa6-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="88aa6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88aa6-125">-DefaultProfile</span></span>
<span data-ttu-id="88aa6-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88aa6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88aa6-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="88aa6-127">-DisableAutoRollback</span></span>
<span data-ttu-id="88aa6-128">Deaktivieren des automatischen Rollbacks für die Richtlinie für das automatische OS-Upgrade</span><span class="sxs-lookup"><span data-stu-id="88aa6-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="88aa6-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="88aa6-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="88aa6-130">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung für Linux-Betriebssystem deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="88aa6-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="88aa6-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="88aa6-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="88aa6-132">Gibt an, ob die Windows-virtuellen Computer im VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="88aa6-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="88aa6-133">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="88aa6-133">-IdentityId</span></span>
<span data-ttu-id="88aa6-134">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="88aa6-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="88aa6-135">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="88aa6-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="88aa6-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="88aa6-136">-IdentityType</span></span>
<span data-ttu-id="88aa6-137">Gibt den Typ der Identität an, die für den Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="88aa6-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="88aa6-138">Der Typ "SystemAssignedUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Gruppe von Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="88aa6-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="88aa6-139">Der Typ "None" entfernt alle Identitäten aus dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="88aa6-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="88aa6-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="88aa6-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88aa6-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="88aa6-141">SystemAssigned</span></span>
- <span data-ttu-id="88aa6-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="88aa6-142">UserAssigned</span></span>
- <span data-ttu-id="88aa6-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="88aa6-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="88aa6-144">Keine</span><span class="sxs-lookup"><span data-stu-id="88aa6-144">None</span></span>

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

### <span data-ttu-id="88aa6-145">-Imagereference-Nr</span><span class="sxs-lookup"><span data-stu-id="88aa6-145">-ImageReferenceId</span></span>
<span data-ttu-id="88aa6-146">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="88aa6-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="88aa6-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="88aa6-148">Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="88aa6-149">Verwenden Sie das Get-AzVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88aa6-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="88aa6-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="88aa6-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="88aa6-151">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="88aa6-152">Verwenden Sie zum Abrufen eines Verlegers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88aa6-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="88aa6-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="88aa6-153">-ImageReferenceSku</span></span>
<span data-ttu-id="88aa6-154">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="88aa6-155">Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88aa6-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="88aa6-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="88aa6-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="88aa6-157">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="88aa6-158">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="88aa6-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="88aa6-159">-ImageUri</span></span>
<span data-ttu-id="88aa6-160">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="88aa6-161">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.</span><span class="sxs-lookup"><span data-stu-id="88aa6-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="88aa6-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="88aa6-162">-LicenseType</span></span>
<span data-ttu-id="88aa6-163">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="88aa6-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="88aa6-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="88aa6-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="88aa6-165">Gibt den Speicher Kontotyp für verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="88aa6-166">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="88aa6-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88aa6-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="88aa6-167">StandardLRS</span></span>
- <span data-ttu-id="88aa6-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="88aa6-168">PremiumLRS</span></span>

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

### <span data-ttu-id="88aa6-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="88aa6-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="88aa6-170">Der maximale Prozentsatz der virtuellen Computer Instanzen, die vom parallelen Upgrade in einem Batch gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="88aa6-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="88aa6-171">Da dies ein Maximum ist, können ungesunde Instanzen in früheren oder zukünftigen Batches dazu führen, dass der Prozentsatz der Instanzen in einem Batch verringert wird, um eine höhere Zuverlässigkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="88aa6-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="88aa6-172">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88aa6-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="88aa6-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="88aa6-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="88aa6-174">Der maximale Prozentsatz der gesamten virtuellen Computer Instanzen im Skalierungs Satz, die gleichzeitig fehlerhaft sein können, entweder als Ergebnis eines Upgrades oder durch die Integritätsprüfung des virtuellen Computers in einem ungesunden Zustand, bevor das parallele Upgrade abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="88aa6-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="88aa6-175">Diese Einschränkung wird vor dem Starten eines Batches überprüft.</span><span class="sxs-lookup"><span data-stu-id="88aa6-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="88aa6-176">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88aa6-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="88aa6-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="88aa6-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="88aa6-178">Der maximale Prozentsatz der aktualisierten virtuellen Computer Instanzen, die sich in einem fehlerhaften Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="88aa6-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="88aa6-179">Diese Überprüfung erfolgt, nachdem jeder Batch aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="88aa6-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="88aa6-180">Wenn dieser Prozentsatz jemals überschritten wird, wird das Rolling-Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="88aa6-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="88aa6-181">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88aa6-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="88aa6-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="88aa6-182">-OsDiskCaching</span></span>
<span data-ttu-id="88aa6-183">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="88aa6-184">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="88aa6-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88aa6-185">Keine</span><span class="sxs-lookup"><span data-stu-id="88aa6-185">None</span></span>
- <span data-ttu-id="88aa6-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="88aa6-186">ReadOnly</span></span>
- <span data-ttu-id="88aa6-187">ReadWrite der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="88aa6-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="88aa6-188">Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="88aa6-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="88aa6-189">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="88aa6-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="88aa6-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="88aa6-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="88aa6-191">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="88aa6-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="88aa6-192">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="88aa6-192">-Overprovision</span></span>
<span data-ttu-id="88aa6-193">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="88aa6-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="88aa6-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="88aa6-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="88aa6-195">Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.</span><span class="sxs-lookup"><span data-stu-id="88aa6-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="88aa6-196">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="88aa6-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="88aa6-197">Der Standardwert ist 0 Sekunden (PT0S).</span><span class="sxs-lookup"><span data-stu-id="88aa6-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="88aa6-198">-Planname</span><span class="sxs-lookup"><span data-stu-id="88aa6-198">-PlanName</span></span>
<span data-ttu-id="88aa6-199">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="88aa6-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="88aa6-200">-PlanProduct</span></span>
<span data-ttu-id="88aa6-201">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="88aa6-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="88aa6-202">-PlanPromotionCode</span></span>
<span data-ttu-id="88aa6-203">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="88aa6-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="88aa6-204">-PlanPublisher</span></span>
<span data-ttu-id="88aa6-205">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="88aa6-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="88aa6-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="88aa6-207">Gibt an, ob der Virtual Machine-Agent auf den virtuellen Windows-Computern im VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="88aa6-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="88aa6-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88aa6-208">-ResourceGroupName</span></span>
<span data-ttu-id="88aa6-209">Gibt den Namen der Ressourcengruppe an, zu der der VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="88aa6-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="88aa6-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="88aa6-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="88aa6-211">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="88aa6-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="88aa6-212">-SkuCapacity</span></span>
<span data-ttu-id="88aa6-213">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="88aa6-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="88aa6-214">-SkuName</span></span>
<span data-ttu-id="88aa6-215">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="88aa6-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="88aa6-216">-SkuTier</span></span>
<span data-ttu-id="88aa6-217">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="88aa6-218">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="88aa6-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88aa6-219">Standard</span><span class="sxs-lookup"><span data-stu-id="88aa6-219">Standard</span></span>
- <span data-ttu-id="88aa6-220">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="88aa6-220">Basic</span></span>

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

### <span data-ttu-id="88aa6-221">-Tag</span><span class="sxs-lookup"><span data-stu-id="88aa6-221">-Tag</span></span>
<span data-ttu-id="88aa6-222">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="88aa6-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="88aa6-223">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="88aa6-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="88aa6-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="88aa6-224">-TimeZone</span></span>
<span data-ttu-id="88aa6-225">Gibt die Zeitzone für Windows-Betriebssysteme an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="88aa6-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="88aa6-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="88aa6-227">Das Flag, mit dem eine Funktion für einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem Skalierungs Satz der virtuellen Maschine aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="88aa6-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="88aa6-228">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können nur dann einem VMSS hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="88aa6-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="88aa6-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="88aa6-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="88aa6-230">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="88aa6-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="88aa6-231">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="88aa6-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88aa6-232">Automatisch</span><span class="sxs-lookup"><span data-stu-id="88aa6-232">Automatic</span></span>
- <span data-ttu-id="88aa6-233">Manuell</span><span class="sxs-lookup"><span data-stu-id="88aa6-233">Manual</span></span>
- <span data-ttu-id="88aa6-234">Rollout</span><span class="sxs-lookup"><span data-stu-id="88aa6-234">Rolling</span></span>

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

### <span data-ttu-id="88aa6-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="88aa6-235">-VhdContainer</span></span>
<span data-ttu-id="88aa6-236">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88aa6-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="88aa6-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="88aa6-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="88aa6-238">Gibt ein lokales VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="88aa6-239">Verwenden Sie das Get-AzVmss-Cmdlet, um ein VMSS-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88aa6-239">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="88aa6-240">Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für die VMSS.</span><span class="sxs-lookup"><span data-stu-id="88aa6-240">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="88aa6-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="88aa6-241">-VMScaleSetName</span></span>
<span data-ttu-id="88aa6-242">Gibt den Namen des von diesem Cmdlet erstellten VMSS an.</span><span class="sxs-lookup"><span data-stu-id="88aa6-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="88aa6-243">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88aa6-243">-Confirm</span></span>
<span data-ttu-id="88aa6-244">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88aa6-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88aa6-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88aa6-245">-WhatIf</span></span>
<span data-ttu-id="88aa6-246">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88aa6-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88aa6-247">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88aa6-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88aa6-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88aa6-248">CommonParameters</span></span>
<span data-ttu-id="88aa6-249">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88aa6-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88aa6-250">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88aa6-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88aa6-251">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88aa6-251">INPUTS</span></span>

### <span data-ttu-id="88aa6-252">System. String</span><span class="sxs-lookup"><span data-stu-id="88aa6-252">System.String</span></span>

### <span data-ttu-id="88aa6-253">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="88aa6-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="88aa6-254">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88aa6-254">System.Boolean</span></span>

## <span data-ttu-id="88aa6-255">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88aa6-255">OUTPUTS</span></span>

### <span data-ttu-id="88aa6-256">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="88aa6-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="88aa6-257">Notizen</span><span class="sxs-lookup"><span data-stu-id="88aa6-257">NOTES</span></span>

## <span data-ttu-id="88aa6-258">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88aa6-258">RELATED LINKS</span></span>

[<span data-ttu-id="88aa6-259">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88aa6-259">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="88aa6-260">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="88aa6-260">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="88aa6-261">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88aa6-261">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="88aa6-262">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88aa6-262">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="88aa6-263">Satz-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88aa6-263">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="88aa6-264">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88aa6-264">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="88aa6-265">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88aa6-265">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


