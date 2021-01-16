---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379895"
---
# <span data-ttu-id="77758-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="77758-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="77758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77758-102">SYNOPSIS</span></span>
<span data-ttu-id="77758-103">Gibt den Verbindungsmonitor mit dem angegebenen Namen oder die Liste der Verbindungsmonitore zurück.</span><span class="sxs-lookup"><span data-stu-id="77758-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="77758-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77758-104">SYNTAX</span></span>

### <span data-ttu-id="77758-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="77758-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77758-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="77758-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77758-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="77758-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77758-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="77758-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77758-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77758-109">DESCRIPTION</span></span>
<span data-ttu-id="77758-110">Das Get-AzNetworkWatcherConnectionMonitor-Cmdlet gibt den Verbindungsmonitor mit dem angegebenen Namen bzw. der angegebenen ressourcen-ID oder die Liste der Verbindungsmonitore zurück, die dem angegebenen Netzwerküberwachungs- bzw. Netzwerkspeicherort zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="77758-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="77758-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="77758-111">EXAMPLES</span></span>

### <span data-ttu-id="77758-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77758-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="77758-113">Name: cm-ID: /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag: W/"40961b58-e379-4204-a47b-0c47773 ProvisioningState: Succeeded Source : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a 1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/ikgvm", "Port": 0 } Destination : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 12.01.2018 19:19:28 MonitoringStatus : Stopped Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : { "key1": "value1" }</span><span class="sxs-lookup"><span data-stu-id="77758-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="77758-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77758-114">PARAMETERS</span></span>

### <span data-ttu-id="77758-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77758-115">-DefaultProfile</span></span>
<span data-ttu-id="77758-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77758-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77758-117">-Location</span><span class="sxs-lookup"><span data-stu-id="77758-117">-Location</span></span>
<span data-ttu-id="77758-118">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="77758-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="77758-119">-Name</span><span class="sxs-lookup"><span data-stu-id="77758-119">-Name</span></span>
<span data-ttu-id="77758-120">Der Name des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="77758-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77758-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="77758-121">-NetworkWatcher</span></span>
<span data-ttu-id="77758-122">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="77758-122">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77758-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="77758-123">-NetworkWatcherName</span></span>
<span data-ttu-id="77758-124">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="77758-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="77758-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77758-125">-ResourceGroupName</span></span>
<span data-ttu-id="77758-126">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="77758-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="77758-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77758-127">-ResourceId</span></span>
<span data-ttu-id="77758-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="77758-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77758-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77758-129">CommonParameters</span></span>
<span data-ttu-id="77758-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77758-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77758-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77758-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77758-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="77758-132">INPUTS</span></span>

### <span data-ttu-id="77758-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="77758-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="77758-134">System.String</span><span class="sxs-lookup"><span data-stu-id="77758-134">System.String</span></span>

## <span data-ttu-id="77758-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="77758-135">OUTPUTS</span></span>

### <span data-ttu-id="77758-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="77758-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="77758-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="77758-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="77758-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="77758-138">NOTES</span></span>

## <span data-ttu-id="77758-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="77758-139">RELATED LINKS</span></span>
