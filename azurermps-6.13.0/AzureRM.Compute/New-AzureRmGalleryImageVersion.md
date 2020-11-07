---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
ms.openlocfilehash: f27c861386e7a570fe72a5266362bee7fed39e5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664892"
---
# <span data-ttu-id="61ddf-101">New-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="61ddf-101">New-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="61ddf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="61ddf-103">Erstellen Sie eine Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="61ddf-103">Create a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61ddf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61ddf-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ddf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61ddf-105">DESCRIPTION</span></span>
<span data-ttu-id="61ddf-106">Erstellen Sie eine Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="61ddf-106">Create a gallery image version.</span></span>

## <span data-ttu-id="61ddf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61ddf-107">EXAMPLES</span></span>

### <span data-ttu-id="61ddf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61ddf-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="61ddf-109">Erstellen Sie eine Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="61ddf-109">Create a gallery image version.</span></span>

## <span data-ttu-id="61ddf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="61ddf-110">PARAMETERS</span></span>

### <span data-ttu-id="61ddf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61ddf-111">-AsJob</span></span>
<span data-ttu-id="61ddf-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="61ddf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61ddf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ddf-113">-DefaultProfile</span></span>
<span data-ttu-id="61ddf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61ddf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ddf-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="61ddf-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="61ddf-116">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="61ddf-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="61ddf-117">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="61ddf-117">-GalleryName</span></span>
<span data-ttu-id="61ddf-118">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="61ddf-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="61ddf-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="61ddf-119">-Location</span></span>
<span data-ttu-id="61ddf-120">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="61ddf-120">Resource location</span></span>

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

### <span data-ttu-id="61ddf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="61ddf-121">-Name</span></span>
<span data-ttu-id="61ddf-122">Der Name der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="61ddf-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="61ddf-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="61ddf-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="61ddf-124">Das Ende des Lebenszyklus der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="61ddf-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="61ddf-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="61ddf-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="61ddf-126">Wenn diese Einstellung festgesetzt ist, verwenden virtuelle Computer, die von der neuesten Version der Bild Definition bereitgestellt werden, nicht diese Bildversion.</span><span class="sxs-lookup"><span data-stu-id="61ddf-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="61ddf-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="61ddf-127">-ReplicaCount</span></span>
<span data-ttu-id="61ddf-128">Die Anzahl der Replikate der Bild Version, die pro Region erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="61ddf-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="61ddf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ddf-129">-ResourceGroupName</span></span>
<span data-ttu-id="61ddf-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="61ddf-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="61ddf-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="61ddf-131">-SourceImageId</span></span>
<span data-ttu-id="61ddf-132">Die ID des Quellbilds, aus dem die Bild Version erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="61ddf-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="61ddf-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="61ddf-133">-Tag</span></span>
<span data-ttu-id="61ddf-134">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="61ddf-134">Resource tags</span></span>

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

### <span data-ttu-id="61ddf-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="61ddf-135">-TargetRegion</span></span>
<span data-ttu-id="61ddf-136">Die Ziel Regionen, in die die Bild Version repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="61ddf-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="61ddf-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61ddf-137">-Confirm</span></span>
<span data-ttu-id="61ddf-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61ddf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ddf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ddf-139">-WhatIf</span></span>
<span data-ttu-id="61ddf-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61ddf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61ddf-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61ddf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61ddf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ddf-142">CommonParameters</span></span>
<span data-ttu-id="61ddf-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ddf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ddf-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61ddf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ddf-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61ddf-145">INPUTS</span></span>

### <span data-ttu-id="61ddf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="61ddf-146">System.String</span></span>

### <span data-ttu-id="61ddf-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="61ddf-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="61ddf-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="61ddf-148">System.Int32</span></span>

### <span data-ttu-id="61ddf-149">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="61ddf-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="61ddf-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="61ddf-150">System.DateTime</span></span>

### <span data-ttu-id="61ddf-151">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="61ddf-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="61ddf-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61ddf-152">OUTPUTS</span></span>

### <span data-ttu-id="61ddf-153">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="61ddf-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="61ddf-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="61ddf-154">NOTES</span></span>

## <span data-ttu-id="61ddf-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61ddf-155">RELATED LINKS</span></span>
