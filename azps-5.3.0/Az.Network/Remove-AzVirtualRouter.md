---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385215"
---
# <span data-ttu-id="5b1ed-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5b1ed-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="5b1ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b1ed-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1ed-103">Löscht einen Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="5b1ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b1ed-104">SYNTAX</span></span>

### <span data-ttu-id="5b1ed-105">VirtualRouterNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b1ed-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1ed-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1ed-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1ed-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1ed-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b1ed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b1ed-108">DESCRIPTION</span></span>
<span data-ttu-id="5b1ed-109">Das **Cmdlet "Remove-AzVirtualRouter"** löscht einen Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5b1ed-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="5b1ed-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b1ed-110">EXAMPLES</span></span>

### <span data-ttu-id="5b1ed-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b1ed-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="5b1ed-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b1ed-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="5b1ed-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5b1ed-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="5b1ed-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b1ed-114">PARAMETERS</span></span>

### <span data-ttu-id="5b1ed-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b1ed-115">-AsJob</span></span>
<span data-ttu-id="5b1ed-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5b1ed-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b1ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1ed-117">-DefaultProfile</span></span>
<span data-ttu-id="5b1ed-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b1ed-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5b1ed-119">-Force</span></span>
<span data-ttu-id="5b1ed-120">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="5b1ed-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5b1ed-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b1ed-121">-InputObject</span></span>
<span data-ttu-id="5b1ed-122">Das Eingabeobjekt des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1ed-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b1ed-123">-PassThru</span></span>
<span data-ttu-id="5b1ed-124">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="5b1ed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1ed-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b1ed-126">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1ed-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1ed-127">-ResourceId</span></span>
<span data-ttu-id="5b1ed-128">Die Id der virtuellen Routerressource.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1ed-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="5b1ed-129">-RouterName</span></span>
<span data-ttu-id="5b1ed-130">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1ed-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b1ed-131">-Confirm</span></span>
<span data-ttu-id="5b1ed-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1ed-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5b1ed-133">-WhatIf</span></span>
<span data-ttu-id="5b1ed-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b1ed-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1ed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1ed-136">CommonParameters</span></span>
<span data-ttu-id="5b1ed-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1ed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1ed-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b1ed-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1ed-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b1ed-139">INPUTS</span></span>

### <span data-ttu-id="5b1ed-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5b1ed-140">System.String</span></span>

### <span data-ttu-id="5b1ed-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5b1ed-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="5b1ed-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b1ed-142">OUTPUTS</span></span>

### <span data-ttu-id="5b1ed-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b1ed-143">System.Boolean</span></span>

## <span data-ttu-id="5b1ed-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5b1ed-144">NOTES</span></span>

## <span data-ttu-id="5b1ed-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5b1ed-145">RELATED LINKS</span></span>
