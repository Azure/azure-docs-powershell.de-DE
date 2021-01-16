---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299224"
---
# <span data-ttu-id="ce127-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="ce127-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="ce127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce127-102">SYNOPSIS</span></span>
<span data-ttu-id="ce127-103">Löschen einer Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="ce127-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="ce127-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce127-104">SYNTAX</span></span>

### <span data-ttu-id="ce127-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce127-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce127-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ce127-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce127-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ce127-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce127-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce127-108">DESCRIPTION</span></span>
<span data-ttu-id="ce127-109">Löschen einer Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="ce127-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="ce127-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce127-110">EXAMPLES</span></span>

### <span data-ttu-id="ce127-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce127-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="ce127-112">Entfernen Sie die Bilddefinition des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="ce127-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="ce127-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce127-113">PARAMETERS</span></span>

### <span data-ttu-id="ce127-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce127-114">-AsJob</span></span>
<span data-ttu-id="ce127-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ce127-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce127-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce127-116">-DefaultProfile</span></span>
<span data-ttu-id="ce127-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce127-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce127-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ce127-118">-Force</span></span>
<span data-ttu-id="ce127-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="ce127-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce127-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="ce127-120">-GalleryName</span></span>
<span data-ttu-id="ce127-121">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="ce127-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="ce127-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce127-122">-InputObject</span></span>
<span data-ttu-id="ce127-123">Das Bilddefinitionsobjekt des PS Gallery</span><span class="sxs-lookup"><span data-stu-id="ce127-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce127-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ce127-124">-Name</span></span>
<span data-ttu-id="ce127-125">Der Name der Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="ce127-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce127-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce127-126">-ResourceGroupName</span></span>
<span data-ttu-id="ce127-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ce127-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce127-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce127-128">-ResourceId</span></span>
<span data-ttu-id="ce127-129">Die Ressourcen-ID für die Bilddefinition des Katalogs</span><span class="sxs-lookup"><span data-stu-id="ce127-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="ce127-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce127-130">-Confirm</span></span>
<span data-ttu-id="ce127-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce127-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce127-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ce127-132">-WhatIf</span></span>
<span data-ttu-id="ce127-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce127-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce127-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce127-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce127-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce127-135">CommonParameters</span></span>
<span data-ttu-id="ce127-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce127-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce127-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce127-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce127-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce127-138">INPUTS</span></span>

### <span data-ttu-id="ce127-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ce127-139">System.String</span></span>

### <span data-ttu-id="ce127-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="ce127-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="ce127-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce127-141">OUTPUTS</span></span>

### <span data-ttu-id="ce127-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ce127-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ce127-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce127-143">NOTES</span></span>

## <span data-ttu-id="ce127-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce127-144">RELATED LINKS</span></span>
