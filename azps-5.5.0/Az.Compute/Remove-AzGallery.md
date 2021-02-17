---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175945"
---
# <span data-ttu-id="40ec2-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="40ec2-101">Remove-AzGallery</span></span>

## <span data-ttu-id="40ec2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="40ec2-103">Löschen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="40ec2-103">Delete a gallery.</span></span>

## <span data-ttu-id="40ec2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40ec2-104">SYNTAX</span></span>

### <span data-ttu-id="40ec2-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="40ec2-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ec2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="40ec2-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ec2-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="40ec2-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40ec2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40ec2-108">DESCRIPTION</span></span>
<span data-ttu-id="40ec2-109">Löschen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="40ec2-109">Delete a gallery.</span></span>

## <span data-ttu-id="40ec2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40ec2-110">EXAMPLES</span></span>

### <span data-ttu-id="40ec2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40ec2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="40ec2-112">Löschen Sie den angegebenen Katalog.</span><span class="sxs-lookup"><span data-stu-id="40ec2-112">Delete the given gallery.</span></span>

## <span data-ttu-id="40ec2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40ec2-113">PARAMETERS</span></span>

### <span data-ttu-id="40ec2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40ec2-114">-AsJob</span></span>
<span data-ttu-id="40ec2-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="40ec2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40ec2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ec2-116">-DefaultProfile</span></span>
<span data-ttu-id="40ec2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40ec2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40ec2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="40ec2-118">-Force</span></span>
<span data-ttu-id="40ec2-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="40ec2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="40ec2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40ec2-120">-InputObject</span></span>
<span data-ttu-id="40ec2-121">Das PS -Katalogobjekt</span><span class="sxs-lookup"><span data-stu-id="40ec2-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="40ec2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="40ec2-122">-Name</span></span>
<span data-ttu-id="40ec2-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="40ec2-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="40ec2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40ec2-124">-ResourceGroupName</span></span>
<span data-ttu-id="40ec2-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40ec2-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="40ec2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40ec2-126">-ResourceId</span></span>
<span data-ttu-id="40ec2-127">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="40ec2-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="40ec2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40ec2-128">-Confirm</span></span>
<span data-ttu-id="40ec2-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40ec2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40ec2-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="40ec2-130">-WhatIf</span></span>
<span data-ttu-id="40ec2-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40ec2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40ec2-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40ec2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40ec2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ec2-133">CommonParameters</span></span>
<span data-ttu-id="40ec2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ec2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ec2-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40ec2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ec2-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40ec2-136">INPUTS</span></span>

### <span data-ttu-id="40ec2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="40ec2-137">System.String</span></span>

### <span data-ttu-id="40ec2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="40ec2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="40ec2-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40ec2-139">OUTPUTS</span></span>

### <span data-ttu-id="40ec2-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="40ec2-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="40ec2-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40ec2-141">NOTES</span></span>

## <span data-ttu-id="40ec2-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40ec2-142">RELATED LINKS</span></span>
