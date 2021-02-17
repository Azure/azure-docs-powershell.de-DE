---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172609"
---
# <span data-ttu-id="96408-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="96408-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="96408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96408-102">SYNOPSIS</span></span>
<span data-ttu-id="96408-103">Erstellen Sie eine Testgruppe für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="96408-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="96408-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96408-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96408-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96408-105">DESCRIPTION</span></span>
<span data-ttu-id="96408-106">Das New-AzNetworkWatcherConnectionMonitorTestGroupObject erstellt eine Testgruppe für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="96408-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="96408-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="96408-107">EXAMPLES</span></span>

### <span data-ttu-id="96408-108">Beispiel 1: Erstellen einer Testgruppe mit 2 testConfigurations, w Quell- und 2 Zielendpunkten</span><span class="sxs-lookup"><span data-stu-id="96408-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="96408-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96408-109">PARAMETERS</span></span>

### <span data-ttu-id="96408-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96408-110">-DefaultProfile</span></span>
<span data-ttu-id="96408-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96408-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96408-112">-Destination</span><span class="sxs-lookup"><span data-stu-id="96408-112">-Destination</span></span>
<span data-ttu-id="96408-113">Liste der Zielendpunkte.</span><span class="sxs-lookup"><span data-stu-id="96408-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="96408-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="96408-114">-Disable</span></span>
<span data-ttu-id="96408-115">Flag, das angibt, ob die Testgruppe deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="96408-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="96408-116">-Name</span><span class="sxs-lookup"><span data-stu-id="96408-116">-Name</span></span>
<span data-ttu-id="96408-117">Der Name der Testgruppe.</span><span class="sxs-lookup"><span data-stu-id="96408-117">The test group name.</span></span>

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

### <span data-ttu-id="96408-118">-Source</span><span class="sxs-lookup"><span data-stu-id="96408-118">-Source</span></span>
<span data-ttu-id="96408-119">Liste der Quellendpunkte.</span><span class="sxs-lookup"><span data-stu-id="96408-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="96408-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="96408-120">-TestConfiguration</span></span>
<span data-ttu-id="96408-121">Liste der Testkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="96408-121">List of test configuration.</span></span>

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

### <span data-ttu-id="96408-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96408-122">-Confirm</span></span>
<span data-ttu-id="96408-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96408-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96408-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="96408-124">-WhatIf</span></span>
<span data-ttu-id="96408-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96408-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96408-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96408-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96408-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96408-127">CommonParameters</span></span>
<span data-ttu-id="96408-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96408-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96408-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96408-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96408-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="96408-130">INPUTS</span></span>

### <span data-ttu-id="96408-131">Keine</span><span class="sxs-lookup"><span data-stu-id="96408-131">None</span></span>

## <span data-ttu-id="96408-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="96408-132">OUTPUTS</span></span>

### <span data-ttu-id="96408-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="96408-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="96408-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="96408-134">NOTES</span></span>

## <span data-ttu-id="96408-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="96408-135">RELATED LINKS</span></span>
