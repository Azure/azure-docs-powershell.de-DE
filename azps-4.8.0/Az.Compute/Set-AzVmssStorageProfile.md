---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167114"
---
# <span data-ttu-id="02d2c-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="02d2c-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="02d2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="02d2c-103">Legt die Speicherprofil Eigenschaften für VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="02d2c-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="02d2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02d2c-104">SYNTAX</span></span>

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

## <span data-ttu-id="02d2c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="02d2c-106">Das Cmdlet " **Set-AzVmssStorageProfile** " legt die Speicherprofil Eigenschaften für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="02d2c-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="02d2c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02d2c-107">EXAMPLES</span></span>

### <span data-ttu-id="02d2c-108">Beispiel 1: Einrichten der Speicherprofil Eigenschaften für das VMSS</span><span class="sxs-lookup"><span data-stu-id="02d2c-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="02d2c-109">Mit diesem Befehl werden die Speicherprofil Eigenschaften für das VMSS mit dem Namen ContosoVMSS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02d2c-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="02d2c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="02d2c-110">PARAMETERS</span></span>

### <span data-ttu-id="02d2c-111">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="02d2c-111">-DataDisk</span></span>
<span data-ttu-id="02d2c-112">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="02d2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d2c-113">-DefaultProfile</span></span>
<span data-ttu-id="02d2c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02d2c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02d2c-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="02d2c-115">-DiffDiskSetting</span></span>
<span data-ttu-id="02d2c-116">Gibt die differenzierenden Datenträgereinstellungen für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="02d2c-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="02d2c-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="02d2c-118">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträger Verschlüsselungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="02d2c-119">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="02d2c-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="02d2c-120">-Bild</span><span class="sxs-lookup"><span data-stu-id="02d2c-120">-Image</span></span>
<span data-ttu-id="02d2c-121">Gibt den BLOB-URI für das Benutzerbild an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="02d2c-122">VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.</span><span class="sxs-lookup"><span data-stu-id="02d2c-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="02d2c-123">-Imagereference-Nr</span><span class="sxs-lookup"><span data-stu-id="02d2c-123">-ImageReferenceId</span></span>
<span data-ttu-id="02d2c-124">Gibt die Bildreferenz-ID an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="02d2c-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="02d2c-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="02d2c-126">Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="02d2c-127">Verwenden Sie das Get-AzVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="02d2c-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="02d2c-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="02d2c-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="02d2c-129">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="02d2c-130">Verwenden Sie zum Abrufen eines Verlegers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d2c-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="02d2c-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="02d2c-131">-ImageReferenceSku</span></span>
<span data-ttu-id="02d2c-132">Gibt die VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="02d2c-133">Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d2c-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="02d2c-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="02d2c-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="02d2c-135">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="02d2c-136">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="02d2c-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="02d2c-137">-ManagedDisk</span></span>
<span data-ttu-id="02d2c-138">Gibt den verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="02d2c-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="02d2c-139">-OsDiskCaching</span></span>
<span data-ttu-id="02d2c-140">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="02d2c-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="02d2c-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="02d2c-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="02d2c-142">ReadOnly</span></span>
- <span data-ttu-id="02d2c-143">ReadWrite der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="02d2c-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="02d2c-144">Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="02d2c-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="02d2c-145">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="02d2c-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="02d2c-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="02d2c-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="02d2c-147">Gibt an, wie dieses Cmdlet die virtuellen VMSS-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="02d2c-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="02d2c-148">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="02d2c-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="02d2c-149">Anfügen: dieser Wert wird verwendet, wenn Sie einen spezialisierten Datenträger zum Erstellen des virtuellen VMSS-Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="02d2c-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="02d2c-150">FromImage: dieser Wert wird verwendet, wenn Sie ein Bild zum Erstellen des VMSS-virtuellen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="02d2c-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="02d2c-151">Wenn Sie ein Platt Form Bild verwenden, wird auch der *imagereference* -Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="02d2c-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="02d2c-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="02d2c-152">-OsDiskName</span></span>
<span data-ttu-id="02d2c-153">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="02d2c-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="02d2c-154">-OsDiskOsType</span></span>
<span data-ttu-id="02d2c-155">Gibt den Typ des Betriebssystems auf dem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="02d2c-156">Dies ist nur für Benutzerbild Szenarien und nicht für ein Platt Form Bild erforderlich.</span><span class="sxs-lookup"><span data-stu-id="02d2c-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="02d2c-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="02d2c-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="02d2c-158">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="02d2c-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="02d2c-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="02d2c-159">-VhdContainer</span></span>
<span data-ttu-id="02d2c-160">Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02d2c-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="02d2c-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="02d2c-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="02d2c-162">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="02d2c-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="02d2c-163">Verwenden Sie das New-AzVmssConfig-Objekt, um das Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="02d2c-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="02d2c-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02d2c-164">-Confirm</span></span>
<span data-ttu-id="02d2c-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02d2c-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02d2c-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02d2c-166">-WhatIf</span></span>
<span data-ttu-id="02d2c-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02d2c-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02d2c-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02d2c-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02d2c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d2c-169">CommonParameters</span></span>
<span data-ttu-id="02d2c-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d2c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d2c-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02d2c-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d2c-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02d2c-172">INPUTS</span></span>

### <span data-ttu-id="02d2c-173">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="02d2c-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="02d2c-174">System. String</span><span class="sxs-lookup"><span data-stu-id="02d2c-174">System.String</span></span>

### <span data-ttu-id="02d2c-175">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="02d2c-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="02d2c-176">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="02d2c-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="02d2c-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="02d2c-177">System.String[]</span></span>

### <span data-ttu-id="02d2c-178">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="02d2c-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="02d2c-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02d2c-179">OUTPUTS</span></span>

### <span data-ttu-id="02d2c-180">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="02d2c-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="02d2c-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="02d2c-181">NOTES</span></span>

## <span data-ttu-id="02d2c-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02d2c-182">RELATED LINKS</span></span>

[<span data-ttu-id="02d2c-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="02d2c-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="02d2c-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="02d2c-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="02d2c-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="02d2c-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="02d2c-186">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="02d2c-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


