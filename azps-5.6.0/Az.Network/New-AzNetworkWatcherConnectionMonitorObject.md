---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 78de7eb3e8adbda34e53b5a74036a047ddcd4a1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921872"
---
# <span data-ttu-id="049de-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="049de-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="049de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="049de-102">SYNOPSIS</span></span>
<span data-ttu-id="049de-103">Erstellen Sie ein V2-Objekt für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="049de-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="049de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="049de-104">SYNTAX</span></span>

### <span data-ttu-id="049de-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="049de-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="049de-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="049de-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="049de-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="049de-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="049de-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="049de-108">DESCRIPTION</span></span>
<span data-ttu-id="049de-109">Das New-AzNetworkWatcherConnectionMonitorObject-Cmdlet erstellt ein V2-Verbindungsmonitorobjekt.</span><span class="sxs-lookup"><span data-stu-id="049de-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="049de-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="049de-110">EXAMPLES</span></span>

### <span data-ttu-id="049de-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="049de-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="049de-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }</span><span class="sxs-lookup"><span data-stu-id="049de-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="049de-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="049de-113">PARAMETERS</span></span>

### <span data-ttu-id="049de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049de-114">-DefaultProfile</span></span>
<span data-ttu-id="049de-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="049de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="049de-116">-Location</span><span class="sxs-lookup"><span data-stu-id="049de-116">-Location</span></span>
<span data-ttu-id="049de-117">Speicherort des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="049de-117">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049de-118">-Name</span><span class="sxs-lookup"><span data-stu-id="049de-118">-Name</span></span>
<span data-ttu-id="049de-119">Der Name des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="049de-119">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049de-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="049de-120">-NetworkWatcher</span></span>
<span data-ttu-id="049de-121">Die Netzwerkwächterressource.</span><span class="sxs-lookup"><span data-stu-id="049de-121">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049de-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="049de-122">-NetworkWatcherName</span></span>
<span data-ttu-id="049de-123">Der Name des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="049de-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049de-124">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="049de-124">-Note</span></span>
<span data-ttu-id="049de-125">Notizen, die mit dem Verbindungsmonitor verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="049de-125">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="049de-126">-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="049de-126">-Output</span></span>
<span data-ttu-id="049de-127">Beschreibt die Ausgabeziele eines Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="049de-127">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049de-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="049de-128">-ResourceGroupName</span></span>
<span data-ttu-id="049de-129">Der Name der Ressourcengruppe "Netzwerkwächter".</span><span class="sxs-lookup"><span data-stu-id="049de-129">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049de-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="049de-130">-Tag</span></span>
<span data-ttu-id="049de-131">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="049de-131">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="049de-132">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="049de-132">-TestGroup</span></span>
<span data-ttu-id="049de-133">Die Liste der Testgruppen.</span><span class="sxs-lookup"><span data-stu-id="049de-133">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049de-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="049de-134">-Confirm</span></span>
<span data-ttu-id="049de-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="049de-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="049de-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="049de-136">-WhatIf</span></span>
<span data-ttu-id="049de-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="049de-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="049de-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="049de-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="049de-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049de-139">CommonParameters</span></span>
<span data-ttu-id="049de-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="049de-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049de-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="049de-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049de-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="049de-142">INPUTS</span></span>

### <span data-ttu-id="049de-143">Keine</span><span class="sxs-lookup"><span data-stu-id="049de-143">None</span></span>

## <span data-ttu-id="049de-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="049de-144">OUTPUTS</span></span>

### <span data-ttu-id="049de-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="049de-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="049de-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="049de-146">NOTES</span></span>

## <span data-ttu-id="049de-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="049de-147">RELATED LINKS</span></span>
