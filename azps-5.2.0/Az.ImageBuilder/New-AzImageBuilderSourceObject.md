---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297286"
---
# <span data-ttu-id="012c6-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="012c6-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="012c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="012c6-102">SYNOPSIS</span></span>
<span data-ttu-id="012c6-103">Beschreibt eine Bildquelle für einen virtuellen Computer zum Erstellen, Anpassen und Verteilen.</span><span class="sxs-lookup"><span data-stu-id="012c6-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="012c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="012c6-104">SYNTAX</span></span>

### <span data-ttu-id="012c6-105">ManagedImage (Standard)</span><span class="sxs-lookup"><span data-stu-id="012c6-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="012c6-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="012c6-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="012c6-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="012c6-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="012c6-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="012c6-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="012c6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="012c6-109">DESCRIPTION</span></span>
<span data-ttu-id="012c6-110">Beschreibt eine Bildquelle für einen virtuellen Computer zum Erstellen, Anpassen und Verteilen.</span><span class="sxs-lookup"><span data-stu-id="012c6-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="012c6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="012c6-111">EXAMPLES</span></span>

### <span data-ttu-id="012c6-112">Beispiel 1: Erstellen einer verwalteten Bildquelle</span><span class="sxs-lookup"><span data-stu-id="012c6-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="012c6-113">Mit diesem Befehl wird eine verwaltete Bildquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="012c6-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="012c6-114">Beispiel 2: Erstellen einer freigegebenen Bildquelle</span><span class="sxs-lookup"><span data-stu-id="012c6-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="012c6-115">Mit diesem Befehl wird eine freigegebene Bildquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="012c6-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="012c6-116">Beispiel 3: Erstellen einerPlatfrom-Bildquelle</span><span class="sxs-lookup"><span data-stu-id="012c6-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="012c6-117">Mit diesem Befehl wird eine "platfrom"-Bildquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="012c6-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="012c6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="012c6-118">PARAMETERS</span></span>

### <span data-ttu-id="012c6-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="012c6-119">-ImageId</span></span>
<span data-ttu-id="012c6-120">ARM Ressourcen-ID des verwalteten Bilds im Kundenabonnement.</span><span class="sxs-lookup"><span data-stu-id="012c6-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="012c6-121">-ImageVersionId</span></span>
<span data-ttu-id="012c6-122">ARM Ressourcen-ID der Bildversion in der freigegebenen Bildergalerie.</span><span class="sxs-lookup"><span data-stu-id="012c6-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="012c6-123">-Offer</span></span>
<span data-ttu-id="012c6-124">Bildangebot aus der [Azure Gallery Bilder.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="012c6-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="012c6-125">-PlanName</span></span>
<span data-ttu-id="012c6-126">Name des Kaufplans.</span><span class="sxs-lookup"><span data-stu-id="012c6-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="012c6-127">-PlanProduct</span></span>
<span data-ttu-id="012c6-128">Produkt des Kaufplans.</span><span class="sxs-lookup"><span data-stu-id="012c6-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="012c6-129">-PlanPublisher</span></span>
<span data-ttu-id="012c6-130">Herausgeber des Kaufplans.</span><span class="sxs-lookup"><span data-stu-id="012c6-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="012c6-131">-Publisher</span></span>
<span data-ttu-id="012c6-132">Image Publisher in [Azure Gallery Images.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="012c6-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="012c6-133">-Sku</span></span>
<span data-ttu-id="012c6-134">Bild-SKU aus [der Azure Gallery Images.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="012c6-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="012c6-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="012c6-136">Beschreibt eine Bildquelle, bei der es sich um ein verwaltetes Bild im Kundenabonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="012c6-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="012c6-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="012c6-138">Beschreibt eine Bildquelle aus [azure Gallery Images.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="012c6-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="012c6-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="012c6-140">Beschreibt eine Bildquelle, bei der es sich um eine Bildversion in einer freigegebenen Bildergalerie handelt.</span><span class="sxs-lookup"><span data-stu-id="012c6-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-141">-Version</span><span class="sxs-lookup"><span data-stu-id="012c6-141">-Version</span></span>
<span data-ttu-id="012c6-142">Bildversion aus dem [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="012c6-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012c6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="012c6-143">CommonParameters</span></span>
<span data-ttu-id="012c6-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="012c6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="012c6-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="012c6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="012c6-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="012c6-146">INPUTS</span></span>

## <span data-ttu-id="012c6-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="012c6-147">OUTPUTS</span></span>

### <span data-ttu-id="012c6-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="012c6-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="012c6-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="012c6-149">NOTES</span></span>

<span data-ttu-id="012c6-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="012c6-150">ALIASES</span></span>

## <span data-ttu-id="012c6-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="012c6-151">RELATED LINKS</span></span>

