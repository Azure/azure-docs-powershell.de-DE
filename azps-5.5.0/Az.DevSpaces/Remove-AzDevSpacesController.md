---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175620"
---
# <span data-ttu-id="11134-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="11134-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="11134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11134-102">SYNOPSIS</span></span>
<span data-ttu-id="11134-103">Löschen Sie einen DevSpaces-Controller.</span><span class="sxs-lookup"><span data-stu-id="11134-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="11134-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11134-104">SYNTAX</span></span>

### <span data-ttu-id="11134-105">DevSpacesControllerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="11134-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11134-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11134-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11134-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11134-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11134-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11134-108">DESCRIPTION</span></span>
<span data-ttu-id="11134-109">Löschen Sie einen DevSpaces-Controller.</span><span class="sxs-lookup"><span data-stu-id="11134-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="11134-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="11134-110">EXAMPLES</span></span>

### <span data-ttu-id="11134-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11134-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="11134-112">Löschen Sie einen DevSpaces-Controller namens devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="11134-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="11134-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11134-113">PARAMETERS</span></span>

### <span data-ttu-id="11134-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11134-114">-AsJob</span></span>
<span data-ttu-id="11134-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="11134-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11134-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11134-116">-DefaultProfile</span></span>
<span data-ttu-id="11134-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11134-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11134-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11134-118">-InputObject</span></span>
<span data-ttu-id="11134-119">Ein PSController-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="11134-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="11134-120">-Name</span><span class="sxs-lookup"><span data-stu-id="11134-120">-Name</span></span>
<span data-ttu-id="11134-121">DevSpaces-Controllername.</span><span class="sxs-lookup"><span data-stu-id="11134-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="11134-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11134-122">-PassThru</span></span>
<span data-ttu-id="11134-123">Gibt "true" zurück, wenn "delete" erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="11134-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="11134-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11134-124">-ResourceGroupName</span></span>
<span data-ttu-id="11134-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="11134-125">Resource group name</span></span>

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

### <span data-ttu-id="11134-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11134-126">-ResourceId</span></span>
<span data-ttu-id="11134-127">Die DevSpaces-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="11134-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="11134-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11134-128">-Confirm</span></span>
<span data-ttu-id="11134-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11134-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11134-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="11134-130">-WhatIf</span></span>
<span data-ttu-id="11134-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11134-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11134-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11134-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11134-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11134-133">CommonParameters</span></span>
<span data-ttu-id="11134-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11134-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11134-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11134-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11134-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="11134-136">INPUTS</span></span>

### <span data-ttu-id="11134-137">System.String</span><span class="sxs-lookup"><span data-stu-id="11134-137">System.String</span></span>

### <span data-ttu-id="11134-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="11134-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="11134-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="11134-139">OUTPUTS</span></span>

### <span data-ttu-id="11134-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11134-140">System.Boolean</span></span>

## <span data-ttu-id="11134-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="11134-141">NOTES</span></span>

## <span data-ttu-id="11134-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="11134-142">RELATED LINKS</span></span>
