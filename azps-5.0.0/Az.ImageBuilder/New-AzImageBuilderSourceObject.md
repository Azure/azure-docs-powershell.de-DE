---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296266"
---
# <span data-ttu-id="27cfe-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="27cfe-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="27cfe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="27cfe-103">Beschreibt eine Bildquelle für einen virtuellen Computer zum Erstellen, anpassen und verteilen.</span><span class="sxs-lookup"><span data-stu-id="27cfe-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="27cfe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27cfe-104">SYNTAX</span></span>

### <span data-ttu-id="27cfe-105">ManagedImage (Standard)</span><span class="sxs-lookup"><span data-stu-id="27cfe-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="27cfe-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="27cfe-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="27cfe-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="27cfe-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="27cfe-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="27cfe-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="27cfe-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27cfe-109">DESCRIPTION</span></span>
<span data-ttu-id="27cfe-110">Beschreibt eine Bildquelle für einen virtuellen Computer zum Erstellen, anpassen und verteilen.</span><span class="sxs-lookup"><span data-stu-id="27cfe-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="27cfe-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27cfe-111">EXAMPLES</span></span>

### <span data-ttu-id="27cfe-112">Beispiel 1: Erstellen einer verwalteten Bildquelle</span><span class="sxs-lookup"><span data-stu-id="27cfe-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="27cfe-113">Mit diesem Befehl wird eine verwaltete Bildquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="27cfe-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="27cfe-114">Beispiel 2: Erstellen einer freigegebenen Bildquelle</span><span class="sxs-lookup"><span data-stu-id="27cfe-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="27cfe-115">Mit diesem Befehl wird eine freigegebene Bildquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="27cfe-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="27cfe-116">Beispiel 3: Erstellen einer Plattform-Bildquelle</span><span class="sxs-lookup"><span data-stu-id="27cfe-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="27cfe-117">Mit diesem Befehl wird eine Plattform-Bildquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="27cfe-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="27cfe-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="27cfe-118">PARAMETERS</span></span>

### <span data-ttu-id="27cfe-119">-Imagedaten</span><span class="sxs-lookup"><span data-stu-id="27cfe-119">-ImageId</span></span>
<span data-ttu-id="27cfe-120">Arm-Ressourcen-ID des verwalteten Bilds im Kundenabonnement.</span><span class="sxs-lookup"><span data-stu-id="27cfe-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="27cfe-121">-Imageversional</span><span class="sxs-lookup"><span data-stu-id="27cfe-121">-ImageVersionId</span></span>
<span data-ttu-id="27cfe-122">Arm-Ressourcen-ID der Bildversion im freigegebenen Bilder Katalog</span><span class="sxs-lookup"><span data-stu-id="27cfe-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="27cfe-123">-Angebot</span><span class="sxs-lookup"><span data-stu-id="27cfe-123">-Offer</span></span>
<span data-ttu-id="27cfe-124">Bildangebot aus den [Azure Gallery-Bildern](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="27cfe-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="27cfe-125">-Planname</span><span class="sxs-lookup"><span data-stu-id="27cfe-125">-PlanName</span></span>
<span data-ttu-id="27cfe-126">Name des Kauf Plans</span><span class="sxs-lookup"><span data-stu-id="27cfe-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="27cfe-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="27cfe-127">-PlanProduct</span></span>
<span data-ttu-id="27cfe-128">Produkt des Kauf Plans</span><span class="sxs-lookup"><span data-stu-id="27cfe-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="27cfe-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="27cfe-129">-PlanPublisher</span></span>
<span data-ttu-id="27cfe-130">Publisher des Kauf Plans</span><span class="sxs-lookup"><span data-stu-id="27cfe-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="27cfe-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="27cfe-131">-Publisher</span></span>
<span data-ttu-id="27cfe-132">Bildherausgeber in [Azure Gallery-Bildern](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="27cfe-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="27cfe-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="27cfe-133">-Sku</span></span>
<span data-ttu-id="27cfe-134">Bild-SKU aus den [Azure Gallery-Bildern](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="27cfe-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="27cfe-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="27cfe-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="27cfe-136">Beschreibt eine Bildquelle, bei der es sich um ein verwaltetes Bild im Kundenabonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="27cfe-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="27cfe-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="27cfe-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="27cfe-138">Beschreibt eine Bildquelle aus [Azure Gallery-Bildern](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="27cfe-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="27cfe-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="27cfe-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="27cfe-140">Beschreibt eine Bildquelle, bei der es sich um eine Bildversion in einem freigegebenen Bilder Katalog handelt.</span><span class="sxs-lookup"><span data-stu-id="27cfe-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="27cfe-141">-Version</span><span class="sxs-lookup"><span data-stu-id="27cfe-141">-Version</span></span>
<span data-ttu-id="27cfe-142">Bildversion aus den [Azure Gallery-Bildern](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="27cfe-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="27cfe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cfe-143">CommonParameters</span></span>
<span data-ttu-id="27cfe-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27cfe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cfe-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27cfe-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cfe-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27cfe-146">INPUTS</span></span>

## <span data-ttu-id="27cfe-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27cfe-147">OUTPUTS</span></span>

### <span data-ttu-id="27cfe-148">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="27cfe-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="27cfe-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="27cfe-149">NOTES</span></span>

<span data-ttu-id="27cfe-150">Aliase</span><span class="sxs-lookup"><span data-stu-id="27cfe-150">ALIASES</span></span>

## <span data-ttu-id="27cfe-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27cfe-151">RELATED LINKS</span></span>

