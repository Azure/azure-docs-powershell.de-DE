---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472915"
---
# <span data-ttu-id="97c8b-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="97c8b-101">Update-AzGallery</span></span>

## <span data-ttu-id="97c8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="97c8b-103">Aktualisieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="97c8b-103">Update a gallery.</span></span>

## <span data-ttu-id="97c8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97c8b-104">SYNTAX</span></span>

### <span data-ttu-id="97c8b-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="97c8b-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c8b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="97c8b-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c8b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="97c8b-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c8b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97c8b-108">DESCRIPTION</span></span>
<span data-ttu-id="97c8b-109">Aktualisieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="97c8b-109">Update a gallery.</span></span>

## <span data-ttu-id="97c8b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97c8b-110">EXAMPLES</span></span>

### <span data-ttu-id="97c8b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97c8b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="97c8b-112">Aktualisieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="97c8b-112">Update a gallery.</span></span>

## <span data-ttu-id="97c8b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97c8b-113">PARAMETERS</span></span>

### <span data-ttu-id="97c8b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97c8b-114">-AsJob</span></span>
<span data-ttu-id="97c8b-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="97c8b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97c8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c8b-116">-DefaultProfile</span></span>
<span data-ttu-id="97c8b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97c8b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97c8b-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97c8b-118">-Description</span></span>
<span data-ttu-id="97c8b-119">Die Beschreibung der Katalogressource.</span><span class="sxs-lookup"><span data-stu-id="97c8b-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="97c8b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97c8b-120">-InputObject</span></span>
<span data-ttu-id="97c8b-121">Das PS Gallery-Objekt.</span><span class="sxs-lookup"><span data-stu-id="97c8b-121">The PS Gallery Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c8b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="97c8b-122">-Name</span></span>
<span data-ttu-id="97c8b-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="97c8b-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97c8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="97c8b-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97c8b-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="97c8b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97c8b-126">-ResourceId</span></span>
<span data-ttu-id="97c8b-127">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="97c8b-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="97c8b-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="97c8b-128">-Tag</span></span>
<span data-ttu-id="97c8b-129">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="97c8b-129">Resource tags</span></span>

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

### <span data-ttu-id="97c8b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97c8b-130">-Confirm</span></span>
<span data-ttu-id="97c8b-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="97c8b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c8b-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="97c8b-132">-WhatIf</span></span>
<span data-ttu-id="97c8b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97c8b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97c8b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97c8b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c8b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c8b-135">CommonParameters</span></span>
<span data-ttu-id="97c8b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c8b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c8b-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97c8b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c8b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97c8b-138">INPUTS</span></span>

### <span data-ttu-id="97c8b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="97c8b-139">System.String</span></span>

### <span data-ttu-id="97c8b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="97c8b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="97c8b-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="97c8b-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="97c8b-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97c8b-142">OUTPUTS</span></span>

### <span data-ttu-id="97c8b-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="97c8b-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="97c8b-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97c8b-144">NOTES</span></span>

## <span data-ttu-id="97c8b-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97c8b-145">RELATED LINKS</span></span>
