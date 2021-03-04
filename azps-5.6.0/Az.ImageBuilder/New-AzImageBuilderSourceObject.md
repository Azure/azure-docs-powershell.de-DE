---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: a106435739d7e4ec358038be476cc3f2ba8cd09d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949136"
---
# <span data-ttu-id="58103-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="58103-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="58103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58103-102">SYNOPSIS</span></span>
<span data-ttu-id="58103-103">Beschreibt eine Bildquelle für virtuelle Computer zum Erstellen, Anpassen und Verteilen.</span><span class="sxs-lookup"><span data-stu-id="58103-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="58103-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58103-104">SYNTAX</span></span>

### <span data-ttu-id="58103-105">ManagedImage (Standard)</span><span class="sxs-lookup"><span data-stu-id="58103-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="58103-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="58103-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="58103-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="58103-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="58103-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="58103-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="58103-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58103-109">DESCRIPTION</span></span>
<span data-ttu-id="58103-110">Beschreibt eine Bildquelle für virtuelle Computer zum Erstellen, Anpassen und Verteilen.</span><span class="sxs-lookup"><span data-stu-id="58103-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="58103-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58103-111">EXAMPLES</span></span>

### <span data-ttu-id="58103-112">Beispiel 1: Erstellen einer verwalteten Bildquelle</span><span class="sxs-lookup"><span data-stu-id="58103-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="58103-113">Mit diesem Befehl wird eine verwaltete Bildquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="58103-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="58103-114">Beispiel 2: Erstellen einer freigegebenen Bildquelle</span><span class="sxs-lookup"><span data-stu-id="58103-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="58103-115">Mit diesem Befehl wird eine freigegebene Bildquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="58103-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="58103-116">Beispiel 3: Erstellen einer Platfrom-Bildquelle</span><span class="sxs-lookup"><span data-stu-id="58103-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="58103-117">Mit diesem Befehl wird eine Platfrom-Bildquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="58103-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="58103-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="58103-118">PARAMETERS</span></span>

### <span data-ttu-id="58103-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="58103-119">-ImageId</span></span>
<span data-ttu-id="58103-120">ARM ressourcen-ID des verwalteten Bilds im Kundenabonnement.</span><span class="sxs-lookup"><span data-stu-id="58103-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="58103-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="58103-121">-ImageVersionId</span></span>
<span data-ttu-id="58103-122">ARM ressourcen-ID der Bildversion im freigegebenen Bildkatalog.</span><span class="sxs-lookup"><span data-stu-id="58103-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="58103-123">-Angebot</span><span class="sxs-lookup"><span data-stu-id="58103-123">-Offer</span></span>
<span data-ttu-id="58103-124">Bildangebot aus der [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58103-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58103-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="58103-125">-PlanName</span></span>
<span data-ttu-id="58103-126">Name des Einkaufsplans.</span><span class="sxs-lookup"><span data-stu-id="58103-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="58103-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="58103-127">-PlanProduct</span></span>
<span data-ttu-id="58103-128">Produkt des Einkaufsplans.</span><span class="sxs-lookup"><span data-stu-id="58103-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="58103-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="58103-129">-PlanPublisher</span></span>
<span data-ttu-id="58103-130">Herausgeber des Einkaufsplans.</span><span class="sxs-lookup"><span data-stu-id="58103-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="58103-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="58103-131">-Publisher</span></span>
<span data-ttu-id="58103-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58103-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58103-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="58103-133">-Sku</span></span>
<span data-ttu-id="58103-134">Bildsku aus den [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58103-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58103-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="58103-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="58103-136">Beschreibt eine Bildquelle, bei der es sich um ein verwaltetes Bild im Kundenabonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="58103-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="58103-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="58103-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="58103-138">Beschreibt eine Bildquelle aus [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58103-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58103-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="58103-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="58103-140">Beschreibt eine Bildquelle, bei der es sich um eine Bildversion in einem freigegebenen Bilderkatalog handelt.</span><span class="sxs-lookup"><span data-stu-id="58103-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="58103-141">-Version</span><span class="sxs-lookup"><span data-stu-id="58103-141">-Version</span></span>
<span data-ttu-id="58103-142">Bildversion aus den [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58103-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58103-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58103-143">CommonParameters</span></span>
<span data-ttu-id="58103-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58103-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58103-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58103-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58103-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58103-146">INPUTS</span></span>

## <span data-ttu-id="58103-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58103-147">OUTPUTS</span></span>

### <span data-ttu-id="58103-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="58103-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="58103-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="58103-149">NOTES</span></span>

<span data-ttu-id="58103-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="58103-150">ALIASES</span></span>

## <span data-ttu-id="58103-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="58103-151">RELATED LINKS</span></span>

