---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166226"
---
# <span data-ttu-id="cc7c2-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="cc7c2-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="cc7c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7c2-103">Setzt die RoutingState einer VirtualHub-Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="cc7c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc7c2-104">SYNTAX</span></span>

### <span data-ttu-id="cc7c2-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc7c2-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc7c2-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="cc7c2-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc7c2-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="cc7c2-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc7c2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc7c2-108">DESCRIPTION</span></span>
<span data-ttu-id="cc7c2-109">Setzt den Routingstatus einer vorhandenen VirtualHub-Ressource nur dann zurück, wenn der Routingstatus des virtuellen Hubs nicht bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="cc7c2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc7c2-110">EXAMPLES</span></span>

### <span data-ttu-id="cc7c2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc7c2-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="cc7c2-112">Setzen Sie den Routingstatus des virtuellen Hubs mithilfe von ResourceGroupName und resourceName zurück.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="cc7c2-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cc7c2-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="cc7c2-114">Zurücksetzen des Routing Zustands des virtuellen Hubs mithilfe der zugehörigen Quell-Nr.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="cc7c2-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cc7c2-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="cc7c2-116">Setzen Sie den Routingstatus des virtuellen Hubs mithilfe eines Eingabeobjekts zurück.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="cc7c2-117">Das Eingabeobjekt ist vom Typ PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="cc7c2-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="cc7c2-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="cc7c2-119">Ein vorhandenes virtuelles Hub-Objekt kann abgerufen und dann als Eingabeobjekt an Reset-AzHubRouter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="cc7c2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc7c2-120">PARAMETERS</span></span>

### <span data-ttu-id="cc7c2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc7c2-121">-AsJob</span></span>
<span data-ttu-id="cc7c2-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cc7c2-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc7c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7c2-123">-DefaultProfile</span></span>
<span data-ttu-id="cc7c2-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc7c2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cc7c2-125">-Force</span></span>
<span data-ttu-id="cc7c2-126">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="cc7c2-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cc7c2-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc7c2-127">-InputObject</span></span>
<span data-ttu-id="cc7c2-128">Das virtuelle Hub-Objekt, das geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="cc7c2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="cc7c2-129">-Name</span></span>
<span data-ttu-id="cc7c2-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-130">The resource name.</span></span>

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

### <span data-ttu-id="cc7c2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc7c2-131">-ResourceGroupName</span></span>
<span data-ttu-id="cc7c2-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-132">The resource group name.</span></span>

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

### <span data-ttu-id="cc7c2-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cc7c2-133">-ResourceId</span></span>
<span data-ttu-id="cc7c2-134">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="cc7c2-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc7c2-135">-Confirm</span></span>
<span data-ttu-id="cc7c2-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc7c2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc7c2-137">-WhatIf</span></span>
<span data-ttu-id="cc7c2-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc7c2-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc7c2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7c2-140">CommonParameters</span></span>
<span data-ttu-id="cc7c2-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7c2-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc7c2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7c2-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc7c2-143">INPUTS</span></span>

### <span data-ttu-id="cc7c2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cc7c2-144">System.String</span></span>

### <span data-ttu-id="cc7c2-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cc7c2-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="cc7c2-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc7c2-146">OUTPUTS</span></span>

### <span data-ttu-id="cc7c2-147">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cc7c2-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="cc7c2-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc7c2-148">NOTES</span></span>

## <span data-ttu-id="cc7c2-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc7c2-149">RELATED LINKS</span></span>

[<span data-ttu-id="cc7c2-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cc7c2-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
