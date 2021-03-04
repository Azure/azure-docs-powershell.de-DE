---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: ec233765f401348895275291ddad0571d1ddfc85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931355"
---
# <span data-ttu-id="61e09-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="61e09-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="61e09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61e09-102">SYNOPSIS</span></span>
<span data-ttu-id="61e09-103">Legt die Speicherprofileigenschaften für den VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="61e09-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="61e09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61e09-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61e09-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61e09-105">DESCRIPTION</span></span>
<span data-ttu-id="61e09-106">Das **Cmdlet Set-AzVmssStorageProfile** legt die Speicherprofileigenschaften für den VmSS (Virtual Machine Scale Set) fest.</span><span class="sxs-lookup"><span data-stu-id="61e09-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="61e09-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61e09-107">EXAMPLES</span></span>

### <span data-ttu-id="61e09-108">Beispiel 1: Festlegen der Speicherprofileigenschaften für den VMSS</span><span class="sxs-lookup"><span data-stu-id="61e09-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="61e09-109">Mit diesem Befehl werden die Speicherprofileigenschaften für den VMSS namens ContosoVMSS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="61e09-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="61e09-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="61e09-110">PARAMETERS</span></span>

### <span data-ttu-id="61e09-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="61e09-111">-DataDisk</span></span>
<span data-ttu-id="61e09-112">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="61e09-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e09-113">-DefaultProfile</span></span>
<span data-ttu-id="61e09-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61e09-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61e09-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="61e09-115">-DiffDiskSetting</span></span>
<span data-ttu-id="61e09-116">Gibt die unterschiedlichen Datenträgereinstellungen für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="61e09-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="61e09-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="61e09-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="61e09-118">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatzs an.</span><span class="sxs-lookup"><span data-stu-id="61e09-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="61e09-119">Dies kann nur für verwaltete Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61e09-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="61e09-120">-Image</span><span class="sxs-lookup"><span data-stu-id="61e09-120">-Image</span></span>
<span data-ttu-id="61e09-121">Gibt den Blob-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="61e09-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="61e09-122">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerabbilds.</span><span class="sxs-lookup"><span data-stu-id="61e09-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="61e09-123">-ImageReferenceId</span></span>
<span data-ttu-id="61e09-124">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="61e09-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="61e09-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="61e09-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="61e09-126">Gibt den Typ des Virtual Machine Image (VMImage)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="61e09-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="61e09-127">Verwenden Sie das cmdlet Get-AzVMImageOffer, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61e09-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="61e09-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="61e09-129">Gibt den Namen eines Herausgebers eines VMImages an.</span><span class="sxs-lookup"><span data-stu-id="61e09-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="61e09-130">Verwenden Sie das cmdlet Get-AzVMImagePublisher, um einen Herausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61e09-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="61e09-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="61e09-131">-ImageReferenceSku</span></span>
<span data-ttu-id="61e09-132">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="61e09-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="61e09-133">Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61e09-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="61e09-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="61e09-135">Gibt die Version des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="61e09-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="61e09-136">Wenn Sie die neueste Version verwenden möchten, geben Sie anstelle einer bestimmten Version den Wert der neuesten Version an.</span><span class="sxs-lookup"><span data-stu-id="61e09-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="61e09-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="61e09-137">-ManagedDisk</span></span>
<span data-ttu-id="61e09-138">Gibt den verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="61e09-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="61e09-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="61e09-139">-OsDiskCaching</span></span>
<span data-ttu-id="61e09-140">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="61e09-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="61e09-141">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="61e09-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="61e09-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="61e09-142">ReadOnly</span></span>
- <span data-ttu-id="61e09-143">ReadWrite Der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="61e09-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="61e09-144">Wenn Sie den Zwischenspeicherwert ändern, wird der virtuelle Computer vom Cmdlet neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="61e09-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="61e09-145">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="61e09-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="61e09-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="61e09-147">Gibt an, wie dieses Cmdlet die virtuellen VMSS-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="61e09-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="61e09-148">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="61e09-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="61e09-149">Anfügen: Dieser Wert wird verwendet, wenn Sie einen speziellen Datenträger zum Erstellen des virtuellen VMSS-Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="61e09-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="61e09-150">FromImage: Dieser Wert wird verwendet, wenn Sie ein Bild zum Erstellen des virtuellen VMSS-Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="61e09-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="61e09-151">Wenn Sie ein Plattformbild verwenden, verwenden Sie auch den *Parameter imageReference.*</span><span class="sxs-lookup"><span data-stu-id="61e09-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="61e09-152">-OsDiskName</span></span>
<span data-ttu-id="61e09-153">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="61e09-153">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="61e09-154">-OsDiskOsType</span></span>
<span data-ttu-id="61e09-155">Gibt den Typ des Betriebssystems auf dem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="61e09-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="61e09-156">Dies ist nur für Benutzerbildszenarien und nicht für ein Plattformbild erforderlich.</span><span class="sxs-lookup"><span data-stu-id="61e09-156">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="61e09-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="61e09-158">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="61e09-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="61e09-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="61e09-159">-VhdContainer</span></span>
<span data-ttu-id="61e09-160">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für den VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61e09-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="61e09-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="61e09-162">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="61e09-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="61e09-163">Zum Abrufen des -Objekts verwenden Sie das New-AzVmssConfig-Objekt.</span><span class="sxs-lookup"><span data-stu-id="61e09-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61e09-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61e09-164">-Confirm</span></span>
<span data-ttu-id="61e09-165">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61e09-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e09-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e09-166">-WhatIf</span></span>
<span data-ttu-id="61e09-167">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61e09-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61e09-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61e09-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61e09-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e09-169">CommonParameters</span></span>
<span data-ttu-id="61e09-170">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e09-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e09-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61e09-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e09-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61e09-172">INPUTS</span></span>

### <span data-ttu-id="61e09-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="61e09-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="61e09-174">System.String</span><span class="sxs-lookup"><span data-stu-id="61e09-174">System.String</span></span>

### <span data-ttu-id="61e09-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="61e09-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="61e09-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="61e09-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="61e09-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="61e09-177">System.String[]</span></span>

### <span data-ttu-id="61e09-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="61e09-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="61e09-179">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61e09-179">OUTPUTS</span></span>

### <span data-ttu-id="61e09-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="61e09-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="61e09-181">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="61e09-181">NOTES</span></span>

## <span data-ttu-id="61e09-182">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="61e09-182">RELATED LINKS</span></span>

[<span data-ttu-id="61e09-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="61e09-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="61e09-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="61e09-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="61e09-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="61e09-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="61e09-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="61e09-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


