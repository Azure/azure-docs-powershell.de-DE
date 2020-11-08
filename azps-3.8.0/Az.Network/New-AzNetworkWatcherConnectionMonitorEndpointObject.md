---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995731"
---
# <span data-ttu-id="a0032-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a0032-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="a0032-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0032-102">SYNOPSIS</span></span>
<span data-ttu-id="a0032-103">Erstellt den Endpunkt des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="a0032-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="a0032-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0032-104">SYNTAX</span></span>

### <span data-ttu-id="a0032-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0032-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0032-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="a0032-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0032-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0032-107">DESCRIPTION</span></span>
<span data-ttu-id="a0032-108">New-AzNetworkWatcherConnectionMonitorEndpointObject-Cmdlet erstellt den Endpunkt des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="a0032-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="a0032-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0032-109">EXAMPLES</span></span>

### <span data-ttu-id="a0032-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0032-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="a0032-111">Name: workspaceEndpoint Resourcen:/Subscriptions/00000000-0000-0000-0000-000000000000/ResourceGroups/myresourceGroup/Providers/Microsoft.OperationalInsights/Workspaces/myworkspace Address: Filter: {"Type": "include"; "Items": [{"Type": "AgentAddress AbschnittFür"; "Address": "Win-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="a0032-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="a0032-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0032-112">PARAMETERS</span></span>

### <span data-ttu-id="a0032-113">-Adresse</span><span class="sxs-lookup"><span data-stu-id="a0032-113">-Address</span></span>
<span data-ttu-id="a0032-114">Die Adresse des Verbindungsmonitor Endpunkts (IP-oder Domänenname).</span><span class="sxs-lookup"><span data-stu-id="a0032-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0032-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0032-115">-DefaultProfile</span></span>
<span data-ttu-id="a0032-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0032-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0032-117">-Filter Item</span><span class="sxs-lookup"><span data-stu-id="a0032-117">-FilterItem</span></span>
<span data-ttu-id="a0032-118">Liste der Elemente im Filter.</span><span class="sxs-lookup"><span data-stu-id="a0032-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0032-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="a0032-119">-FilterType</span></span>
<span data-ttu-id="a0032-120">Das Verhalten des Endpunkt Filters.</span><span class="sxs-lookup"><span data-stu-id="a0032-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="a0032-121">Derzeit wird nur "include" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0032-121">Currently only 'Include' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0032-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a0032-122">-Name</span></span>
<span data-ttu-id="a0032-123">Der Name des Verbindungsmonitor Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="a0032-123">The name of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0032-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a0032-124">-ResourceId</span></span>
<span data-ttu-id="a0032-125">Die Ressourcen-ID des Verbindungsmonitor-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="a0032-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0032-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0032-126">-Confirm</span></span>
<span data-ttu-id="a0032-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0032-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0032-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0032-128">-WhatIf</span></span>
<span data-ttu-id="a0032-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0032-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0032-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0032-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0032-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0032-131">CommonParameters</span></span>
<span data-ttu-id="a0032-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0032-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0032-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0032-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0032-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0032-134">INPUTS</span></span>

### <span data-ttu-id="a0032-135">Keine</span><span class="sxs-lookup"><span data-stu-id="a0032-135">None</span></span>

## <span data-ttu-id="a0032-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0032-136">OUTPUTS</span></span>

### <span data-ttu-id="a0032-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a0032-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="a0032-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0032-138">NOTES</span></span>

## <span data-ttu-id="a0032-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0032-139">RELATED LINKS</span></span>
