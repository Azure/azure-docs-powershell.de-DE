---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 44156d29d352adb83fe10fa898af2f655bfd4456
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661422"
---
# <span data-ttu-id="23914-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="23914-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="23914-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23914-102">SYNOPSIS</span></span>
<span data-ttu-id="23914-103">Legt die Speicherprofil Eigenschaften für VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="23914-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="23914-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23914-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23914-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23914-105">DESCRIPTION</span></span>
<span data-ttu-id="23914-106">Das Cmdlet " **Set-AzVmssStorageProfile** " legt die Speicherprofil Eigenschaften für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="23914-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="23914-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23914-107">EXAMPLES</span></span>

### <span data-ttu-id="23914-108">Beispiel 1: Einrichten der Speicherprofil Eigenschaften für das VMSS</span><span class="sxs-lookup"><span data-stu-id="23914-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="23914-109">Mit diesem Befehl werden die Speicherprofil Eigenschaften für das VMSS mit dem Namen ContosoVMSS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23914-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="23914-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="23914-110">PARAMETERS</span></span>

### <span data-ttu-id="23914-111">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="23914-111">-DataDisk</span></span>
<span data-ttu-id="23914-112">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="23914-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="23914-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23914-113">-DefaultProfile</span></span>
<span data-ttu-id="23914-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23914-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23914-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="23914-115">-DiffDiskSetting</span></span>
<span data-ttu-id="23914-116">Gibt die differenzierenden Datenträgereinstellungen für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="23914-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="23914-117">-Bild</span><span class="sxs-lookup"><span data-stu-id="23914-117">-Image</span></span>
<span data-ttu-id="23914-118">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="23914-118">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="23914-119">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.</span><span class="sxs-lookup"><span data-stu-id="23914-119">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="23914-120">-Imagereference-Nr</span><span class="sxs-lookup"><span data-stu-id="23914-120">-ImageReferenceId</span></span>
<span data-ttu-id="23914-121">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="23914-121">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="23914-122">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="23914-122">-ImageReferenceOffer</span></span>
<span data-ttu-id="23914-123">Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="23914-123">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="23914-124">Verwenden Sie das Get-AzVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23914-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="23914-125">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="23914-125">-ImageReferencePublisher</span></span>
<span data-ttu-id="23914-126">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="23914-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="23914-127">Verwenden Sie zum Abrufen eines Verlegers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23914-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="23914-128">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="23914-128">-ImageReferenceSku</span></span>
<span data-ttu-id="23914-129">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="23914-129">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="23914-130">Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23914-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="23914-131">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="23914-131">-ImageReferenceVersion</span></span>
<span data-ttu-id="23914-132">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="23914-132">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="23914-133">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="23914-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="23914-134">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="23914-134">-ManagedDisk</span></span>
<span data-ttu-id="23914-135">Gibt den verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="23914-135">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="23914-136">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="23914-136">-OsDiskCaching</span></span>
<span data-ttu-id="23914-137">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="23914-137">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="23914-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="23914-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="23914-139">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="23914-139">ReadOnly</span></span>
- <span data-ttu-id="23914-140">ReadWrite der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="23914-140">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="23914-141">Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="23914-141">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="23914-142">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="23914-142">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="23914-143">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="23914-143">-OsDiskCreateOption</span></span>
<span data-ttu-id="23914-144">Gibt an, wie dieses Cmdlet die virtuellen VMSS-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="23914-144">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="23914-145">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="23914-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="23914-146">Anfügen: dieser Wert wird verwendet, wenn Sie einen spezialisierten Datenträger zum Erstellen des virtuellen VMSS-Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="23914-146">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="23914-147">FromImage: dieser Wert wird verwendet, wenn Sie ein Bild zum Erstellen des VMSS-virtuellen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="23914-147">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="23914-148">Wenn Sie ein Platt Form Bild verwenden, wird auch der *imagereference* -Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="23914-148">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="23914-149">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="23914-149">-OsDiskName</span></span>
<span data-ttu-id="23914-150">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="23914-150">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="23914-151">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="23914-151">-OsDiskOsType</span></span>
<span data-ttu-id="23914-152">Gibt den Typ des Betriebssystems auf dem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="23914-152">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="23914-153">Dies ist nur für Benutzerbild Szenarien und nicht für ein Platt Form Bild erforderlich.</span><span class="sxs-lookup"><span data-stu-id="23914-153">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="23914-154">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="23914-154">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="23914-155">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="23914-155">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="23914-156">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="23914-156">-VhdContainer</span></span>
<span data-ttu-id="23914-157">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23914-157">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="23914-158">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="23914-158">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="23914-159">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="23914-159">Specifies the VMSS object.</span></span>
<span data-ttu-id="23914-160">Verwenden Sie das New-AzVmssConfig-Objekt, um das Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23914-160">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="23914-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23914-161">-Confirm</span></span>
<span data-ttu-id="23914-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23914-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23914-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23914-163">-WhatIf</span></span>
<span data-ttu-id="23914-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23914-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23914-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23914-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23914-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23914-166">CommonParameters</span></span>
<span data-ttu-id="23914-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23914-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23914-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23914-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23914-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23914-169">INPUTS</span></span>

### <span data-ttu-id="23914-170">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="23914-170">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="23914-171">System. String</span><span class="sxs-lookup"><span data-stu-id="23914-171">System.String</span></span>

### <span data-ttu-id="23914-172">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="23914-172">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="23914-173">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="23914-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="23914-174">System. String []</span><span class="sxs-lookup"><span data-stu-id="23914-174">System.String[]</span></span>

### <span data-ttu-id="23914-175">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="23914-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="23914-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23914-176">OUTPUTS</span></span>

### <span data-ttu-id="23914-177">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="23914-177">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="23914-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="23914-178">NOTES</span></span>

## <span data-ttu-id="23914-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23914-179">RELATED LINKS</span></span>

[<span data-ttu-id="23914-180">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="23914-180">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="23914-181">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="23914-181">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="23914-182">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="23914-182">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="23914-183">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="23914-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


