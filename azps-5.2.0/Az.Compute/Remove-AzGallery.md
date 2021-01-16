---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296573"
---
# <span data-ttu-id="7250e-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="7250e-101">Remove-AzGallery</span></span>

## <span data-ttu-id="7250e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7250e-102">SYNOPSIS</span></span>
<span data-ttu-id="7250e-103">Löschen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="7250e-103">Delete a gallery.</span></span>

## <span data-ttu-id="7250e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7250e-104">SYNTAX</span></span>

### <span data-ttu-id="7250e-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="7250e-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7250e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7250e-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7250e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="7250e-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7250e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7250e-108">DESCRIPTION</span></span>
<span data-ttu-id="7250e-109">Löschen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="7250e-109">Delete a gallery.</span></span>

## <span data-ttu-id="7250e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7250e-110">EXAMPLES</span></span>

### <span data-ttu-id="7250e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7250e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="7250e-112">Löschen Sie den angegebenen Katalog.</span><span class="sxs-lookup"><span data-stu-id="7250e-112">Delete the given gallery.</span></span>

## <span data-ttu-id="7250e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7250e-113">PARAMETERS</span></span>

### <span data-ttu-id="7250e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7250e-114">-AsJob</span></span>
<span data-ttu-id="7250e-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7250e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7250e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7250e-116">-DefaultProfile</span></span>
<span data-ttu-id="7250e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7250e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7250e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7250e-118">-Force</span></span>
<span data-ttu-id="7250e-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="7250e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7250e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7250e-120">-InputObject</span></span>
<span data-ttu-id="7250e-121">Das PS -Katalogobjekt</span><span class="sxs-lookup"><span data-stu-id="7250e-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="7250e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7250e-122">-Name</span></span>
<span data-ttu-id="7250e-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="7250e-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="7250e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7250e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7250e-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7250e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="7250e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7250e-126">-ResourceId</span></span>
<span data-ttu-id="7250e-127">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="7250e-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="7250e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7250e-128">-Confirm</span></span>
<span data-ttu-id="7250e-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7250e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7250e-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7250e-130">-WhatIf</span></span>
<span data-ttu-id="7250e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7250e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7250e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7250e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7250e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7250e-133">CommonParameters</span></span>
<span data-ttu-id="7250e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7250e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7250e-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7250e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7250e-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7250e-136">INPUTS</span></span>

### <span data-ttu-id="7250e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7250e-137">System.String</span></span>

### <span data-ttu-id="7250e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="7250e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="7250e-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7250e-139">OUTPUTS</span></span>

### <span data-ttu-id="7250e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7250e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7250e-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7250e-141">NOTES</span></span>

## <span data-ttu-id="7250e-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7250e-142">RELATED LINKS</span></span>
