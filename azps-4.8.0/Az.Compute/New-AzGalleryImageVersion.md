---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009329"
---
# <span data-ttu-id="348da-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="348da-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="348da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="348da-102">SYNOPSIS</span></span>
<span data-ttu-id="348da-103">Erstellen Sie eine Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="348da-103">Create a gallery image version.</span></span>

## <span data-ttu-id="348da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="348da-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="348da-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="348da-105">DESCRIPTION</span></span>
<span data-ttu-id="348da-106">Erstellen Sie eine Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="348da-106">Create a gallery image version.</span></span>

## <span data-ttu-id="348da-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="348da-107">EXAMPLES</span></span>

### <span data-ttu-id="348da-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="348da-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="348da-109">Erstellen Sie eine Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="348da-109">Create a gallery image version.</span></span>

### <span data-ttu-id="348da-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="348da-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="348da-111">Erstellen Sie eine Katalogbild Version mit Datenträger Bildverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="348da-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="348da-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="348da-112">PARAMETERS</span></span>

### <span data-ttu-id="348da-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="348da-113">-AsJob</span></span>
<span data-ttu-id="348da-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="348da-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="348da-115">-Datadiskimage</span><span class="sxs-lookup"><span data-stu-id="348da-115">-DataDiskImage</span></span>
<span data-ttu-id="348da-116">Datenträger Bilder.</span><span class="sxs-lookup"><span data-stu-id="348da-116">Data disk images.</span></span>   <span data-ttu-id="348da-117">z.b. @ {Source = @ {ID =<source_id>}; LUN = 1; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="348da-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348da-118">-DefaultProfile</span></span>
<span data-ttu-id="348da-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="348da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="348da-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="348da-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="348da-121">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="348da-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348da-122">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="348da-122">-GalleryName</span></span>
<span data-ttu-id="348da-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="348da-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="348da-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="348da-124">-Location</span></span>
<span data-ttu-id="348da-125">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="348da-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348da-126">-Name</span><span class="sxs-lookup"><span data-stu-id="348da-126">-Name</span></span>
<span data-ttu-id="348da-127">Der Name der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="348da-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348da-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="348da-128">-OSDiskImage</span></span>
<span data-ttu-id="348da-129">OS-Datenträgerabbildung, beispielsweise @ {Source = @ {ID =<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="348da-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348da-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="348da-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="348da-131">Das Ende des Lebenszyklus der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="348da-131">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348da-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="348da-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="348da-133">Wenn diese Einstellung festgesetzt ist, verwenden virtuelle Computer, die von der neuesten Version der Bild Definition bereitgestellt werden, nicht diese Bildversion.</span><span class="sxs-lookup"><span data-stu-id="348da-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348da-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="348da-134">-ReplicaCount</span></span>
<span data-ttu-id="348da-135">Die Anzahl der Replikate der Bild Version, die pro Region erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="348da-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="348da-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="348da-136">-ResourceGroupName</span></span>
<span data-ttu-id="348da-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="348da-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="348da-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="348da-138">-SourceImageId</span></span>
<span data-ttu-id="348da-139">Die ID des Quellbilds, aus dem die Bild Version erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="348da-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="348da-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="348da-140">-StorageAccountType</span></span>
<span data-ttu-id="348da-141">Gibt den Speicher Kontotyp an, der zum Speichern des Bilds verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="348da-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="348da-142">Diese Eigenschaft kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="348da-142">This property is not updatable.</span></span> <span data-ttu-id="348da-143">Verfügbare Werte sind Standard_LRS, Standard_ZRS und Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="348da-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="348da-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="348da-144">-Tag</span></span>
<span data-ttu-id="348da-145">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="348da-145">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348da-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="348da-146">-TargetRegion</span></span>
<span data-ttu-id="348da-147">Die Ziel Regionen, in die die Bild Version repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="348da-147">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348da-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="348da-148">-Confirm</span></span>
<span data-ttu-id="348da-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="348da-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="348da-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="348da-150">-WhatIf</span></span>
<span data-ttu-id="348da-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="348da-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="348da-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="348da-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="348da-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348da-153">CommonParameters</span></span>
<span data-ttu-id="348da-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="348da-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348da-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="348da-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348da-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="348da-156">INPUTS</span></span>

### <span data-ttu-id="348da-157">System. String</span><span class="sxs-lookup"><span data-stu-id="348da-157">System.String</span></span>

### <span data-ttu-id="348da-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="348da-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="348da-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="348da-159">System.Int32</span></span>

### <span data-ttu-id="348da-160">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="348da-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="348da-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="348da-161">System.DateTime</span></span>

### <span data-ttu-id="348da-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="348da-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="348da-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="348da-163">OUTPUTS</span></span>

### <span data-ttu-id="348da-164">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="348da-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="348da-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="348da-165">NOTES</span></span>

## <span data-ttu-id="348da-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="348da-166">RELATED LINKS</span></span>
