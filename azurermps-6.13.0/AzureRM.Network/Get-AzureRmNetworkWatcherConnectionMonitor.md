---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3f380135cc6edde875c927dd9d640a10cdf14957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664033"
---
# <span data-ttu-id="f46b7-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f46b7-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="f46b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f46b7-102">SYNOPSIS</span></span>
<span data-ttu-id="f46b7-103">Gibt den Verbindungsmonitor mit dem angegebenen Namen oder der Liste der Verbindungs Monitore zurück.</span><span class="sxs-lookup"><span data-stu-id="f46b7-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f46b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f46b7-104">SYNTAX</span></span>

### <span data-ttu-id="f46b7-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f46b7-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f46b7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f46b7-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f46b7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f46b7-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f46b7-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f46b7-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f46b7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f46b7-109">DESCRIPTION</span></span>
<span data-ttu-id="f46b7-110">Das Get-AzureRmNetworkWatcherConnectionMonitor-Cmdlet gibt den Verbindungsmonitor mit dem angegebenen Namen/der angegebenen Resourcen-oder der Liste der Verbindungs Monitore zurück, die dem angegebenen Netzwerkmonitor/-Standort entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f46b7-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="f46b7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f46b7-111">EXAMPLES</span></span>

### <span data-ttu-id="f46b7-112">Beispiel 1: Abrufen des Verbindungs Monitors anhand des Namens an der angegebenen Position</span><span class="sxs-lookup"><span data-stu-id="f46b7-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="f46b7-113">In diesem Beispiel wird der Verbindungsmonitor über den Namen an der angegebenen Position abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f46b7-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="f46b7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f46b7-114">PARAMETERS</span></span>

### <span data-ttu-id="f46b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46b7-115">-DefaultProfile</span></span>
<span data-ttu-id="f46b7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f46b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46b7-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="f46b7-117">-Location</span></span>
<span data-ttu-id="f46b7-118">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="f46b7-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f46b7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f46b7-119">-Name</span></span>
<span data-ttu-id="f46b7-120">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="f46b7-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="f46b7-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f46b7-121">-NetworkWatcher</span></span>
<span data-ttu-id="f46b7-122">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="f46b7-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="f46b7-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f46b7-123">-NetworkWatcherName</span></span>
<span data-ttu-id="f46b7-124">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="f46b7-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="f46b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f46b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="f46b7-126">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f46b7-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f46b7-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f46b7-127">-ResourceId</span></span>
<span data-ttu-id="f46b7-128">Die Ressourcen-ID des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="f46b7-128">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="f46b7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46b7-129">CommonParameters</span></span>
<span data-ttu-id="f46b7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46b7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46b7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46b7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46b7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f46b7-132">INPUTS</span></span>

### <span data-ttu-id="f46b7-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f46b7-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f46b7-134">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f46b7-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="f46b7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f46b7-135">System.String</span></span>

## <span data-ttu-id="f46b7-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f46b7-136">OUTPUTS</span></span>

### <span data-ttu-id="f46b7-137">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="f46b7-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="f46b7-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f46b7-138">NOTES</span></span>
<span data-ttu-id="f46b7-139">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="f46b7-139">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="f46b7-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f46b7-140">RELATED LINKS</span></span>

[<span data-ttu-id="f46b7-141">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f46b7-141">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="f46b7-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f46b7-142">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="f46b7-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f46b7-143">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="f46b7-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f46b7-144">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="f46b7-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f46b7-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="f46b7-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f46b7-146">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="f46b7-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f46b7-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="f46b7-148">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f46b7-148">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="f46b7-149">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f46b7-149">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="f46b7-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f46b7-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="f46b7-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f46b7-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="f46b7-152">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f46b7-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="f46b7-153">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f46b7-153">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f46b7-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f46b7-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="f46b7-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f46b7-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f46b7-156">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f46b7-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f46b7-157">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f46b7-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f46b7-158">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f46b7-158">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f46b7-159">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f46b7-159">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="f46b7-160">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f46b7-160">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="f46b7-161">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f46b7-161">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="f46b7-162">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f46b7-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="f46b7-163">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f46b7-163">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f46b7-164">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f46b7-164">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="f46b7-165">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f46b7-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="f46b7-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f46b7-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="f46b7-167">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f46b7-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
