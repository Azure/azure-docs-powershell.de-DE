---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageVersion.md
ms.openlocfilehash: e8c50ffb2ac60c65f64806781d9155600c9bbe0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663194"
---
# <span data-ttu-id="3cf4d-101">Update-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3cf4d-101">Update-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="3cf4d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cf4d-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf4d-103">Aktualisieren einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-103">Update a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cf4d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cf4d-104">SYNTAX</span></span>

### <span data-ttu-id="3cf4d-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cf4d-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cf4d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3cf4d-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageVersion [-ResourceId] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cf4d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3cf4d-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob] [-Tag <Hashtable>]
 [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cf4d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cf4d-108">DESCRIPTION</span></span>
<span data-ttu-id="3cf4d-109">Aktualisieren einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-109">Update a gallery image version.</span></span>

## <span data-ttu-id="3cf4d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cf4d-110">EXAMPLES</span></span>

### <span data-ttu-id="3cf4d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3cf4d-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="3cf4d-112">Aktualisieren einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-112">Update a gallery image version.</span></span>

## <span data-ttu-id="3cf4d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cf4d-113">PARAMETERS</span></span>

### <span data-ttu-id="3cf4d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cf4d-114">-AsJob</span></span>
<span data-ttu-id="3cf4d-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3cf4d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cf4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf4d-116">-DefaultProfile</span></span>
<span data-ttu-id="3cf4d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf4d-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3cf4d-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="3cf4d-119">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="3cf4d-120">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="3cf4d-120">-GalleryName</span></span>
<span data-ttu-id="3cf4d-121">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="3cf4d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3cf4d-122">-InputObject</span></span>
<span data-ttu-id="3cf4d-123">Das Version-Objekt des PS Gallery-Bilds</span><span class="sxs-lookup"><span data-stu-id="3cf4d-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="3cf4d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3cf4d-124">-Name</span></span>
<span data-ttu-id="3cf4d-125">Der Name der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="3cf4d-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="3cf4d-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="3cf4d-127">Das Ende des Lebenszyklus der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="3cf4d-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="3cf4d-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="3cf4d-129">Wenn diese Einstellung festgesetzt ist, verwenden virtuelle Computer, die von der neuesten Version der Bild Definition bereitgestellt werden, nicht diese Bildversion.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="3cf4d-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3cf4d-130">-ReplicaCount</span></span>
<span data-ttu-id="3cf4d-131">Die Anzahl der Replikate der Bild Version, die pro Region erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="3cf4d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf4d-132">-ResourceGroupName</span></span>
<span data-ttu-id="3cf4d-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="3cf4d-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3cf4d-134">-ResourceId</span></span>
<span data-ttu-id="3cf4d-135">Die Ressourcen-ID für die Katalogbild Version.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="3cf4d-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="3cf4d-136">-Tag</span></span>
<span data-ttu-id="3cf4d-137">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="3cf4d-137">Resource tags</span></span>

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

### <span data-ttu-id="3cf4d-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="3cf4d-138">-TargetRegion</span></span>
<span data-ttu-id="3cf4d-139">Die Ziel Regionen, in die die Bild Version repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="3cf4d-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cf4d-140">-Confirm</span></span>
<span data-ttu-id="3cf4d-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf4d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf4d-142">-WhatIf</span></span>
<span data-ttu-id="3cf4d-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf4d-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf4d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf4d-145">CommonParameters</span></span>
<span data-ttu-id="3cf4d-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf4d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf4d-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf4d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf4d-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cf4d-148">INPUTS</span></span>

### <span data-ttu-id="3cf4d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf4d-149">System.String</span></span>

### <span data-ttu-id="3cf4d-150">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3cf4d-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="3cf4d-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3cf4d-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3cf4d-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3cf4d-152">System.Int32</span></span>

### <span data-ttu-id="3cf4d-153">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="3cf4d-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3cf4d-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="3cf4d-154">System.DateTime</span></span>

### <span data-ttu-id="3cf4d-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="3cf4d-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="3cf4d-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cf4d-156">OUTPUTS</span></span>

### <span data-ttu-id="3cf4d-157">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3cf4d-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="3cf4d-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cf4d-158">NOTES</span></span>

## <span data-ttu-id="3cf4d-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cf4d-159">RELATED LINKS</span></span>
