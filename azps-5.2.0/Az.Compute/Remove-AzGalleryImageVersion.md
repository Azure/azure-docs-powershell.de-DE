---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362352"
---
# <span data-ttu-id="a2101-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a2101-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="a2101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2101-102">SYNOPSIS</span></span>
<span data-ttu-id="a2101-103">Löschen einer Katalogbildversion</span><span class="sxs-lookup"><span data-stu-id="a2101-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="a2101-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2101-104">SYNTAX</span></span>

### <span data-ttu-id="a2101-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2101-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2101-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a2101-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2101-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a2101-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2101-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2101-108">DESCRIPTION</span></span>
<span data-ttu-id="a2101-109">Löschen einer Katalogbildversion</span><span class="sxs-lookup"><span data-stu-id="a2101-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="a2101-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2101-110">EXAMPLES</span></span>

### <span data-ttu-id="a2101-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2101-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="a2101-112">Löschen Sie die angegebene Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="a2101-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="a2101-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2101-113">PARAMETERS</span></span>

### <span data-ttu-id="a2101-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2101-114">-AsJob</span></span>
<span data-ttu-id="a2101-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a2101-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2101-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2101-116">-DefaultProfile</span></span>
<span data-ttu-id="a2101-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2101-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2101-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a2101-118">-Force</span></span>
<span data-ttu-id="a2101-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="a2101-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a2101-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a2101-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="a2101-121">Der Name der Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="a2101-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="a2101-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="a2101-122">-GalleryName</span></span>
<span data-ttu-id="a2101-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="a2101-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="a2101-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2101-124">-InputObject</span></span>
<span data-ttu-id="a2101-125">Das Ps Gallery Image Version Object</span><span class="sxs-lookup"><span data-stu-id="a2101-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="a2101-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a2101-126">-Name</span></span>
<span data-ttu-id="a2101-127">Der Name der Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="a2101-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="a2101-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2101-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2101-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a2101-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2101-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2101-130">-ResourceId</span></span>
<span data-ttu-id="a2101-131">Die Ressourcen-ID für die Katalogbildversion</span><span class="sxs-lookup"><span data-stu-id="a2101-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="a2101-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2101-132">-Confirm</span></span>
<span data-ttu-id="a2101-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2101-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2101-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a2101-134">-WhatIf</span></span>
<span data-ttu-id="a2101-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2101-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2101-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2101-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2101-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2101-137">CommonParameters</span></span>
<span data-ttu-id="a2101-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2101-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2101-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2101-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2101-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2101-140">INPUTS</span></span>

### <span data-ttu-id="a2101-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a2101-141">System.String</span></span>

### <span data-ttu-id="a2101-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a2101-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="a2101-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2101-143">OUTPUTS</span></span>

### <span data-ttu-id="a2101-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a2101-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a2101-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a2101-145">NOTES</span></span>

## <span data-ttu-id="a2101-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a2101-146">RELATED LINKS</span></span>
