---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: fa535876524961dc8e7a05ca3acc5fa007f759fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927224"
---
# <span data-ttu-id="6383f-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="6383f-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="6383f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6383f-102">SYNOPSIS</span></span>
<span data-ttu-id="6383f-103">Löschen Sie einen DevSpaces-Controller.</span><span class="sxs-lookup"><span data-stu-id="6383f-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="6383f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6383f-104">SYNTAX</span></span>

### <span data-ttu-id="6383f-105">DevSpacesControllerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6383f-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6383f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6383f-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6383f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6383f-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6383f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6383f-108">DESCRIPTION</span></span>
<span data-ttu-id="6383f-109">Löschen Sie einen DevSpaces-Controller.</span><span class="sxs-lookup"><span data-stu-id="6383f-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="6383f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6383f-110">EXAMPLES</span></span>

### <span data-ttu-id="6383f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6383f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="6383f-112">Löschen Sie einen DevSpaces-Controller mit dem Namen devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="6383f-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="6383f-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6383f-113">PARAMETERS</span></span>

### <span data-ttu-id="6383f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6383f-114">-AsJob</span></span>
<span data-ttu-id="6383f-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6383f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6383f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6383f-116">-DefaultProfile</span></span>
<span data-ttu-id="6383f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6383f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6383f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6383f-118">-InputObject</span></span>
<span data-ttu-id="6383f-119">Ein PSController-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6383f-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6383f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6383f-120">-Name</span></span>
<span data-ttu-id="6383f-121">DevSpaces-Controllername.</span><span class="sxs-lookup"><span data-stu-id="6383f-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6383f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6383f-122">-PassThru</span></span>
<span data-ttu-id="6383f-123">Gibt "true" zurück, wenn "Löschen" erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="6383f-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="6383f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6383f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6383f-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="6383f-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6383f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6383f-126">-ResourceId</span></span>
<span data-ttu-id="6383f-127">Die DevSpaces-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6383f-127">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6383f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6383f-128">-Confirm</span></span>
<span data-ttu-id="6383f-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6383f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6383f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6383f-130">-WhatIf</span></span>
<span data-ttu-id="6383f-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6383f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6383f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6383f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6383f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6383f-133">CommonParameters</span></span>
<span data-ttu-id="6383f-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6383f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6383f-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6383f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6383f-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6383f-136">INPUTS</span></span>

### <span data-ttu-id="6383f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6383f-137">System.String</span></span>

### <span data-ttu-id="6383f-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="6383f-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="6383f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6383f-139">OUTPUTS</span></span>

### <span data-ttu-id="6383f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6383f-140">System.Boolean</span></span>

## <span data-ttu-id="6383f-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6383f-141">NOTES</span></span>

## <span data-ttu-id="6383f-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6383f-142">RELATED LINKS</span></span>
