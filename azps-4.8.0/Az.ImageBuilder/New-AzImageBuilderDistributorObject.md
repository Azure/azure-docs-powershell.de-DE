---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009250"
---
# <span data-ttu-id="4febf-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="4febf-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="4febf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4febf-102">SYNOPSIS</span></span>
<span data-ttu-id="4febf-103">Generisches Verteilungsobjekt</span><span class="sxs-lookup"><span data-stu-id="4febf-103">Generic distribution object</span></span>

## <span data-ttu-id="4febf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4febf-104">SYNTAX</span></span>

### <span data-ttu-id="4febf-105">ManagedImageDistributor (Standard)</span><span class="sxs-lookup"><span data-stu-id="4febf-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="4febf-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="4febf-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="4febf-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="4febf-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="4febf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4febf-108">DESCRIPTION</span></span>
<span data-ttu-id="4febf-109">Generisches Verteilungsobjekt</span><span class="sxs-lookup"><span data-stu-id="4febf-109">Generic distribution object</span></span>

## <span data-ttu-id="4febf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4febf-110">EXAMPLES</span></span>

### <span data-ttu-id="4febf-111">Beispiel 1: Erstellen eines verwalteten Bild Verteilers</span><span class="sxs-lookup"><span data-stu-id="4febf-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="4febf-112">Dieser Befehl erstellt einen verwalteten Bild Verteiler.</span><span class="sxs-lookup"><span data-stu-id="4febf-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="4febf-113">Beispiel 2: Erstellen eines VHD-Verteilers</span><span class="sxs-lookup"><span data-stu-id="4febf-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="4febf-114">Dieser Befehl erstellt einen VHD-Verteiler.</span><span class="sxs-lookup"><span data-stu-id="4febf-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="4febf-115">Beispiel 3: Erstellen eines freigegebenen Bild Verteilers</span><span class="sxs-lookup"><span data-stu-id="4febf-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="4febf-116">Dieser Befehl erstellt einen freigegebenen Bild Verteiler.</span><span class="sxs-lookup"><span data-stu-id="4febf-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="4febf-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4febf-117">PARAMETERS</span></span>

### <span data-ttu-id="4febf-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="4febf-118">-ArtifactTag</span></span>
<span data-ttu-id="4febf-119">Tags, die auf das Artefakt angewendet werden, nachdem es vom Verteiler erstellt/aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4febf-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

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

### <span data-ttu-id="4febf-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="4febf-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="4febf-121">Flag, das angibt, ob die erstellte Bildversion von letzterem ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4febf-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="4febf-122">Unterlassen Sie die Verwendung des standardmäßigen (false).</span><span class="sxs-lookup"><span data-stu-id="4febf-122">Omit to use the default (false).</span></span>

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

### <span data-ttu-id="4febf-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="4febf-123">-GalleryImageId</span></span>
<span data-ttu-id="4febf-124">Ressourcen-ID des freigegebenen Bildergalerie-Bilds</span><span class="sxs-lookup"><span data-stu-id="4febf-124">Resource Id of the Shared Image Gallery image.</span></span>

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

### <span data-ttu-id="4febf-125">-Imagedaten</span><span class="sxs-lookup"><span data-stu-id="4febf-125">-ImageId</span></span>
<span data-ttu-id="4febf-126">Die Ressourcen-ID des verwalteten Datenträgerabbilds.</span><span class="sxs-lookup"><span data-stu-id="4febf-126">Resource Id of the Managed Disk Image.</span></span>

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

### <span data-ttu-id="4febf-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="4febf-127">-Location</span></span>
<span data-ttu-id="4febf-128">Azure Position für das Bild, sollte übereinstimmen, wenn Bild bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4febf-128">Azure location for the image, should match if image already exists.</span></span>

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

### <span data-ttu-id="4febf-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="4febf-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="4febf-130">Als verwaltete Datenträgerabbildung verteilen.</span><span class="sxs-lookup"><span data-stu-id="4febf-130">Distribute as a Managed Disk Image.</span></span>

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

### <span data-ttu-id="4febf-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="4febf-131">-ReplicationRegion</span></span>
<span data-ttu-id="4febf-132">Eine Liste der Regionen, in die das Bild repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="4febf-132">A list of regions that the image will be replicated to.</span></span>

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

### <span data-ttu-id="4febf-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="4febf-133">-RunOutputName</span></span>
<span data-ttu-id="4febf-134">Der Name, der für das zugeordnete RunOutput verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4febf-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="4febf-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="4febf-135">-SharedImageDistributor</span></span>
<span data-ttu-id="4febf-136">Über freigegebene Bildergalerie verteilen.</span><span class="sxs-lookup"><span data-stu-id="4febf-136">Distribute via Shared Image Gallery.</span></span>

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

### <span data-ttu-id="4febf-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4febf-137">-StorageAccountType</span></span>
<span data-ttu-id="4febf-138">Der zum Speichern des freigegebenen Bilds zu verwendende Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="4febf-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="4febf-139">Unterlassen Sie die Verwendung der Standardeinstellung (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="4febf-139">Omit to use the default (Standard_LRS).</span></span>

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

### <span data-ttu-id="4febf-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="4febf-140">-VhdDistributor</span></span>
<span data-ttu-id="4febf-141">Verteilen über VHD in einem Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="4febf-141">Distribute via VHD in a storage account.</span></span>

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

### <span data-ttu-id="4febf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4febf-142">CommonParameters</span></span>
<span data-ttu-id="4febf-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4febf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4febf-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4febf-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4febf-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4febf-145">INPUTS</span></span>

## <span data-ttu-id="4febf-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4febf-146">OUTPUTS</span></span>

### <span data-ttu-id="4febf-147">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="4febf-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="4febf-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="4febf-148">NOTES</span></span>

<span data-ttu-id="4febf-149">Aliase</span><span class="sxs-lookup"><span data-stu-id="4febf-149">ALIASES</span></span>

## <span data-ttu-id="4febf-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4febf-150">RELATED LINKS</span></span>

