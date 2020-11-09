---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302686"
---
# <span data-ttu-id="76c43-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="76c43-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="76c43-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76c43-102">SYNOPSIS</span></span>
<span data-ttu-id="76c43-103">Erstellen Sie eine Testgruppe für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="76c43-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="76c43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76c43-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76c43-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76c43-105">DESCRIPTION</span></span>
<span data-ttu-id="76c43-106">Das New-AzNetworkWatcherConnectionMonitorTestGroupObject-Cmdlet erstellt eine Testgruppe für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="76c43-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="76c43-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76c43-107">EXAMPLES</span></span>

### <span data-ttu-id="76c43-108">Beispiel 1: Erstellen einer Testgruppe mit 2 testConfigurations-, w-Quell-und 2-zielendpunkten</span><span class="sxs-lookup"><span data-stu-id="76c43-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="76c43-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="76c43-109">PARAMETERS</span></span>

### <span data-ttu-id="76c43-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c43-110">-DefaultProfile</span></span>
<span data-ttu-id="76c43-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76c43-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c43-112">-Ziel</span><span class="sxs-lookup"><span data-stu-id="76c43-112">-Destination</span></span>
<span data-ttu-id="76c43-113">Liste der Zielendpunkte</span><span class="sxs-lookup"><span data-stu-id="76c43-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="76c43-114">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="76c43-114">-Disable</span></span>
<span data-ttu-id="76c43-115">Flag, das angibt, ob Testgruppe deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="76c43-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="76c43-116">-Name</span><span class="sxs-lookup"><span data-stu-id="76c43-116">-Name</span></span>
<span data-ttu-id="76c43-117">Der Name der Testgruppe.</span><span class="sxs-lookup"><span data-stu-id="76c43-117">The test group name.</span></span>

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

### <span data-ttu-id="76c43-118">-Source</span><span class="sxs-lookup"><span data-stu-id="76c43-118">-Source</span></span>
<span data-ttu-id="76c43-119">Liste der Quell Endpunkte</span><span class="sxs-lookup"><span data-stu-id="76c43-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="76c43-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="76c43-120">-TestConfiguration</span></span>
<span data-ttu-id="76c43-121">Liste der Testkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="76c43-121">List of test configuration.</span></span>

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

### <span data-ttu-id="76c43-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76c43-122">-Confirm</span></span>
<span data-ttu-id="76c43-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76c43-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c43-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c43-124">-WhatIf</span></span>
<span data-ttu-id="76c43-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76c43-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c43-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76c43-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c43-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c43-127">CommonParameters</span></span>
<span data-ttu-id="76c43-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c43-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c43-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76c43-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c43-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76c43-130">INPUTS</span></span>

### <span data-ttu-id="76c43-131">Keine</span><span class="sxs-lookup"><span data-stu-id="76c43-131">None</span></span>

## <span data-ttu-id="76c43-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76c43-132">OUTPUTS</span></span>

### <span data-ttu-id="76c43-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="76c43-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="76c43-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="76c43-134">NOTES</span></span>

## <span data-ttu-id="76c43-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76c43-135">RELATED LINKS</span></span>
