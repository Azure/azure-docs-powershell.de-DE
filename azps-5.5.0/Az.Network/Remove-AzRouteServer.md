---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 2b50d49c108408e1639b5f5f490c2aaafc7bbd82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158953"
---
# <span data-ttu-id="1a0f0-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="1a0f0-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="1a0f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0f0-103">Löscht einen Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="1a0f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a0f0-104">SYNTAX</span></span>

### <span data-ttu-id="1a0f0-105">RouteServerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a0f0-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a0f0-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a0f0-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a0f0-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a0f0-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a0f0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a0f0-108">DESCRIPTION</span></span>
<span data-ttu-id="1a0f0-109">Das **Cmdlet "Remove-AzRouteServer"** löscht einen Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="1a0f0-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="1a0f0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a0f0-110">EXAMPLES</span></span>

### <span data-ttu-id="1a0f0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a0f0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="1a0f0-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1a0f0-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="1a0f0-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1a0f0-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="1a0f0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a0f0-114">PARAMETERS</span></span>

### <span data-ttu-id="1a0f0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a0f0-115">-AsJob</span></span>
<span data-ttu-id="1a0f0-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1a0f0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a0f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0f0-117">-DefaultProfile</span></span>
<span data-ttu-id="1a0f0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a0f0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1a0f0-119">-Force</span></span>
<span data-ttu-id="1a0f0-120">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="1a0f0-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1a0f0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a0f0-121">-InputObject</span></span>
<span data-ttu-id="1a0f0-122">Das Eingabeobjekt des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-122">The route server input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServer
Parameter Sets: RouteServerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0f0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a0f0-123">-PassThru</span></span>
<span data-ttu-id="1a0f0-124">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="1a0f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a0f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a0f0-126">Der Ressourcengruppenname des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-126">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0f0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a0f0-127">-ResourceId</span></span>
<span data-ttu-id="1a0f0-128">Die Ressourcen-ID des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-128">The route server resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0f0-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="1a0f0-129">-RouteServerName</span></span>
<span data-ttu-id="1a0f0-130">Der Name des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-130">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0f0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a0f0-131">-Confirm</span></span>
<span data-ttu-id="1a0f0-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a0f0-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1a0f0-133">-WhatIf</span></span>
<span data-ttu-id="1a0f0-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a0f0-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a0f0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0f0-136">CommonParameters</span></span>
<span data-ttu-id="1a0f0-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0f0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0f0-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a0f0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0f0-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a0f0-139">INPUTS</span></span>

### <span data-ttu-id="1a0f0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1a0f0-140">System.String</span></span>

### <span data-ttu-id="1a0f0-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="1a0f0-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="1a0f0-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a0f0-142">OUTPUTS</span></span>

### <span data-ttu-id="1a0f0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a0f0-143">System.Boolean</span></span>

## <span data-ttu-id="1a0f0-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a0f0-144">NOTES</span></span>

## <span data-ttu-id="1a0f0-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a0f0-145">RELATED LINKS</span></span>
