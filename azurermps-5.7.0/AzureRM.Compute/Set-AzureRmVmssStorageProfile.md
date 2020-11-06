---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 26f61261bd8fd1c2d5fc2bbdacec71f73db91fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498997"
---
# <span data-ttu-id="4142b-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="4142b-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="4142b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4142b-102">SYNOPSIS</span></span>
<span data-ttu-id="4142b-103">Legt die Speicherprofil Eigenschaften für VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="4142b-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4142b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4142b-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [-OsDiskName <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4142b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4142b-105">DESCRIPTION</span></span>
<span data-ttu-id="4142b-106">Das Cmdlet " **Set-AzureRmVmssStorageProfile** " legt die Speicherprofil Eigenschaften für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4142b-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4142b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4142b-107">EXAMPLES</span></span>

### <span data-ttu-id="4142b-108">Beispiel 1: Einrichten der Speicherprofil Eigenschaften für das VMSS</span><span class="sxs-lookup"><span data-stu-id="4142b-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="4142b-109">Mit diesem Befehl werden die Speicherprofil Eigenschaften für das VMSS mit dem Namen ContosoVMSS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4142b-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="4142b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4142b-110">PARAMETERS</span></span>

### <span data-ttu-id="4142b-111">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="4142b-111">-DataDisk</span></span>
<span data-ttu-id="4142b-112">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="4142b-112">Specifies the data disk object.</span></span>

```yaml
Type: VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-113">-Bild</span><span class="sxs-lookup"><span data-stu-id="4142b-113">-Image</span></span>
<span data-ttu-id="4142b-114">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="4142b-114">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="4142b-115">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.</span><span class="sxs-lookup"><span data-stu-id="4142b-115">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-116">-Imagereference-Nr</span><span class="sxs-lookup"><span data-stu-id="4142b-116">-ImageReferenceId</span></span>
<span data-ttu-id="4142b-117">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="4142b-117">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="4142b-118">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="4142b-118">-ImageReferenceOffer</span></span>
<span data-ttu-id="4142b-119">Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="4142b-119">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="4142b-120">Verwenden Sie das Get-AzureRmVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4142b-120">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-121">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="4142b-121">-ImageReferencePublisher</span></span>
<span data-ttu-id="4142b-122">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="4142b-122">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="4142b-123">Verwenden Sie zum Abrufen eines Verlegers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4142b-123">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4142b-124">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="4142b-124">-ImageReferenceSku</span></span>
<span data-ttu-id="4142b-125">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="4142b-125">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="4142b-126">Verwenden Sie zum Abrufen von SKUs das Get-AzureRmVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4142b-126">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-127">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="4142b-127">-ImageReferenceVersion</span></span>
<span data-ttu-id="4142b-128">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="4142b-128">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="4142b-129">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="4142b-129">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="4142b-130">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="4142b-130">-ManagedDisk</span></span>
<span data-ttu-id="4142b-131">Gibt den verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="4142b-131">Specifies the managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-132">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="4142b-132">-OsDiskCaching</span></span>
<span data-ttu-id="4142b-133">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4142b-133">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="4142b-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4142b-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4142b-135">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4142b-135">ReadOnly</span></span>
- <span data-ttu-id="4142b-136">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4142b-136">ReadWrite</span></span>

<span data-ttu-id="4142b-137">Der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="4142b-137">The default value is ReadWrite.</span></span>
<span data-ttu-id="4142b-138">Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="4142b-138">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="4142b-139">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="4142b-139">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-140">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="4142b-140">-OsDiskCreateOption</span></span>
<span data-ttu-id="4142b-141">Gibt an, wie dieses Cmdlet die virtuellen VMSS-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="4142b-141">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="4142b-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4142b-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4142b-143">Anfügen: dieser Wert wird verwendet, wenn Sie einen spezialisierten Datenträger zum Erstellen des virtuellen VMSS-Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="4142b-143">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="4142b-144">FromImage: dieser Wert wird verwendet, wenn Sie ein Bild zum Erstellen des VMSS-virtuellen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="4142b-144">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="4142b-145">Wenn Sie ein Platt Form Bild verwenden, wird auch der *imagereference* -Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="4142b-145">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-146">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="4142b-146">-OsDiskName</span></span>
<span data-ttu-id="4142b-147">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4142b-147">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-148">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="4142b-148">-OsDiskOsType</span></span>
<span data-ttu-id="4142b-149">Gibt den Typ des Betriebssystems auf dem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="4142b-149">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="4142b-150">Dies ist nur für Benutzerbild Szenarien und nicht für ein Platt Form Bild erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4142b-150">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-151">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="4142b-151">-VhdContainer</span></span>
<span data-ttu-id="4142b-152">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4142b-152">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-153">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4142b-153">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4142b-154">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4142b-154">Specifies the VMSS object.</span></span>
<span data-ttu-id="4142b-155">Verwenden Sie das New-AzureRmVmssConfig-Objekt, um das Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4142b-155">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4142b-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4142b-156">-Confirm</span></span>
<span data-ttu-id="4142b-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4142b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4142b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4142b-158">-WhatIf</span></span>
<span data-ttu-id="4142b-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4142b-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4142b-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4142b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4142b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4142b-161">CommonParameters</span></span>
<span data-ttu-id="4142b-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4142b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4142b-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4142b-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4142b-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4142b-164">INPUTS</span></span>

###  
<span data-ttu-id="4142b-165">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="4142b-165">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4142b-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4142b-166">OUTPUTS</span></span>

## <span data-ttu-id="4142b-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="4142b-167">NOTES</span></span>

## <span data-ttu-id="4142b-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4142b-168">RELATED LINKS</span></span>

[<span data-ttu-id="4142b-169">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4142b-169">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4142b-170">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4142b-170">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4142b-171">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4142b-171">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="4142b-172">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4142b-172">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


