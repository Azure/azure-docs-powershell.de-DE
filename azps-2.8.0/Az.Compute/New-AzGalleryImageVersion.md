---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 80536a8bfce32d713649f3feab4d77b1662206b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652079"
---
# <span data-ttu-id="404df-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="404df-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="404df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="404df-102">SYNOPSIS</span></span>
<span data-ttu-id="404df-103">Erstellen Sie eine Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="404df-103">Create a gallery image version.</span></span>

## <span data-ttu-id="404df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="404df-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-StorageAccountType <String>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="404df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="404df-105">DESCRIPTION</span></span>
<span data-ttu-id="404df-106">Erstellen Sie eine Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="404df-106">Create a gallery image version.</span></span>

## <span data-ttu-id="404df-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="404df-107">EXAMPLES</span></span>

### <span data-ttu-id="404df-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="404df-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="404df-109">Erstellen Sie eine Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="404df-109">Create a gallery image version.</span></span>

## <span data-ttu-id="404df-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="404df-110">PARAMETERS</span></span>

### <span data-ttu-id="404df-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="404df-111">-AsJob</span></span>
<span data-ttu-id="404df-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="404df-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="404df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="404df-113">-DefaultProfile</span></span>
<span data-ttu-id="404df-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="404df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="404df-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="404df-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="404df-116">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="404df-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="404df-117">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="404df-117">-GalleryName</span></span>
<span data-ttu-id="404df-118">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="404df-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="404df-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="404df-119">-Location</span></span>
<span data-ttu-id="404df-120">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="404df-120">Resource location</span></span>

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

### <span data-ttu-id="404df-121">-Name</span><span class="sxs-lookup"><span data-stu-id="404df-121">-Name</span></span>
<span data-ttu-id="404df-122">Der Name der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="404df-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="404df-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="404df-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="404df-124">Das Ende des Lebenszyklus der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="404df-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="404df-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="404df-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="404df-126">Wenn diese Einstellung festgesetzt ist, verwenden virtuelle Computer, die von der neuesten Version der Bild Definition bereitgestellt werden, nicht diese Bildversion.</span><span class="sxs-lookup"><span data-stu-id="404df-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="404df-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="404df-127">-ReplicaCount</span></span>
<span data-ttu-id="404df-128">Die Anzahl der Replikate der Bild Version, die pro Region erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="404df-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="404df-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="404df-129">-ResourceGroupName</span></span>
<span data-ttu-id="404df-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="404df-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="404df-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="404df-131">-SourceImageId</span></span>
<span data-ttu-id="404df-132">Die ID des Quellbilds, aus dem die Bild Version erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="404df-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="404df-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="404df-133">-StorageAccountType</span></span>
<span data-ttu-id="404df-134">Gibt den Speicher Kontotyp an, der zum Speichern des Bilds verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="404df-134">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="404df-135">Diese Eigenschaft kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="404df-135">This property is not updatable.</span></span> <span data-ttu-id="404df-136">Verfügbare Werte sind Standard_LRS und Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="404df-136">Available values are Standard_LRS and Standard_ZRS.</span></span>

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

### <span data-ttu-id="404df-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="404df-137">-Tag</span></span>
<span data-ttu-id="404df-138">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="404df-138">Resource tags</span></span>

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

### <span data-ttu-id="404df-139">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="404df-139">-TargetRegion</span></span>
<span data-ttu-id="404df-140">Die Ziel Regionen, in die die Bild Version repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="404df-140">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="404df-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="404df-141">-Confirm</span></span>
<span data-ttu-id="404df-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="404df-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="404df-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="404df-143">-WhatIf</span></span>
<span data-ttu-id="404df-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="404df-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="404df-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="404df-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="404df-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404df-146">CommonParameters</span></span>
<span data-ttu-id="404df-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404df-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404df-148">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="404df-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404df-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="404df-149">INPUTS</span></span>

### <span data-ttu-id="404df-150">System. String</span><span class="sxs-lookup"><span data-stu-id="404df-150">System.String</span></span>

### <span data-ttu-id="404df-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="404df-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="404df-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="404df-152">System.Int32</span></span>

### <span data-ttu-id="404df-153">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="404df-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="404df-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="404df-154">System.DateTime</span></span>

### <span data-ttu-id="404df-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="404df-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="404df-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="404df-156">OUTPUTS</span></span>

### <span data-ttu-id="404df-157">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="404df-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="404df-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="404df-158">NOTES</span></span>

## <span data-ttu-id="404df-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="404df-159">RELATED LINKS</span></span>
