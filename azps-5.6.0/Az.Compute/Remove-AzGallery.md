---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: abc9fd93545f229c39dd696a856781ceed748a77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937080"
---
# <span data-ttu-id="17822-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="17822-101">Remove-AzGallery</span></span>

## <span data-ttu-id="17822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17822-102">SYNOPSIS</span></span>
<span data-ttu-id="17822-103">Löschen sie einen Katalog.</span><span class="sxs-lookup"><span data-stu-id="17822-103">Delete a gallery.</span></span>

## <span data-ttu-id="17822-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17822-104">SYNTAX</span></span>

### <span data-ttu-id="17822-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="17822-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17822-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="17822-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17822-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="17822-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17822-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17822-108">DESCRIPTION</span></span>
<span data-ttu-id="17822-109">Löschen sie einen Katalog.</span><span class="sxs-lookup"><span data-stu-id="17822-109">Delete a gallery.</span></span>

## <span data-ttu-id="17822-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17822-110">EXAMPLES</span></span>

### <span data-ttu-id="17822-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17822-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="17822-112">Löschen Sie den angegebenen Katalog.</span><span class="sxs-lookup"><span data-stu-id="17822-112">Delete the given gallery.</span></span>

## <span data-ttu-id="17822-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="17822-113">PARAMETERS</span></span>

### <span data-ttu-id="17822-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17822-114">-AsJob</span></span>
<span data-ttu-id="17822-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="17822-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17822-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17822-116">-DefaultProfile</span></span>
<span data-ttu-id="17822-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17822-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17822-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="17822-118">-Force</span></span>
<span data-ttu-id="17822-119">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="17822-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17822-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17822-120">-InputObject</span></span>
<span data-ttu-id="17822-121">Das PS-Katalogobjekt</span><span class="sxs-lookup"><span data-stu-id="17822-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="17822-122">-Name</span><span class="sxs-lookup"><span data-stu-id="17822-122">-Name</span></span>
<span data-ttu-id="17822-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="17822-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="17822-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17822-124">-ResourceGroupName</span></span>
<span data-ttu-id="17822-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17822-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="17822-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17822-126">-ResourceId</span></span>
<span data-ttu-id="17822-127">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="17822-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="17822-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17822-128">-Confirm</span></span>
<span data-ttu-id="17822-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17822-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17822-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17822-130">-WhatIf</span></span>
<span data-ttu-id="17822-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17822-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17822-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17822-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17822-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17822-133">CommonParameters</span></span>
<span data-ttu-id="17822-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17822-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17822-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17822-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17822-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17822-136">INPUTS</span></span>

### <span data-ttu-id="17822-137">System.String</span><span class="sxs-lookup"><span data-stu-id="17822-137">System.String</span></span>

### <span data-ttu-id="17822-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="17822-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="17822-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17822-139">OUTPUTS</span></span>

### <span data-ttu-id="17822-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="17822-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="17822-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="17822-141">NOTES</span></span>

## <span data-ttu-id="17822-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="17822-142">RELATED LINKS</span></span>
