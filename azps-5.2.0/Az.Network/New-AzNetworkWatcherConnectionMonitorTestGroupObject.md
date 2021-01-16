---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301728"
---
# <span data-ttu-id="e2ea3-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="e2ea3-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="e2ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ea3-103">Erstellen Sie eine Testgruppe für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="e2ea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2ea3-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2ea3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="e2ea3-106">Das New-AzNetworkWatcherConnectionMonitorTestGroupObject erstellt eine Testgruppe für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="e2ea3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e2ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="e2ea3-108">Beispiel 1: Erstellen einer Testgruppe mit 2 testConfigurations, w Quell- und 2 Zielendpunkten</span><span class="sxs-lookup"><span data-stu-id="e2ea3-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="e2ea3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2ea3-109">PARAMETERS</span></span>

### <span data-ttu-id="e2ea3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ea3-110">-DefaultProfile</span></span>
<span data-ttu-id="e2ea3-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ea3-112">-Destination</span><span class="sxs-lookup"><span data-stu-id="e2ea3-112">-Destination</span></span>
<span data-ttu-id="e2ea3-113">Liste der Zielendpunkte.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ea3-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="e2ea3-114">-Disable</span></span>
<span data-ttu-id="e2ea3-115">Flag, das angibt, ob die Testgruppe deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="e2ea3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e2ea3-116">-Name</span></span>
<span data-ttu-id="e2ea3-117">Der Name der Testgruppe.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-117">The test group name.</span></span>

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

### <span data-ttu-id="e2ea3-118">-Source</span><span class="sxs-lookup"><span data-stu-id="e2ea3-118">-Source</span></span>
<span data-ttu-id="e2ea3-119">Liste der Quellendpunkte.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ea3-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2ea3-120">-TestConfiguration</span></span>
<span data-ttu-id="e2ea3-121">Liste der Testkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ea3-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2ea3-122">-Confirm</span></span>
<span data-ttu-id="e2ea3-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ea3-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e2ea3-124">-WhatIf</span></span>
<span data-ttu-id="e2ea3-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ea3-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ea3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ea3-127">CommonParameters</span></span>
<span data-ttu-id="e2ea3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ea3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ea3-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2ea3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ea3-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e2ea3-130">INPUTS</span></span>

### <span data-ttu-id="e2ea3-131">Keine</span><span class="sxs-lookup"><span data-stu-id="e2ea3-131">None</span></span>

## <span data-ttu-id="e2ea3-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e2ea3-132">OUTPUTS</span></span>

### <span data-ttu-id="e2ea3-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="e2ea3-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="e2ea3-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e2ea3-134">NOTES</span></span>

## <span data-ttu-id="e2ea3-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e2ea3-135">RELATED LINKS</span></span>
