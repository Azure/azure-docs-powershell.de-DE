---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 544af56c5e1ff72a3b23c3dcf89af36f7d74eff2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848856"
---
# <span data-ttu-id="336c3-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="336c3-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="336c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="336c3-102">SYNOPSIS</span></span>
<span data-ttu-id="336c3-103">Aktualisiert den Zustand eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="336c3-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="336c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="336c3-104">SYNTAX</span></span>

### <span data-ttu-id="336c3-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="336c3-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="336c3-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="336c3-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="336c3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="336c3-107">DESCRIPTION</span></span>
<span data-ttu-id="336c3-108">Das Cmdlet **Update-AzureRmVmss** aktualisiert den Zustand eines virtuellen Computer-Skalierungs Satzes (VMSS) auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="336c3-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="336c3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="336c3-109">EXAMPLES</span></span>

### <span data-ttu-id="336c3-110">Beispiel 1: Aktualisieren Sie den Zustand eines VMSS auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="336c3-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="336c3-111">Dieser Befehl aktualisiert den Zustand des VMSS mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört, in den Zustand eines lokalen VMSS-Objekts $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="336c3-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="336c3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="336c3-112">PARAMETERS</span></span>

### <span data-ttu-id="336c3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="336c3-113">-AsJob</span></span>
<span data-ttu-id="336c3-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="336c3-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="336c3-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="336c3-116">Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="336c3-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="336c3-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="336c3-118">Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="336c3-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="336c3-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="336c3-120">Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="336c3-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="336c3-121">-CustomData</span></span>
<span data-ttu-id="336c3-122">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="336c3-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="336c3-123">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="336c3-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="336c3-124">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="336c3-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336c3-125">-DefaultProfile</span></span>
<span data-ttu-id="336c3-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="336c3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="336c3-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="336c3-128">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung für Linux-Betriebssystem deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="336c3-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="336c3-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="336c3-130">Gibt an, ob die Windows-virtuellen Computer im VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="336c3-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-131">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="336c3-131">-IdentityId</span></span>
<span data-ttu-id="336c3-132">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="336c3-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="336c3-133">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="336c3-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="336c3-134">-IdentityType</span></span>
<span data-ttu-id="336c3-135">Gibt den Typ der Identität an, die für den Skalierungs Satz der virtuellen Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="336c3-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="336c3-136">Der Typ "SystemAssignedUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Gruppe von Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="336c3-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="336c3-137">Der Typ "None" entfernt alle Identitäten aus dem Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="336c3-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="336c3-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="336c3-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="336c3-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="336c3-139">SystemAssigned</span></span>
- <span data-ttu-id="336c3-140">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="336c3-140">UserAssigned</span></span>
- <span data-ttu-id="336c3-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="336c3-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="336c3-142">Keine</span><span class="sxs-lookup"><span data-stu-id="336c3-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-143">-Imagereference-Nr</span><span class="sxs-lookup"><span data-stu-id="336c3-143">-ImageReferenceId</span></span>
<span data-ttu-id="336c3-144">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="336c3-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="336c3-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="336c3-146">Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="336c3-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="336c3-147">Verwenden Sie das Get-AzureRmVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="336c3-147">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="336c3-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="336c3-149">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="336c3-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="336c3-150">Verwenden Sie zum Abrufen eines Verlegers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="336c3-150">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="336c3-151">-ImageReferenceSku</span></span>
<span data-ttu-id="336c3-152">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="336c3-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="336c3-153">Verwenden Sie zum Abrufen von SKUs das Get-AzureRmVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="336c3-153">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="336c3-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="336c3-155">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="336c3-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="336c3-156">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="336c3-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="336c3-157">-ImageUri</span></span>
<span data-ttu-id="336c3-158">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="336c3-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="336c3-159">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.</span><span class="sxs-lookup"><span data-stu-id="336c3-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="336c3-160">-LicenseType</span></span>
<span data-ttu-id="336c3-161">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="336c3-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="336c3-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="336c3-163">Gibt den Speicher Kontotyp für verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="336c3-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="336c3-164">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="336c3-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="336c3-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="336c3-165">StandardLRS</span></span>
- <span data-ttu-id="336c3-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="336c3-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="336c3-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="336c3-168">Der maximale Prozentsatz der virtuellen Computer Instanzen, die vom parallelen Upgrade in einem Batch gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="336c3-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="336c3-169">Da dies ein Maximum ist, können ungesunde Instanzen in früheren oder zukünftigen Batches dazu führen, dass der Prozentsatz der Instanzen in einem Batch verringert wird, um eine höhere Zuverlässigkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="336c3-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="336c3-170">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="336c3-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="336c3-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="336c3-172">Der maximale Prozentsatz der gesamten virtuellen Computer Instanzen im Skalierungs Satz, die gleichzeitig fehlerhaft sein können, entweder als Ergebnis eines Upgrades oder durch die Integritätsprüfung des virtuellen Computers in einem ungesunden Zustand, bevor das parallele Upgrade abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="336c3-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="336c3-173">Diese Einschränkung wird vor dem Starten eines Batches überprüft.</span><span class="sxs-lookup"><span data-stu-id="336c3-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="336c3-174">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="336c3-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="336c3-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="336c3-176">Der maximale Prozentsatz der aktualisierten virtuellen Computer Instanzen, die sich in einem fehlerhaften Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="336c3-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="336c3-177">Diese Überprüfung erfolgt, nachdem jeder Batch aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="336c3-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="336c3-178">Wenn dieser Prozentsatz jemals überschritten wird, wird das Rolling-Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="336c3-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="336c3-179">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="336c3-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="336c3-180">-OsDiskCaching</span></span>
<span data-ttu-id="336c3-181">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="336c3-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="336c3-182">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="336c3-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="336c3-183">Keine</span><span class="sxs-lookup"><span data-stu-id="336c3-183">None</span></span>
- <span data-ttu-id="336c3-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="336c3-184">ReadOnly</span></span>
- <span data-ttu-id="336c3-185">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="336c3-185">ReadWrite</span></span>

<span data-ttu-id="336c3-186">Der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="336c3-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="336c3-187">Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="336c3-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="336c3-188">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="336c3-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="336c3-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="336c3-190">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="336c3-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-191">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="336c3-191">-Overprovision</span></span>
<span data-ttu-id="336c3-192">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="336c3-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-193">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="336c3-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="336c3-194">Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.</span><span class="sxs-lookup"><span data-stu-id="336c3-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="336c3-195">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="336c3-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="336c3-196">Der Standardwert ist 0 Sekunden (PT0S).</span><span class="sxs-lookup"><span data-stu-id="336c3-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-197">-Planname</span><span class="sxs-lookup"><span data-stu-id="336c3-197">-PlanName</span></span>
<span data-ttu-id="336c3-198">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="336c3-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-199">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="336c3-199">-PlanProduct</span></span>
<span data-ttu-id="336c3-200">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="336c3-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="336c3-201">-PlanPromotionCode</span></span>
<span data-ttu-id="336c3-202">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="336c3-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="336c3-203">-PlanPublisher</span></span>
<span data-ttu-id="336c3-204">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="336c3-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="336c3-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="336c3-206">Gibt an, ob der Virtual Machine-Agent auf den virtuellen Windows-Computern im VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="336c3-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="336c3-207">-ResourceGroupName</span></span>
<span data-ttu-id="336c3-208">Gibt den Namen der Ressourcengruppe an, zu der der VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="336c3-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="336c3-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="336c3-210">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="336c3-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="336c3-211">-SkuCapacity</span></span>
<span data-ttu-id="336c3-212">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="336c3-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="336c3-213">-SkuName</span></span>
<span data-ttu-id="336c3-214">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="336c3-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="336c3-215">-SkuTier</span></span>
<span data-ttu-id="336c3-216">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="336c3-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="336c3-217">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="336c3-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="336c3-218">Standard</span><span class="sxs-lookup"><span data-stu-id="336c3-218">Standard</span></span>
- <span data-ttu-id="336c3-219">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="336c3-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-220">-Tag</span><span class="sxs-lookup"><span data-stu-id="336c3-220">-Tag</span></span>
<span data-ttu-id="336c3-221">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="336c3-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="336c3-222">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="336c3-222">For example:</span></span>

<span data-ttu-id="336c3-223">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="336c3-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="336c3-224">-TimeZone</span></span>
<span data-ttu-id="336c3-225">Gibt die Zeitzone für Windows-Betriebssysteme an.</span><span class="sxs-lookup"><span data-stu-id="336c3-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="336c3-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="336c3-227">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="336c3-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="336c3-228">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="336c3-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="336c3-229">Automatisch</span><span class="sxs-lookup"><span data-stu-id="336c3-229">Automatic</span></span>
- <span data-ttu-id="336c3-230">Manuell</span><span class="sxs-lookup"><span data-stu-id="336c3-230">Manual</span></span>
- <span data-ttu-id="336c3-231">Rollout</span><span class="sxs-lookup"><span data-stu-id="336c3-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="336c3-232">-VhdContainer</span></span>
<span data-ttu-id="336c3-233">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="336c3-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="336c3-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="336c3-235">Gibt ein lokales VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="336c3-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="336c3-236">Verwenden Sie das Get-AzureRmVmss-Cmdlet, um ein VMSS-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="336c3-236">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="336c3-237">Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für die VMSS.</span><span class="sxs-lookup"><span data-stu-id="336c3-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="336c3-238">-VMScaleSetName</span></span>
<span data-ttu-id="336c3-239">Gibt den Namen des von diesem Cmdlet erstellten VMSS an.</span><span class="sxs-lookup"><span data-stu-id="336c3-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-240">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="336c3-240">-Confirm</span></span>
<span data-ttu-id="336c3-241">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="336c3-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="336c3-242">-WhatIf</span></span>
<span data-ttu-id="336c3-243">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="336c3-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="336c3-244">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="336c3-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336c3-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336c3-245">CommonParameters</span></span>
<span data-ttu-id="336c3-246">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="336c3-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336c3-247">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="336c3-247">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336c3-248">Eingaben</span><span class="sxs-lookup"><span data-stu-id="336c3-248">INPUTS</span></span>

### <span data-ttu-id="336c3-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="336c3-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="336c3-250">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="336c3-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="336c3-251">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="336c3-251">OUTPUTS</span></span>

### <span data-ttu-id="336c3-252">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="336c3-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="336c3-253">Notizen</span><span class="sxs-lookup"><span data-stu-id="336c3-253">NOTES</span></span>

## <span data-ttu-id="336c3-254">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="336c3-254">RELATED LINKS</span></span>

[<span data-ttu-id="336c3-255">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="336c3-255">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="336c3-256">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="336c3-256">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="336c3-257">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="336c3-257">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="336c3-258">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="336c3-258">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="336c3-259">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="336c3-259">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="336c3-260">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="336c3-260">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="336c3-261">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="336c3-261">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


