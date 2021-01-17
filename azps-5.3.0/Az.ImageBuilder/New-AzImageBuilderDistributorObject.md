---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469588"
---
# <span data-ttu-id="0153d-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="0153d-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="0153d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0153d-102">SYNOPSIS</span></span>
<span data-ttu-id="0153d-103">Generisches Verteilungsobjekt</span><span class="sxs-lookup"><span data-stu-id="0153d-103">Generic distribution object</span></span>

## <span data-ttu-id="0153d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0153d-104">SYNTAX</span></span>

### <span data-ttu-id="0153d-105">ManagedImageDistributor (Standard)</span><span class="sxs-lookup"><span data-stu-id="0153d-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="0153d-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="0153d-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="0153d-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="0153d-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="0153d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0153d-108">DESCRIPTION</span></span>
<span data-ttu-id="0153d-109">Generisches Verteilungsobjekt</span><span class="sxs-lookup"><span data-stu-id="0153d-109">Generic distribution object</span></span>

## <span data-ttu-id="0153d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0153d-110">EXAMPLES</span></span>

### <span data-ttu-id="0153d-111">Beispiel 1: Erstellen eines verwalteten Bildverteilers</span><span class="sxs-lookup"><span data-stu-id="0153d-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="0153d-112">Mit diesem Befehl wird ein verwalteter Bildvertreiber erstellt.</span><span class="sxs-lookup"><span data-stu-id="0153d-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="0153d-113">Beispiel 2: Erstellen eines VHD-Händlers</span><span class="sxs-lookup"><span data-stu-id="0153d-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="0153d-114">Dieser Befehl erstellt einen VHD-Händler.</span><span class="sxs-lookup"><span data-stu-id="0153d-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="0153d-115">Beispiel 3: Erstellen eines freigegebenen Bildvertreibers</span><span class="sxs-lookup"><span data-stu-id="0153d-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="0153d-116">Mit diesem Befehl wird ein freigegebener Bildvertreiber erstellt.</span><span class="sxs-lookup"><span data-stu-id="0153d-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="0153d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0153d-117">PARAMETERS</span></span>

### <span data-ttu-id="0153d-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="0153d-118">-ArtifactTag</span></span>
<span data-ttu-id="0153d-119">Tags, die auf das Artefakt angewendet werden, nachdem es vom Distributor erstellt/aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0153d-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="0153d-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="0153d-121">Flag, das angibt, ob die erstellte Bildversion von der neuesten Version ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0153d-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="0153d-122">Weglassen, um den Standardwert (false) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0153d-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="0153d-123">-GalleryImageId</span></span>
<span data-ttu-id="0153d-124">Ressourcen-ID des Bilds "Freigegebene Bildergalerie".</span><span class="sxs-lookup"><span data-stu-id="0153d-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="0153d-125">-ImageId</span></span>
<span data-ttu-id="0153d-126">Ressourcen-ID des Bilds für verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="0153d-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-127">-Location</span><span class="sxs-lookup"><span data-stu-id="0153d-127">-Location</span></span>
<span data-ttu-id="0153d-128">Der Azure-Speicherort für das Bild sollte übereinstimmen, wenn das Bild bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0153d-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="0153d-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="0153d-130">Als verwaltetes Datenträgerabbild verteilen.</span><span class="sxs-lookup"><span data-stu-id="0153d-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="0153d-131">-ReplicationRegion</span></span>
<span data-ttu-id="0153d-132">Eine Liste der Bereiche, in die das Bild repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="0153d-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="0153d-133">-RunOutputName</span></span>
<span data-ttu-id="0153d-134">Der Name, der für den zugeordneten RunOutput verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0153d-134">The name to be used for the associated RunOutput.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="0153d-135">-SharedImageDistributor</span></span>
<span data-ttu-id="0153d-136">Verteilen über freigegebene Bildergalerie.</span><span class="sxs-lookup"><span data-stu-id="0153d-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0153d-137">-StorageAccountType</span></span>
<span data-ttu-id="0153d-138">Speicherkontotyp, der zum Speichern des freigegebenen Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0153d-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="0153d-139">Weglassen, um die Standardeinstellung (Standard_LRS) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0153d-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="0153d-140">-VhdDistributor</span></span>
<span data-ttu-id="0153d-141">Verteilen sie über VHD in einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="0153d-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0153d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0153d-142">CommonParameters</span></span>
<span data-ttu-id="0153d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0153d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0153d-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0153d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0153d-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0153d-145">INPUTS</span></span>

## <span data-ttu-id="0153d-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0153d-146">OUTPUTS</span></span>

### <span data-ttu-id="0153d-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="0153d-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="0153d-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0153d-148">NOTES</span></span>

<span data-ttu-id="0153d-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0153d-149">ALIASES</span></span>

## <span data-ttu-id="0153d-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0153d-150">RELATED LINKS</span></span>

