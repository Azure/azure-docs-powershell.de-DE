---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172628"
---
# <span data-ttu-id="4d9fc-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="4d9fc-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="4d9fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="4d9fc-103">Erstellt einen Endpunkt für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="4d9fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d9fc-104">SYNTAX</span></span>

### <span data-ttu-id="4d9fc-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4d9fc-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d9fc-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="4d9fc-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d9fc-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="4d9fc-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d9fc-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="4d9fc-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d9fc-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="4d9fc-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d9fc-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="4d9fc-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d9fc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d9fc-111">DESCRIPTION</span></span>
<span data-ttu-id="4d9fc-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet erstellt einen Endpunkt für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="4d9fc-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d9fc-113">EXAMPLES</span></span>

### <span data-ttu-id="4d9fc-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d9fc-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="4d9fc-115">Name: workspaceEndpoint-Typ: MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-00000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: Scope : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span><span class="sxs-lookup"><span data-stu-id="4d9fc-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="4d9fc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d9fc-116">PARAMETERS</span></span>

### <span data-ttu-id="4d9fc-117">-Address</span><span class="sxs-lookup"><span data-stu-id="4d9fc-117">-Address</span></span>
<span data-ttu-id="4d9fc-118">Adresse des Endpunkts des Verbindungsmonitors (IP oder Domänenname).</span><span class="sxs-lookup"><span data-stu-id="4d9fc-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="4d9fc-119">-AzureSubnet</span></span>
<span data-ttu-id="4d9fc-120">Azure Subnet Endpoint Switch.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4d9fc-121">-AzureVM</span></span>
<span data-ttu-id="4d9fc-122">Azure VM endpoint switch.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="4d9fc-123">-AzureVNet</span></span>
<span data-ttu-id="4d9fc-124">Azure Vnet-Endpunkt-Schalter.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="4d9fc-125">-CoverageLevel</span></span>
<span data-ttu-id="4d9fc-126">Testabdeckung für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="4d9fc-127">Unterstützte Werte sind "Default", "Low", "BelowAverage", "Average", "AboveAvergae", "Full".</span><span class="sxs-lookup"><span data-stu-id="4d9fc-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d9fc-128">-DefaultProfile</span></span>
<span data-ttu-id="4d9fc-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d9fc-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="4d9fc-130">-ExcludeItem</span></span>
<span data-ttu-id="4d9fc-131">Liste der Elemente, die aus dem Endpunktbereich ausgeschlossen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="4d9fc-132">-ExternalAddress</span></span>
<span data-ttu-id="4d9fc-133">Schalter für externen Adressendpunkt.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="4d9fc-134">-IncludeItem</span></span>
<span data-ttu-id="4d9fc-135">Liste der Elemente, die in den Endbereich aufgenommen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="4d9fc-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="4d9fc-137">Endpunktschalter für MMA Workspace Machine.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="4d9fc-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="4d9fc-139">Endpunktschalter für MMA Workspace Network.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-140">-Name</span><span class="sxs-lookup"><span data-stu-id="4d9fc-140">-Name</span></span>
<span data-ttu-id="4d9fc-141">Der Name des Endpunkts des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-141">The name of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d9fc-142">-ResourceId</span></span>
<span data-ttu-id="4d9fc-143">Ressourcen-ID des Endpunkts des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d9fc-144">-Confirm</span></span>
<span data-ttu-id="4d9fc-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d9fc-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4d9fc-146">-WhatIf</span></span>
<span data-ttu-id="4d9fc-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d9fc-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d9fc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9fc-149">CommonParameters</span></span>
<span data-ttu-id="4d9fc-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9fc-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d9fc-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9fc-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d9fc-152">INPUTS</span></span>

### <span data-ttu-id="4d9fc-153">Keine</span><span class="sxs-lookup"><span data-stu-id="4d9fc-153">None</span></span>

## <span data-ttu-id="4d9fc-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d9fc-154">OUTPUTS</span></span>

### <span data-ttu-id="4d9fc-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="4d9fc-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="4d9fc-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4d9fc-156">NOTES</span></span>

## <span data-ttu-id="4d9fc-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4d9fc-157">RELATED LINKS</span></span>
