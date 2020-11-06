---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: d2ecc5799319dcbc9b2e3710c186ffd7ebc09c64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499650"
---
# <span data-ttu-id="c471f-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c471f-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="c471f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c471f-102">SYNOPSIS</span></span>
<span data-ttu-id="c471f-103">Aktualisiert den Zustand eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="c471f-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c471f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c471f-104">SYNTAX</span></span>

### <span data-ttu-id="c471f-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="c471f-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>]
 [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>]
 [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c471f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c471f-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>]
 -IdentityType <ResourceIdentityType> [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c471f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c471f-107">DESCRIPTION</span></span>
<span data-ttu-id="c471f-108">Das Cmdlet **Update-AzureRmVmss** aktualisiert den Zustand eines virtuellen Computer-Skalierungs Satzes (VMSS) auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c471f-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="c471f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c471f-109">EXAMPLES</span></span>

### <span data-ttu-id="c471f-110">Beispiel 1: Aktualisieren Sie den Zustand eines VMSS auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c471f-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="c471f-111">Dieser Befehl aktualisiert den Zustand des VMSS mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört, in den Zustand eines lokalen VMSS-Objekts $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="c471f-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="c471f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c471f-112">PARAMETERS</span></span>

### <span data-ttu-id="c471f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c471f-113">-AsJob</span></span>
<span data-ttu-id="c471f-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="c471f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c471f-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c471f-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="c471f-116">Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c471f-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="c471f-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="c471f-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="c471f-118">Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c471f-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="c471f-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="c471f-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="c471f-120">Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c471f-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="c471f-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="c471f-121">-CustomData</span></span>
<span data-ttu-id="c471f-122">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="c471f-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="c471f-123">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c471f-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="c471f-124">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="c471f-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="c471f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c471f-125">-DefaultProfile</span></span>
<span data-ttu-id="c471f-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c471f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c471f-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="c471f-127">-DisableAutoRollback</span></span>
<span data-ttu-id="c471f-128">Deaktivieren des automatischen Rollbacks für die Richtlinie für das automatische OS-Upgrade</span><span class="sxs-lookup"><span data-stu-id="c471f-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="c471f-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="c471f-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="c471f-130">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung für Linux-Betriebssystem deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c471f-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="c471f-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="c471f-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="c471f-132">Gibt an, ob die Windows-virtuellen Computer im VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c471f-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="c471f-133">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="c471f-133">-IdentityId</span></span>
<span data-ttu-id="c471f-134">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c471f-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="c471f-135">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="c471f-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="c471f-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c471f-136">-IdentityType</span></span>
<span data-ttu-id="c471f-137">Gibt den Typ der Identität an, die für den Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c471f-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="c471f-138">Der Typ "SystemAssignedUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Gruppe von Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="c471f-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="c471f-139">Der Typ "None" entfernt alle Identitäten aus dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="c471f-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="c471f-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c471f-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c471f-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="c471f-141">SystemAssigned</span></span>
- <span data-ttu-id="c471f-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="c471f-142">UserAssigned</span></span>
- <span data-ttu-id="c471f-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="c471f-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="c471f-144">Keine</span><span class="sxs-lookup"><span data-stu-id="c471f-144">None</span></span>

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

### <span data-ttu-id="c471f-145">-Imagereference-Nr</span><span class="sxs-lookup"><span data-stu-id="c471f-145">-ImageReferenceId</span></span>
<span data-ttu-id="c471f-146">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="c471f-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="c471f-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="c471f-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="c471f-148">Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="c471f-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="c471f-149">Verwenden Sie das Get-AzureRmVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c471f-149">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="c471f-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="c471f-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="c471f-151">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="c471f-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="c471f-152">Verwenden Sie zum Abrufen eines Verlegers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c471f-152">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="c471f-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="c471f-153">-ImageReferenceSku</span></span>
<span data-ttu-id="c471f-154">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="c471f-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="c471f-155">Verwenden Sie zum Abrufen von SKUs das Get-AzureRmVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c471f-155">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="c471f-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="c471f-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="c471f-157">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="c471f-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="c471f-158">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="c471f-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="c471f-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="c471f-159">-ImageUri</span></span>
<span data-ttu-id="c471f-160">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="c471f-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="c471f-161">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.</span><span class="sxs-lookup"><span data-stu-id="c471f-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="c471f-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c471f-162">-LicenseType</span></span>
<span data-ttu-id="c471f-163">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="c471f-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="c471f-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c471f-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="c471f-165">Gibt den Speicher Kontotyp für verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="c471f-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="c471f-166">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c471f-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c471f-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="c471f-167">StandardLRS</span></span>
- <span data-ttu-id="c471f-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="c471f-168">PremiumLRS</span></span>

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

### <span data-ttu-id="c471f-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="c471f-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="c471f-170">Der maximale Prozentsatz der virtuellen Computer Instanzen, die vom parallelen Upgrade in einem Batch gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c471f-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="c471f-171">Da dies ein Maximum ist, können ungesunde Instanzen in früheren oder zukünftigen Batches dazu führen, dass der Prozentsatz der Instanzen in einem Batch verringert wird, um eine höhere Zuverlässigkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="c471f-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="c471f-172">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c471f-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="c471f-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="c471f-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="c471f-174">Der maximale Prozentsatz der gesamten virtuellen Computer Instanzen im Skalierungs Satz, die gleichzeitig fehlerhaft sein können, entweder als Ergebnis eines Upgrades oder durch die Integritätsprüfung des virtuellen Computers in einem ungesunden Zustand, bevor das parallele Upgrade abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="c471f-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="c471f-175">Diese Einschränkung wird vor dem Starten eines Batches überprüft.</span><span class="sxs-lookup"><span data-stu-id="c471f-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="c471f-176">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c471f-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="c471f-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="c471f-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="c471f-178">Der maximale Prozentsatz der aktualisierten virtuellen Computer Instanzen, die sich in einem fehlerhaften Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="c471f-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="c471f-179">Diese Überprüfung erfolgt, nachdem jeder Batch aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c471f-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="c471f-180">Wenn dieser Prozentsatz jemals überschritten wird, wird das Rolling-Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c471f-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="c471f-181">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c471f-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="c471f-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="c471f-182">-OsDiskCaching</span></span>
<span data-ttu-id="c471f-183">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="c471f-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="c471f-184">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c471f-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c471f-185">Keine</span><span class="sxs-lookup"><span data-stu-id="c471f-185">None</span></span>
- <span data-ttu-id="c471f-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c471f-186">ReadOnly</span></span>
- <span data-ttu-id="c471f-187">ReadWrite der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="c471f-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="c471f-188">Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="c471f-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="c471f-189">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="c471f-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="c471f-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="c471f-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="c471f-191">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c471f-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="c471f-192">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="c471f-192">-Overprovision</span></span>
<span data-ttu-id="c471f-193">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="c471f-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="c471f-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="c471f-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="c471f-195">Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.</span><span class="sxs-lookup"><span data-stu-id="c471f-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="c471f-196">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c471f-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="c471f-197">Der Standardwert ist 0 Sekunden (PT0S).</span><span class="sxs-lookup"><span data-stu-id="c471f-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="c471f-198">-Planname</span><span class="sxs-lookup"><span data-stu-id="c471f-198">-PlanName</span></span>
<span data-ttu-id="c471f-199">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="c471f-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="c471f-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="c471f-200">-PlanProduct</span></span>
<span data-ttu-id="c471f-201">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="c471f-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="c471f-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="c471f-202">-PlanPromotionCode</span></span>
<span data-ttu-id="c471f-203">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="c471f-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="c471f-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="c471f-204">-PlanPublisher</span></span>
<span data-ttu-id="c471f-205">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="c471f-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="c471f-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="c471f-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="c471f-207">Gibt an, ob der Virtual Machine-Agent auf den virtuellen Windows-Computern im VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c471f-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="c471f-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c471f-208">-ResourceGroupName</span></span>
<span data-ttu-id="c471f-209">Gibt den Namen der Ressourcengruppe an, zu der der VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="c471f-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c471f-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c471f-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="c471f-211">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="c471f-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="c471f-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c471f-212">-SkuCapacity</span></span>
<span data-ttu-id="c471f-213">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="c471f-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="c471f-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c471f-214">-SkuName</span></span>
<span data-ttu-id="c471f-215">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="c471f-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="c471f-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c471f-216">-SkuTier</span></span>
<span data-ttu-id="c471f-217">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="c471f-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="c471f-218">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c471f-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c471f-219">Standard</span><span class="sxs-lookup"><span data-stu-id="c471f-219">Standard</span></span>
- <span data-ttu-id="c471f-220">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="c471f-220">Basic</span></span>

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

### <span data-ttu-id="c471f-221">-Tag</span><span class="sxs-lookup"><span data-stu-id="c471f-221">-Tag</span></span>
<span data-ttu-id="c471f-222">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="c471f-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c471f-223">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="c471f-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c471f-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="c471f-224">-TimeZone</span></span>
<span data-ttu-id="c471f-225">Gibt die Zeitzone für Windows-Betriebssysteme an.</span><span class="sxs-lookup"><span data-stu-id="c471f-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="c471f-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="c471f-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="c471f-227">Das Flag, mit dem eine Funktion für einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem Skalierungs Satz der virtuellen Maschine aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c471f-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="c471f-228">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können nur dann einem VMSS hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c471f-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="c471f-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="c471f-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="c471f-230">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="c471f-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="c471f-231">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c471f-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c471f-232">Automatisch</span><span class="sxs-lookup"><span data-stu-id="c471f-232">Automatic</span></span>
- <span data-ttu-id="c471f-233">Manuell</span><span class="sxs-lookup"><span data-stu-id="c471f-233">Manual</span></span>
- <span data-ttu-id="c471f-234">Rollout</span><span class="sxs-lookup"><span data-stu-id="c471f-234">Rolling</span></span>

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

### <span data-ttu-id="c471f-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="c471f-235">-VhdContainer</span></span>
<span data-ttu-id="c471f-236">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c471f-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="c471f-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c471f-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c471f-238">Gibt ein lokales VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c471f-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="c471f-239">Verwenden Sie das Get-AzureRmVmss-Cmdlet, um ein VMSS-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c471f-239">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="c471f-240">Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für die VMSS.</span><span class="sxs-lookup"><span data-stu-id="c471f-240">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c471f-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c471f-241">-VMScaleSetName</span></span>
<span data-ttu-id="c471f-242">Gibt den Namen des von diesem Cmdlet erstellten VMSS an.</span><span class="sxs-lookup"><span data-stu-id="c471f-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c471f-243">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c471f-243">-Confirm</span></span>
<span data-ttu-id="c471f-244">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c471f-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c471f-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c471f-245">-WhatIf</span></span>
<span data-ttu-id="c471f-246">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c471f-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c471f-247">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c471f-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c471f-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c471f-248">CommonParameters</span></span>
<span data-ttu-id="c471f-249">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c471f-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c471f-250">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c471f-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c471f-251">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c471f-251">INPUTS</span></span>

### <span data-ttu-id="c471f-252">System. String</span><span class="sxs-lookup"><span data-stu-id="c471f-252">System.String</span></span>

### <span data-ttu-id="c471f-253">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c471f-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="c471f-254">Parameter: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c471f-254">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

## <span data-ttu-id="c471f-255">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c471f-255">OUTPUTS</span></span>

### <span data-ttu-id="c471f-256">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c471f-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c471f-257">Notizen</span><span class="sxs-lookup"><span data-stu-id="c471f-257">NOTES</span></span>

## <span data-ttu-id="c471f-258">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c471f-258">RELATED LINKS</span></span>

[<span data-ttu-id="c471f-259">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c471f-259">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c471f-260">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c471f-260">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c471f-261">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c471f-261">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c471f-262">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c471f-262">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c471f-263">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c471f-263">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c471f-264">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c471f-264">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="c471f-265">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c471f-265">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


