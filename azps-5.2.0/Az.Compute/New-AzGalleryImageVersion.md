---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357019"
---
# <span data-ttu-id="d8dbc-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d8dbc-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="d8dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dbc-103">Erstellen Sie eine Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-103">Create a gallery image version.</span></span>

## <span data-ttu-id="d8dbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8dbc-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8dbc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8dbc-105">DESCRIPTION</span></span>
<span data-ttu-id="d8dbc-106">Erstellen Sie eine Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-106">Create a gallery image version.</span></span>

## <span data-ttu-id="d8dbc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8dbc-107">EXAMPLES</span></span>

### <span data-ttu-id="d8dbc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8dbc-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="d8dbc-109">Erstellen Sie eine Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-109">Create a gallery image version.</span></span>

### <span data-ttu-id="d8dbc-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d8dbc-110">Example 2</span></span>
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

<span data-ttu-id="d8dbc-111">Erstellen Sie eine Katalogbildversion mit Datenträgerbildverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="d8dbc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8dbc-112">PARAMETERS</span></span>

### <span data-ttu-id="d8dbc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8dbc-113">-AsJob</span></span>
<span data-ttu-id="d8dbc-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d8dbc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8dbc-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="d8dbc-115">-DataDiskImage</span></span>
<span data-ttu-id="d8dbc-116">Datenträgerbilder für Daten.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-116">Data disk images.</span></span>   <span data-ttu-id="d8dbc-117">z. B. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="d8dbc-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="d8dbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dbc-118">-DefaultProfile</span></span>
<span data-ttu-id="d8dbc-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8dbc-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d8dbc-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="d8dbc-121">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="d8dbc-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="d8dbc-122">-GalleryName</span></span>
<span data-ttu-id="d8dbc-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="d8dbc-124">-Location</span><span class="sxs-lookup"><span data-stu-id="d8dbc-124">-Location</span></span>
<span data-ttu-id="d8dbc-125">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="d8dbc-125">Resource location</span></span>

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

### <span data-ttu-id="d8dbc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d8dbc-126">-Name</span></span>
<span data-ttu-id="d8dbc-127">Der Name der Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="d8dbc-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="d8dbc-128">-OSDiskImage</span></span>
<span data-ttu-id="d8dbc-129">Abbild des Betriebssystemdatenträgers, z. B. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="d8dbc-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="d8dbc-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="d8dbc-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="d8dbc-131">Das Datum des Lebenszyklusendes der Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="d8dbc-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="d8dbc-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="d8dbc-133">Wenn dies festgelegt ist, wird diese Bildversion von virtuellen Computern, die mit der neuesten Version der Bilddefinition bereitgestellt wurden, nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="d8dbc-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="d8dbc-134">-ReplicaCount</span></span>
<span data-ttu-id="d8dbc-135">Die Anzahl der Replikate der Bildversion, die pro Region erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="d8dbc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dbc-136">-ResourceGroupName</span></span>
<span data-ttu-id="d8dbc-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8dbc-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="d8dbc-138">-SourceImageId</span></span>
<span data-ttu-id="d8dbc-139">Die ID des Quellbilds, aus dem die Bildversion erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="d8dbc-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d8dbc-140">-StorageAccountType</span></span>
<span data-ttu-id="d8dbc-141">Gibt den Speicherkontotyp an, der zum Speichern des Bilds verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="d8dbc-142">Diese Eigenschaft ist nicht updatable.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-142">This property is not updatable.</span></span> <span data-ttu-id="d8dbc-143">Verfügbare Werte sind Standard_LRS, Standard_ZRS und Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="d8dbc-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8dbc-144">-Tag</span></span>
<span data-ttu-id="d8dbc-145">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="d8dbc-145">Resource tags</span></span>

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

### <span data-ttu-id="d8dbc-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="d8dbc-146">-TargetRegion</span></span>
<span data-ttu-id="d8dbc-147">Die Zielbereiche, in die die Bildversion repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="d8dbc-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8dbc-148">-Confirm</span></span>
<span data-ttu-id="d8dbc-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8dbc-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d8dbc-150">-WhatIf</span></span>
<span data-ttu-id="d8dbc-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8dbc-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8dbc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dbc-153">CommonParameters</span></span>
<span data-ttu-id="d8dbc-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dbc-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8dbc-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dbc-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8dbc-156">INPUTS</span></span>

### <span data-ttu-id="d8dbc-157">System.String</span><span class="sxs-lookup"><span data-stu-id="d8dbc-157">System.String</span></span>

### <span data-ttu-id="d8dbc-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8dbc-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d8dbc-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d8dbc-159">System.Int32</span></span>

### <span data-ttu-id="d8dbc-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d8dbc-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d8dbc-161">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="d8dbc-161">System.DateTime</span></span>

### <span data-ttu-id="d8dbc-162">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="d8dbc-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="d8dbc-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8dbc-163">OUTPUTS</span></span>

### <span data-ttu-id="d8dbc-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d8dbc-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="d8dbc-165">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d8dbc-165">NOTES</span></span>

## <span data-ttu-id="d8dbc-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d8dbc-166">RELATED LINKS</span></span>
