---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: d8ab2ce24db9c6ab07989dc5a4a45b8bfca8fc78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841572"
---
# <span data-ttu-id="de33c-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de33c-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="de33c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de33c-102">SYNOPSIS</span></span>
<span data-ttu-id="de33c-103">Gibt den Verbindungsmonitor mit dem angegebenen Namen oder der Liste der Verbindungs Monitore zurück.</span><span class="sxs-lookup"><span data-stu-id="de33c-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="de33c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de33c-104">SYNTAX</span></span>

### <span data-ttu-id="de33c-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="de33c-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="de33c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="de33c-106">SetByName</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="de33c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="de33c-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="de33c-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="de33c-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="de33c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de33c-109">DESCRIPTION</span></span>
<span data-ttu-id="de33c-110">Das Get-AzNetworkWatcherConnectionMonitor-Cmdlet gibt den Verbindungsmonitor mit dem angegebenen Namen/der angegebenen Resourcen-oder der Liste der Verbindungs Monitore zurück, die dem angegebenen Netzwerkmonitor/-Standort entsprechen.</span><span class="sxs-lookup"><span data-stu-id="de33c-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="de33c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de33c-111">EXAMPLES</span></span>

### <span data-ttu-id="de33c-112">---------------Beispiel 1: Abrufen des Verbindungs Monitors anhand des Namens an der angegebenen Position---------------</span><span class="sxs-lookup"><span data-stu-id="de33c-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


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

<span data-ttu-id="de33c-113">In diesem Beispiel wird der Verbindungsmonitor über den Namen an der angegebenen Position abgerufen.</span><span class="sxs-lookup"><span data-stu-id="de33c-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="de33c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="de33c-114">PARAMETERS</span></span>

### <span data-ttu-id="de33c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de33c-115">-AsJob</span></span>
<span data-ttu-id="de33c-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="de33c-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de33c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de33c-117">-DefaultProfile</span></span>
<span data-ttu-id="de33c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de33c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de33c-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="de33c-119">-Location</span></span>
<span data-ttu-id="de33c-120">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="de33c-120">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de33c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="de33c-121">-Name</span></span>
<span data-ttu-id="de33c-122">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="de33c-122">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de33c-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de33c-123">-NetworkWatcher</span></span>
<span data-ttu-id="de33c-124">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="de33c-124">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de33c-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="de33c-125">-NetworkWatcherName</span></span>
<span data-ttu-id="de33c-126">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="de33c-126">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de33c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de33c-127">-ResourceGroupName</span></span>
<span data-ttu-id="de33c-128">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="de33c-128">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de33c-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="de33c-129">-ResourceId</span></span>
<span data-ttu-id="de33c-130">Die Ressourcen-ID des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="de33c-130">Resource ID of the connection monitor.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de33c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de33c-131">CommonParameters</span></span>
<span data-ttu-id="de33c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de33c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de33c-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de33c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de33c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de33c-134">INPUTS</span></span>

### <span data-ttu-id="de33c-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de33c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="de33c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="de33c-136">System.String</span></span>


## <span data-ttu-id="de33c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de33c-137">OUTPUTS</span></span>

### <span data-ttu-id="de33c-138">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="de33c-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="de33c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="de33c-139">NOTES</span></span>
<span data-ttu-id="de33c-140">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="de33c-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="de33c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de33c-141">RELATED LINKS</span></span>
<span data-ttu-id="de33c-142">[Neu – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="de33c-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="de33c-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="de33c-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="de33c-144">[Neu – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Neu – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="de33c-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="de33c-145">[Neu – AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="de33c-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>