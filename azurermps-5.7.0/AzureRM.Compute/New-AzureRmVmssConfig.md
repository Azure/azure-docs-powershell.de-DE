---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481318"
---
# <span data-ttu-id="582fe-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="582fe-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="582fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="582fe-102">SYNOPSIS</span></span>
<span data-ttu-id="582fe-103">Erstellt ein VMSS-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="582fe-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="582fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="582fe-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="582fe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="582fe-105">DESCRIPTION</span></span>
<span data-ttu-id="582fe-106">Das Cmdlet **New-AzureRmVmssConfig** erstellt ein konfigurierbares lokales Virtual Manager-Skalierungs Satz Objekt (VMSS).</span><span class="sxs-lookup"><span data-stu-id="582fe-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="582fe-107">Zum Konfigurieren des VMSS-Objekts sind andere Cmdlets erforderlich.</span><span class="sxs-lookup"><span data-stu-id="582fe-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="582fe-108">Diese Cmdlets lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="582fe-108">These cmdlets are:</span></span>

- <span data-ttu-id="582fe-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="582fe-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="582fe-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="582fe-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="582fe-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="582fe-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="582fe-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="582fe-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="582fe-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="582fe-113">EXAMPLES</span></span>

### <span data-ttu-id="582fe-114">Beispiel 1: Erstellen eines VMSS-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="582fe-114">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="582fe-115">In diesem Beispiel wird ein VMSS-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="582fe-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="582fe-116">Der erste Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="582fe-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="582fe-117">Der zweite Befehl verwendet das Cmdlet **New-AzureRmVmss** zum Erstellen eines VMSS, das das im ersten Befehl erstellte VMSS-Konfigurationsobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="582fe-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="582fe-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="582fe-118">PARAMETERS</span></span>

### <span data-ttu-id="582fe-119">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="582fe-119">-BootDiagnostic</span></span>
<span data-ttu-id="582fe-120">Gibt das Start Diagnose Profil für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="582fe-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-121">-Extension</span><span class="sxs-lookup"><span data-stu-id="582fe-121">-Extension</span></span>
<span data-ttu-id="582fe-122">Gibt das Erweiterungs Informationsobjekt für die VMSS an.</span><span class="sxs-lookup"><span data-stu-id="582fe-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="582fe-123">Sie können das **Add-AzureRmVmssExtension-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="582fe-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="582fe-124">-IdentityType</span></span>
<span data-ttu-id="582fe-125">Geben Sie die Identität des Skalierungs Satzes für virtuelle Maschinen an, wenn Sie konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="582fe-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="582fe-126">-LicenseType</span></span>
<span data-ttu-id="582fe-127">Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.</span><span class="sxs-lookup"><span data-stu-id="582fe-127">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="582fe-128">-Location</span></span>
<span data-ttu-id="582fe-129">Gibt die Azure-Position an, an der die VMSS erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="582fe-129">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-130">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="582fe-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="582fe-131">Gibt das Netzwerkprofil Objekt an, das die Netzwerkeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="582fe-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="582fe-132">Sie können das **Add-AzureRmVmssNetworkInterfaceConfiguration-** Cmdlet verwenden, um dieses Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="582fe-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="582fe-133">-OsProfile</span></span>
<span data-ttu-id="582fe-134">Gibt das Betriebssystem-Profilobjekt an, das die Betriebssystemeigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="582fe-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="582fe-135">Sie können das Cmdlet " **Satz-AzureRmVmssOsProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="582fe-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-136">-Überversorgung</span><span class="sxs-lookup"><span data-stu-id="582fe-136">-Overprovision</span></span>
<span data-ttu-id="582fe-137">Gibt an, ob das Cmdlet die VMSS überzeichnet.</span><span class="sxs-lookup"><span data-stu-id="582fe-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-138">-Planname</span><span class="sxs-lookup"><span data-stu-id="582fe-138">-PlanName</span></span>
<span data-ttu-id="582fe-139">Gibt den Plan Namen an.</span><span class="sxs-lookup"><span data-stu-id="582fe-139">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-140">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="582fe-140">-PlanProduct</span></span>
<span data-ttu-id="582fe-141">Gibt das Plan Produkt an.</span><span class="sxs-lookup"><span data-stu-id="582fe-141">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="582fe-142">-PlanPromotionCode</span></span>
<span data-ttu-id="582fe-143">Gibt den Plan Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="582fe-143">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-144">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="582fe-144">-PlanPublisher</span></span>
<span data-ttu-id="582fe-145">Gibt den Plan Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="582fe-145">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="582fe-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="582fe-147">Geben Sie die Wiederherstellungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="582fe-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-148">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="582fe-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="582fe-149">Gibt die Gruppe für einzelne Placements an.</span><span class="sxs-lookup"><span data-stu-id="582fe-149">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-150">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="582fe-150">-SkuCapacity</span></span>
<span data-ttu-id="582fe-151">Gibt die Anzahl der Instanzen im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="582fe-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="582fe-152">-SkuName</span></span>
<span data-ttu-id="582fe-153">Gibt die Größe aller Instanzen von VMSS an.</span><span class="sxs-lookup"><span data-stu-id="582fe-153">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-154">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="582fe-154">-SkuTier</span></span>
<span data-ttu-id="582fe-155">Gibt die VMSS-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="582fe-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="582fe-156">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="582fe-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="582fe-157">Standard</span><span class="sxs-lookup"><span data-stu-id="582fe-157">Standard</span></span>
- <span data-ttu-id="582fe-158">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="582fe-158">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="582fe-159">-StorageProfile</span></span>
<span data-ttu-id="582fe-160">Gibt das Speicherprofil Objekt an, das die Datenträgereigenschaften für die VMSS-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="582fe-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="582fe-161">Sie können das Cmdlet " **Satz-AzureRmVmssStorageProfile** " verwenden, um dieses Objekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="582fe-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="582fe-162">-Tag</span></span>
<span data-ttu-id="582fe-163">Gibt die Tags an, die dem VMSS zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="582fe-163">Specifies the tags that will be assigned to the VMSS.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="582fe-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="582fe-165">Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.</span><span class="sxs-lookup"><span data-stu-id="582fe-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="582fe-166">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="582fe-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="582fe-167">Automatisch</span><span class="sxs-lookup"><span data-stu-id="582fe-167">Automatic</span></span>
- <span data-ttu-id="582fe-168">Manuell</span><span class="sxs-lookup"><span data-stu-id="582fe-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="582fe-169">-Confirm</span></span>
<span data-ttu-id="582fe-170">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="582fe-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="582fe-171">-WhatIf</span></span>
<span data-ttu-id="582fe-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="582fe-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="582fe-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="582fe-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="582fe-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582fe-174">CommonParameters</span></span>
<span data-ttu-id="582fe-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582fe-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582fe-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="582fe-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582fe-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="582fe-177">INPUTS</span></span>

### <span data-ttu-id="582fe-178">Keine</span><span class="sxs-lookup"><span data-stu-id="582fe-178">None</span></span>
<span data-ttu-id="582fe-179">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="582fe-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="582fe-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="582fe-180">OUTPUTS</span></span>

### <span data-ttu-id="582fe-181">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="582fe-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="582fe-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="582fe-182">NOTES</span></span>

## <span data-ttu-id="582fe-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="582fe-183">RELATED LINKS</span></span>

[<span data-ttu-id="582fe-184">Satz-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="582fe-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="582fe-185">Satz-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="582fe-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="582fe-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="582fe-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="582fe-187">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="582fe-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="582fe-188">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="582fe-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


