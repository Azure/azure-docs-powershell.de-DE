---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305387"
---
# <span data-ttu-id="d6f68-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="d6f68-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="d6f68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f68-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f68-103">Setzt das RoutingState einer VirtualHub-Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="d6f68-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="d6f68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6f68-104">SYNTAX</span></span>

### <span data-ttu-id="d6f68-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6f68-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f68-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f68-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f68-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d6f68-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f68-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6f68-108">DESCRIPTION</span></span>
<span data-ttu-id="d6f68-109">Setzt den Routingstatus einer vorhandenen VirtualHub-Ressource nur zurück, wenn der Routingstatus des virtuellen Hubs nicht bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d6f68-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="d6f68-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6f68-110">EXAMPLES</span></span>

### <span data-ttu-id="d6f68-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6f68-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="d6f68-112">Setzen Sie den Routingstatus des virtuellen Hubs mithilfe von ResourceGroupName und ResourceName zurück.</span><span class="sxs-lookup"><span data-stu-id="d6f68-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="d6f68-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d6f68-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="d6f68-114">Setzen Sie den Routingstatus des virtuellen Hubs mit seiner ResourceId zurück.</span><span class="sxs-lookup"><span data-stu-id="d6f68-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="d6f68-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d6f68-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="d6f68-116">Setzen Sie den Routingstatus des virtuellen Hubs mithilfe eines Eingabeobjekts zurück.</span><span class="sxs-lookup"><span data-stu-id="d6f68-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="d6f68-117">Das Eingabeobjekt ist vom Typ "PSVirtualHub".</span><span class="sxs-lookup"><span data-stu-id="d6f68-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="d6f68-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d6f68-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="d6f68-119">Ein vorhandenes virtuelles Hubobjekt kann abgerufen und dann als Eingabeobjekt an Reset-AzHubRouter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d6f68-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="d6f68-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6f68-120">PARAMETERS</span></span>

### <span data-ttu-id="d6f68-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6f68-121">-AsJob</span></span>
<span data-ttu-id="d6f68-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d6f68-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6f68-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f68-123">-DefaultProfile</span></span>
<span data-ttu-id="d6f68-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6f68-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f68-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d6f68-125">-Force</span></span>
<span data-ttu-id="d6f68-126">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="d6f68-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d6f68-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6f68-127">-InputObject</span></span>
<span data-ttu-id="d6f68-128">Das zu ändernde virtuelle Hubobjekt.</span><span class="sxs-lookup"><span data-stu-id="d6f68-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f68-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d6f68-129">-Name</span></span>
<span data-ttu-id="d6f68-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d6f68-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f68-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f68-131">-ResourceGroupName</span></span>
<span data-ttu-id="d6f68-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d6f68-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f68-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f68-133">-ResourceId</span></span>
<span data-ttu-id="d6f68-134">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6f68-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f68-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6f68-135">-Confirm</span></span>
<span data-ttu-id="d6f68-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6f68-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f68-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d6f68-137">-WhatIf</span></span>
<span data-ttu-id="d6f68-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6f68-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f68-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6f68-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f68-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f68-140">CommonParameters</span></span>
<span data-ttu-id="d6f68-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f68-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f68-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f68-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f68-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6f68-143">INPUTS</span></span>

### <span data-ttu-id="d6f68-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d6f68-144">System.String</span></span>

### <span data-ttu-id="d6f68-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d6f68-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="d6f68-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6f68-146">OUTPUTS</span></span>

### <span data-ttu-id="d6f68-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d6f68-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="d6f68-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d6f68-148">NOTES</span></span>

## <span data-ttu-id="d6f68-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d6f68-149">RELATED LINKS</span></span>

[<span data-ttu-id="d6f68-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d6f68-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
