---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 6d708689c4156cb01e950490314d7fdd2a88b67c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928328"
---
# <span data-ttu-id="e6e7b-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e6e7b-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="e6e7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e7b-103">Aktualisieren einer Katalogbildversion</span><span class="sxs-lookup"><span data-stu-id="e6e7b-103">Update a gallery image version.</span></span>

## <span data-ttu-id="e6e7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6e7b-104">SYNTAX</span></span>

### <span data-ttu-id="e6e7b-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6e7b-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6e7b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e6e7b-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6e7b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e6e7b-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e7b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6e7b-108">DESCRIPTION</span></span>
<span data-ttu-id="e6e7b-109">Aktualisieren einer Katalogbildversion</span><span class="sxs-lookup"><span data-stu-id="e6e7b-109">Update a gallery image version.</span></span>

## <span data-ttu-id="e6e7b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6e7b-110">EXAMPLES</span></span>

### <span data-ttu-id="e6e7b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6e7b-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="e6e7b-112">Aktualisieren einer Katalogbildversion</span><span class="sxs-lookup"><span data-stu-id="e6e7b-112">Update a gallery image version.</span></span>

## <span data-ttu-id="e6e7b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e6e7b-113">PARAMETERS</span></span>

### <span data-ttu-id="e6e7b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6e7b-114">-AsJob</span></span>
<span data-ttu-id="e6e7b-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e6e7b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6e7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e7b-116">-DefaultProfile</span></span>
<span data-ttu-id="e6e7b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6e7b-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="e6e7b-119">Der Name der Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-119">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-120">-GalleryName</span></span>
<span data-ttu-id="e6e7b-121">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6e7b-122">-InputObject</span></span>
<span data-ttu-id="e6e7b-123">Das PS Gallery Image Version Object.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-123">The PS Gallery Image Version Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e6e7b-124">-Name</span></span>
<span data-ttu-id="e6e7b-125">Der Name der Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-125">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="e6e7b-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="e6e7b-127">Das Datum des Lebenszyklus des Katalogs Bildversion.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="e6e7b-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="e6e7b-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="e6e7b-129">Wenn dies festgelegt ist, verwenden virtuelle Computer, die mit der neuesten Version der Bilddefinition bereitgestellt wurden, diese Bildversion nicht.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="e6e7b-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="e6e7b-130">-ReplicaCount</span></span>
<span data-ttu-id="e6e7b-131">Die Anzahl der Replikate der Bildversion, die pro Region erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="e6e7b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-132">-ResourceGroupName</span></span>
<span data-ttu-id="e6e7b-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6e7b-134">-ResourceId</span></span>
<span data-ttu-id="e6e7b-135">Die Ressourcen-ID für die Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-135">The resource ID for the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6e7b-136">-Tag</span></span>
<span data-ttu-id="e6e7b-137">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="e6e7b-137">Resource tags</span></span>

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

### <span data-ttu-id="e6e7b-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="e6e7b-138">-TargetRegion</span></span>
<span data-ttu-id="e6e7b-139">Die Zielregionen, in die die Bildversion repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="e6e7b-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6e7b-140">-Confirm</span></span>
<span data-ttu-id="e6e7b-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e7b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e7b-142">-WhatIf</span></span>
<span data-ttu-id="e6e7b-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e7b-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e7b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e7b-145">CommonParameters</span></span>
<span data-ttu-id="e6e7b-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e7b-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6e7b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e7b-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6e7b-148">INPUTS</span></span>

### <span data-ttu-id="e6e7b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="e6e7b-149">System.String</span></span>

### <span data-ttu-id="e6e7b-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e6e7b-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="e6e7b-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6e7b-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e6e7b-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e6e7b-152">System.Int32</span></span>

### <span data-ttu-id="e6e7b-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e6e7b-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e6e7b-154">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="e6e7b-154">System.DateTime</span></span>

### <span data-ttu-id="e6e7b-155">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="e6e7b-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="e6e7b-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6e7b-156">OUTPUTS</span></span>

### <span data-ttu-id="e6e7b-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e6e7b-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="e6e7b-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e6e7b-158">NOTES</span></span>

## <span data-ttu-id="e6e7b-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e6e7b-159">RELATED LINKS</span></span>
