---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301455"
---
# <span data-ttu-id="1991b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="1991b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="1991b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1991b-102">SYNOPSIS</span></span>
<span data-ttu-id="1991b-103">Erstellt den Endpunkt des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="1991b-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="1991b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1991b-104">SYNTAX</span></span>

### <span data-ttu-id="1991b-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1991b-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1991b-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="1991b-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1991b-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="1991b-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1991b-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="1991b-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1991b-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="1991b-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1991b-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="1991b-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1991b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1991b-111">DESCRIPTION</span></span>
<span data-ttu-id="1991b-112">New-AzNetworkWatcherConnectionMonitorEndpointObject-Cmdlet erstellt den Endpunkt des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="1991b-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="1991b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1991b-113">EXAMPLES</span></span>

### <span data-ttu-id="1991b-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1991b-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="1991b-115">Name: workspaceEndpoint Typ: MMAWorkspaceMachine-Ressourcen-Nr:/Subscriptions/00000000-0000-0000-0000-000000000000/ResourceGroups/myresourceGroup/Providers/Microsoft.OperationalInsights/Workspaces/myworkspace-Adresse: Scope: {"include": [{"Address": "Win-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="1991b-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="1991b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="1991b-116">PARAMETERS</span></span>

### <span data-ttu-id="1991b-117">-Adresse</span><span class="sxs-lookup"><span data-stu-id="1991b-117">-Address</span></span>
<span data-ttu-id="1991b-118">Die Adresse des Verbindungsmonitor Endpunkts (IP-oder Domänenname).</span><span class="sxs-lookup"><span data-stu-id="1991b-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

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

### <span data-ttu-id="1991b-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="1991b-119">-AzureSubnet</span></span>
<span data-ttu-id="1991b-120">Azure-Subnet-Endpunkt Schalter</span><span class="sxs-lookup"><span data-stu-id="1991b-120">Azure Subnet endpoint switch.</span></span>

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

### <span data-ttu-id="1991b-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1991b-121">-AzureVM</span></span>
<span data-ttu-id="1991b-122">Azure VM-Endpunkt Schalter</span><span class="sxs-lookup"><span data-stu-id="1991b-122">Azure VM endpoint switch.</span></span>

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

### <span data-ttu-id="1991b-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="1991b-123">-AzureVNet</span></span>
<span data-ttu-id="1991b-124">Azure vnet-Endpunkt Schalter</span><span class="sxs-lookup"><span data-stu-id="1991b-124">Azure Vnet endpoint switch.</span></span>

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

### <span data-ttu-id="1991b-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="1991b-125">-CoverageLevel</span></span>
<span data-ttu-id="1991b-126">Test Abdeckung für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="1991b-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="1991b-127">Unterstützte Werte sind Standard, Low, BelowAverage, Average, AboveAvergae, Full.</span><span class="sxs-lookup"><span data-stu-id="1991b-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

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

### <span data-ttu-id="1991b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1991b-128">-DefaultProfile</span></span>
<span data-ttu-id="1991b-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1991b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1991b-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="1991b-130">-ExcludeItem</span></span>
<span data-ttu-id="1991b-131">Liste der Elemente, die vom Endpunkt Bereich ausgeschlossen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1991b-131">List of items which need to be excluded from endpoint scope.</span></span>

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

### <span data-ttu-id="1991b-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="1991b-132">-ExternalAddress</span></span>
<span data-ttu-id="1991b-133">Endpunkt Schalter für externe Adressen.</span><span class="sxs-lookup"><span data-stu-id="1991b-133">External Address endpoint switch.</span></span>

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

### <span data-ttu-id="1991b-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="1991b-134">-IncludeItem</span></span>
<span data-ttu-id="1991b-135">Liste der Elemente, die in den endpont-Bereich aufgenommen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1991b-135">List of items which need to be included into endpont scope.</span></span>

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

### <span data-ttu-id="1991b-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="1991b-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="1991b-137">MMA-Arbeitsbereichs Computer Endpunkt Schalter</span><span class="sxs-lookup"><span data-stu-id="1991b-137">MMA Workspace Machine endpoint switch.</span></span>

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

### <span data-ttu-id="1991b-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="1991b-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="1991b-139">MMA-Workspace-Netzwerkendpunkt Schalter</span><span class="sxs-lookup"><span data-stu-id="1991b-139">MMA Workspace Network endpoint switch.</span></span>

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

### <span data-ttu-id="1991b-140">-Name</span><span class="sxs-lookup"><span data-stu-id="1991b-140">-Name</span></span>
<span data-ttu-id="1991b-141">Der Name des Verbindungsmonitor Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="1991b-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="1991b-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1991b-142">-ResourceId</span></span>
<span data-ttu-id="1991b-143">Die Ressourcen-ID des Verbindungsmonitor-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="1991b-143">Resource ID of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="1991b-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1991b-144">-Confirm</span></span>
<span data-ttu-id="1991b-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1991b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1991b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1991b-146">-WhatIf</span></span>
<span data-ttu-id="1991b-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1991b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1991b-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1991b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1991b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1991b-149">CommonParameters</span></span>
<span data-ttu-id="1991b-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1991b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1991b-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1991b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1991b-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1991b-152">INPUTS</span></span>

### <span data-ttu-id="1991b-153">Keine</span><span class="sxs-lookup"><span data-stu-id="1991b-153">None</span></span>

## <span data-ttu-id="1991b-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1991b-154">OUTPUTS</span></span>

### <span data-ttu-id="1991b-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="1991b-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="1991b-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="1991b-156">NOTES</span></span>

## <span data-ttu-id="1991b-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1991b-157">RELATED LINKS</span></span>
