---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003518"
---
# <span data-ttu-id="3a244-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3a244-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3a244-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a244-102">SYNOPSIS</span></span>
<span data-ttu-id="3a244-103">Gibt den Verbindungsmonitor mit dem angegebenen Namen oder der Liste der Verbindungs Monitore zurück.</span><span class="sxs-lookup"><span data-stu-id="3a244-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="3a244-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a244-104">SYNTAX</span></span>

### <span data-ttu-id="3a244-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a244-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a244-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3a244-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a244-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3a244-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a244-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3a244-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a244-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a244-109">DESCRIPTION</span></span>
<span data-ttu-id="3a244-110">Das Get-AzNetworkWatcherConnectionMonitor-Cmdlet gibt den Verbindungsmonitor mit dem angegebenen Namen/der angegebenen Resourcen-oder der Liste der Verbindungs Monitore zurück, die dem angegebenen Netzwerkmonitor/-Standort entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3a244-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="3a244-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a244-111">EXAMPLES</span></span>

### <span data-ttu-id="3a244-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a244-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="3a244-113">Name: cm ID:/Subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/Providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionmonitors/cm ETag: W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState: Nachfolge Quelle: {"Resource-ID": "/Subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/Anbieter/Microsoft. C ompute/virtualMachines/irinavm"; "Port": 0} Ziel: {"Adresse": "Google.com"; "Port": 80} MonitoringIntervalInSeconds: 60 Autostart: true Startwert: 1/12/2018 7:19:28 Uhr MonitoringStatus: gestoppter Standort: centraluseuap Typ: Microsoft. Network/networkWatchers-connectionMonitors-Tags: {"key1": "Value1"}</span><span class="sxs-lookup"><span data-stu-id="3a244-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="3a244-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a244-114">PARAMETERS</span></span>

### <span data-ttu-id="3a244-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a244-115">-DefaultProfile</span></span>
<span data-ttu-id="3a244-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a244-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a244-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="3a244-117">-Location</span></span>
<span data-ttu-id="3a244-118">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="3a244-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3a244-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3a244-119">-Name</span></span>
<span data-ttu-id="3a244-120">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="3a244-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="3a244-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a244-121">-NetworkWatcher</span></span>
<span data-ttu-id="3a244-122">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="3a244-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="3a244-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3a244-123">-NetworkWatcherName</span></span>
<span data-ttu-id="3a244-124">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="3a244-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="3a244-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a244-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a244-126">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3a244-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3a244-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3a244-127">-ResourceId</span></span>
<span data-ttu-id="3a244-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3a244-128">Resource ID.</span></span>

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

### <span data-ttu-id="3a244-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a244-129">CommonParameters</span></span>
<span data-ttu-id="3a244-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a244-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a244-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a244-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a244-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a244-132">INPUTS</span></span>

### <span data-ttu-id="3a244-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a244-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3a244-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3a244-134">System.String</span></span>

## <span data-ttu-id="3a244-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a244-135">OUTPUTS</span></span>

### <span data-ttu-id="3a244-136">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="3a244-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="3a244-137">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="3a244-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="3a244-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a244-138">NOTES</span></span>

## <span data-ttu-id="3a244-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a244-139">RELATED LINKS</span></span>
