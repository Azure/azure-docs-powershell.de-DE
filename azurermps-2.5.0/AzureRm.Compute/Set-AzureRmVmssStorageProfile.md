---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssstorageprofile
schema: 2.0.0
ms.openlocfilehash: c96ff571ef1b82e52a313c2044a41b97d46ffa0b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849360"
---
# <span data-ttu-id="43b9c-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="43b9c-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="43b9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="43b9c-103">Legt die Speicherprofil Eigenschaften für VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="43b9c-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43b9c-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43b9c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="43b9c-106">Das Cmdlet " **Set-AzureRmVmssStorageProfile** " legt die Speicherprofil Eigenschaften für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="43b9c-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="43b9c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43b9c-107">EXAMPLES</span></span>

### <span data-ttu-id="43b9c-108">Beispiel 1: Einrichten der Speicherprofil Eigenschaften für das VMSS</span><span class="sxs-lookup"><span data-stu-id="43b9c-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="43b9c-109">Mit diesem Befehl werden die Speicherprofil Eigenschaften für das VMSS mit dem Namen ContosoVMSS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="43b9c-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="43b9c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="43b9c-110">PARAMETERS</span></span>

### <span data-ttu-id="43b9c-111">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="43b9c-111">-DataDisk</span></span>
<span data-ttu-id="43b9c-112">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="43b9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b9c-113">-DefaultProfile</span></span>
<span data-ttu-id="43b9c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43b9c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b9c-115">-Bild</span><span class="sxs-lookup"><span data-stu-id="43b9c-115">-Image</span></span>
<span data-ttu-id="43b9c-116">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="43b9c-117">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.</span><span class="sxs-lookup"><span data-stu-id="43b9c-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="43b9c-118">-Imagereference-Nr</span><span class="sxs-lookup"><span data-stu-id="43b9c-118">-ImageReferenceId</span></span>
<span data-ttu-id="43b9c-119">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="43b9c-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="43b9c-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="43b9c-121">Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="43b9c-122">Verwenden Sie das Get-AzureRmVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43b9c-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="43b9c-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="43b9c-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="43b9c-124">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="43b9c-125">Verwenden Sie zum Abrufen eines Verlegers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43b9c-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="43b9c-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="43b9c-126">-ImageReferenceSku</span></span>
<span data-ttu-id="43b9c-127">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="43b9c-128">Verwenden Sie zum Abrufen von SKUs das Get-AzureRmVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43b9c-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="43b9c-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="43b9c-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="43b9c-130">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="43b9c-131">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="43b9c-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="43b9c-132">-ManagedDisk</span></span>
<span data-ttu-id="43b9c-133">Gibt den verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-133">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="43b9c-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="43b9c-134">-OsDiskCaching</span></span>
<span data-ttu-id="43b9c-135">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="43b9c-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="43b9c-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43b9c-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="43b9c-137">ReadOnly</span></span>
- <span data-ttu-id="43b9c-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="43b9c-138">ReadWrite</span></span>

<span data-ttu-id="43b9c-139">Der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="43b9c-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="43b9c-140">Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="43b9c-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="43b9c-141">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="43b9c-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="43b9c-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="43b9c-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="43b9c-143">Gibt an, wie dieses Cmdlet die virtuellen VMSS-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="43b9c-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="43b9c-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="43b9c-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43b9c-145">Anfügen: dieser Wert wird verwendet, wenn Sie einen spezialisierten Datenträger zum Erstellen des virtuellen VMSS-Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="43b9c-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="43b9c-146">FromImage: dieser Wert wird verwendet, wenn Sie ein Bild zum Erstellen des VMSS-virtuellen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="43b9c-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="43b9c-147">Wenn Sie ein Platt Form Bild verwenden, wird auch der *imagereference* -Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="43b9c-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="43b9c-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="43b9c-148">-OsDiskName</span></span>
<span data-ttu-id="43b9c-149">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-149">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b9c-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="43b9c-150">-OsDiskOsType</span></span>
<span data-ttu-id="43b9c-151">Gibt den Typ des Betriebssystems auf dem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="43b9c-152">Dies ist nur für Benutzerbild Szenarien und nicht für ein Platt Form Bild erforderlich.</span><span class="sxs-lookup"><span data-stu-id="43b9c-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="43b9c-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="43b9c-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="43b9c-154">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="43b9c-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="43b9c-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="43b9c-155">-VhdContainer</span></span>
<span data-ttu-id="43b9c-156">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43b9c-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="43b9c-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="43b9c-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="43b9c-158">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="43b9c-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="43b9c-159">Verwenden Sie das New-AzureRmVmssConfig-Objekt, um das Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43b9c-159">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43b9c-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43b9c-160">-Confirm</span></span>
<span data-ttu-id="43b9c-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43b9c-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43b9c-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43b9c-162">-WhatIf</span></span>
<span data-ttu-id="43b9c-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43b9c-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43b9c-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43b9c-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43b9c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b9c-165">CommonParameters</span></span>
<span data-ttu-id="43b9c-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b9c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b9c-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43b9c-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b9c-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43b9c-168">INPUTS</span></span>

###  
<span data-ttu-id="43b9c-169">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="43b9c-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="43b9c-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43b9c-170">OUTPUTS</span></span>

### <span data-ttu-id="43b9c-171">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="43b9c-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="43b9c-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="43b9c-172">NOTES</span></span>

## <span data-ttu-id="43b9c-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43b9c-173">RELATED LINKS</span></span>

[<span data-ttu-id="43b9c-174">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="43b9c-174">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="43b9c-175">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="43b9c-175">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="43b9c-176">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="43b9c-176">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="43b9c-177">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="43b9c-177">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


