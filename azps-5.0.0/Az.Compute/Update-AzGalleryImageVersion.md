---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296422"
---
# <span data-ttu-id="1a46e-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1a46e-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="1a46e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a46e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a46e-103">Aktualisieren einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="1a46e-103">Update a gallery image version.</span></span>

## <span data-ttu-id="1a46e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a46e-104">SYNTAX</span></span>

### <span data-ttu-id="1a46e-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a46e-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a46e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1a46e-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a46e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1a46e-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a46e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a46e-108">DESCRIPTION</span></span>
<span data-ttu-id="1a46e-109">Aktualisieren einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="1a46e-109">Update a gallery image version.</span></span>

## <span data-ttu-id="1a46e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a46e-110">EXAMPLES</span></span>

### <span data-ttu-id="1a46e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a46e-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="1a46e-112">Aktualisieren einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="1a46e-112">Update a gallery image version.</span></span>

## <span data-ttu-id="1a46e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a46e-113">PARAMETERS</span></span>

### <span data-ttu-id="1a46e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a46e-114">-AsJob</span></span>
<span data-ttu-id="1a46e-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1a46e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a46e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a46e-116">-DefaultProfile</span></span>
<span data-ttu-id="1a46e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a46e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a46e-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="1a46e-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="1a46e-119">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="1a46e-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="1a46e-120">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="1a46e-120">-GalleryName</span></span>
<span data-ttu-id="1a46e-121">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="1a46e-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="1a46e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1a46e-122">-InputObject</span></span>
<span data-ttu-id="1a46e-123">Das Version-Objekt des PS Gallery-Bilds</span><span class="sxs-lookup"><span data-stu-id="1a46e-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="1a46e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1a46e-124">-Name</span></span>
<span data-ttu-id="1a46e-125">Der Name der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="1a46e-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="1a46e-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="1a46e-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="1a46e-127">Das Ende des Lebenszyklus der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="1a46e-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="1a46e-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="1a46e-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="1a46e-129">Wenn diese Einstellung festgesetzt ist, verwenden virtuelle Computer, die von der neuesten Version der Bild Definition bereitgestellt werden, nicht diese Bildversion.</span><span class="sxs-lookup"><span data-stu-id="1a46e-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="1a46e-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="1a46e-130">-ReplicaCount</span></span>
<span data-ttu-id="1a46e-131">Die Anzahl der Replikate der Bild Version, die pro Region erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a46e-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="1a46e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a46e-132">-ResourceGroupName</span></span>
<span data-ttu-id="1a46e-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1a46e-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="1a46e-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1a46e-134">-ResourceId</span></span>
<span data-ttu-id="1a46e-135">Die Ressourcen-ID für die Katalogbild Version.</span><span class="sxs-lookup"><span data-stu-id="1a46e-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="1a46e-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="1a46e-136">-Tag</span></span>
<span data-ttu-id="1a46e-137">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="1a46e-137">Resource tags</span></span>

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

### <span data-ttu-id="1a46e-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="1a46e-138">-TargetRegion</span></span>
<span data-ttu-id="1a46e-139">Die Ziel Regionen, in die die Bild Version repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a46e-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="1a46e-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a46e-140">-Confirm</span></span>
<span data-ttu-id="1a46e-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a46e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a46e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a46e-142">-WhatIf</span></span>
<span data-ttu-id="1a46e-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a46e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a46e-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a46e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a46e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a46e-145">CommonParameters</span></span>
<span data-ttu-id="1a46e-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a46e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a46e-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a46e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a46e-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a46e-148">INPUTS</span></span>

### <span data-ttu-id="1a46e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1a46e-149">System.String</span></span>

### <span data-ttu-id="1a46e-150">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1a46e-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="1a46e-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1a46e-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1a46e-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1a46e-152">System.Int32</span></span>

### <span data-ttu-id="1a46e-153">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="1a46e-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1a46e-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="1a46e-154">System.DateTime</span></span>

### <span data-ttu-id="1a46e-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="1a46e-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="1a46e-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a46e-156">OUTPUTS</span></span>

### <span data-ttu-id="1a46e-157">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1a46e-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="1a46e-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a46e-158">NOTES</span></span>

## <span data-ttu-id="1a46e-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a46e-159">RELATED LINKS</span></span>
