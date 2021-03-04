---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: 4ab9feb0d99bc808cfabb481baf81bb12e050f28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921819"
---
# <span data-ttu-id="2fa79-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="2fa79-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="2fa79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa79-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa79-103">Erstellen Sie eine Testgruppe für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="2fa79-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="2fa79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fa79-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa79-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fa79-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa79-106">Das New-AzNetworkWatcherConnectionMonitorTestGroupObject-Cmdlet erstellt eine Testgruppe für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="2fa79-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="2fa79-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fa79-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa79-108">Beispiel 1: Erstellen einer Testgruppe mit 2 testConfigurations, w Source und 2 Zielendpunkten</span><span class="sxs-lookup"><span data-stu-id="2fa79-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="2fa79-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2fa79-109">PARAMETERS</span></span>

### <span data-ttu-id="2fa79-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa79-110">-DefaultProfile</span></span>
<span data-ttu-id="2fa79-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fa79-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fa79-112">-Ziel</span><span class="sxs-lookup"><span data-stu-id="2fa79-112">-Destination</span></span>
<span data-ttu-id="2fa79-113">Liste der Zielendpunkte.</span><span class="sxs-lookup"><span data-stu-id="2fa79-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="2fa79-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="2fa79-114">-Disable</span></span>
<span data-ttu-id="2fa79-115">Kennzeichnung, die angibt, ob die Testgruppe deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2fa79-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="2fa79-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2fa79-116">-Name</span></span>
<span data-ttu-id="2fa79-117">Der Name der Testgruppe.</span><span class="sxs-lookup"><span data-stu-id="2fa79-117">The test group name.</span></span>

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

### <span data-ttu-id="2fa79-118">-Source</span><span class="sxs-lookup"><span data-stu-id="2fa79-118">-Source</span></span>
<span data-ttu-id="2fa79-119">Liste der Quellendpunkte.</span><span class="sxs-lookup"><span data-stu-id="2fa79-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="2fa79-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fa79-120">-TestConfiguration</span></span>
<span data-ttu-id="2fa79-121">Liste der Testkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2fa79-121">List of test configuration.</span></span>

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

### <span data-ttu-id="2fa79-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fa79-122">-Confirm</span></span>
<span data-ttu-id="2fa79-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fa79-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa79-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa79-124">-WhatIf</span></span>
<span data-ttu-id="2fa79-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fa79-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa79-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fa79-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa79-127">CommonParameters</span></span>
<span data-ttu-id="2fa79-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa79-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fa79-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa79-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fa79-130">INPUTS</span></span>

### <span data-ttu-id="2fa79-131">Keine</span><span class="sxs-lookup"><span data-stu-id="2fa79-131">None</span></span>

## <span data-ttu-id="2fa79-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fa79-132">OUTPUTS</span></span>

### <span data-ttu-id="2fa79-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="2fa79-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="2fa79-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2fa79-134">NOTES</span></span>

## <span data-ttu-id="2fa79-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2fa79-135">RELATED LINKS</span></span>
