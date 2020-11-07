---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitorReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitorReport.md
ms.openlocfilehash: a1bdb9a1e77793622d0c23793701b9d3119b4f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662464"
---
# <span data-ttu-id="4fd5d-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4fd5d-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>

## <span data-ttu-id="4fd5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4fd5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd5d-103">Abfragen einer Momentaufnahme des letzten Verbindungsstatus</span><span class="sxs-lookup"><span data-stu-id="4fd5d-103">Query a snapshot of the most recent connection states.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fd5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fd5d-104">SYNTAX</span></span>

### <span data-ttu-id="4fd5d-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4fd5d-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fd5d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4fd5d-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcher <PSNetworkWatcher> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fd5d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4fd5d-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -Location <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fd5d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd5d-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fd5d-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4fd5d-109">SetByInputObject</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -InputObject <PSConnectionMonitorResult> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fd5d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fd5d-110">DESCRIPTION</span></span>
<span data-ttu-id="4fd5d-111">Das Get-AzureRmNetworkWatcherConnectionMonitorReport-Cmdlet gibt den Bericht in den letzten Verbindungsstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-111">The Get-AzureRmNetworkWatcherConnectionMonitorReport cmdlet returns the report on the most recent connection states.</span></span>

## <span data-ttu-id="4fd5d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fd5d-112">EXAMPLES</span></span>

### <span data-ttu-id="4fd5d-113">Beispiel 1: Abrufen des neuesten Verbindungs-Snapshots des Verbindungs Monitors anhand des Namens an der angegebenen Position</span><span class="sxs-lookup"><span data-stu-id="4fd5d-113">Example 1: Get the most recent connection snapshot of the connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitorReport -Location centraluseuap -Name cm


States : [
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-12T01:18:20Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "1530e0f2-c9b7-4bc0-a205-cf7332cd8983",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "80e46c56-2cf9-4106-8602-608a74832d41"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "80e46c56-2cf9-4106-8602-608a74832d41",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "e17cf884-69db-43b8-9cd5-f920770a0dbe"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "e17cf884-69db-43b8-9cd5-f920770a0dbe",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Unreachable",
             "StartTime": "2018-01-12T01:14:11Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "b6251ff8-3d07-4fdf-98f8-04b168e1cf90",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "de6d463b-47fb-4beb-afc4-d77782755313"
                 ],
                 "Issues": [
                   {
                     "Origin": "Local",
                     "Severity": "Error",
                     "Type": "NetworkError",
                     "Context": []
                   }
                 ]
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "de6d463b-47fb-4beb-afc4-d77782755313",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "0cbadb7e-cd99-4fa9-a832-eb4e0d112293"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "0cbadb7e-cd99-4fa9-a832-eb4e0d112293",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "538005d1-994a-4350-9866-6985385beecf"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "538005d1-994a-4350-9866-6985385beecf",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-11T23:54:05Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "3dbec7e8-a37f-4acd-bc5f-86918fffba0e",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "1a87cf61-1be6-4add-bba7-f84afbcf3726"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "1a87cf61-1be6-4add-bba7-f84afbcf3726",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "070c0740-308e-43ba-b72f-5d8d5a6537ec"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "070c0740-308e-43ba-b72f-5d8d5a6537ec",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "760182e1-c88d-4cfc-a711-65e7e622a67a"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "760182e1-c88d-4cfc-a711-65e7e622a67a",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           }
         ]
```

<span data-ttu-id="4fd5d-114">In diesem Beispiel wird der letzte Verbindungsstatus des angegebenen Verbindungs Monitors abgefragt.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-114">In this example we query the most recent connection states of the specified connection monitor.</span></span>

## <span data-ttu-id="4fd5d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fd5d-115">PARAMETERS</span></span>

### <span data-ttu-id="4fd5d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fd5d-116">-AsJob</span></span>
<span data-ttu-id="4fd5d-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4fd5d-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd5d-118">-DefaultProfile</span></span>
<span data-ttu-id="4fd5d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd5d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4fd5d-120">-InputObject</span></span>
<span data-ttu-id="4fd5d-121">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-121">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5d-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="4fd5d-122">-Location</span></span>
<span data-ttu-id="4fd5d-123">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-123">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4fd5d-124">-Name</span></span>
<span data-ttu-id="4fd5d-125">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="4fd5d-125">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5d-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4fd5d-126">-NetworkWatcher</span></span>
<span data-ttu-id="4fd5d-127">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="4fd5d-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4fd5d-128">-NetworkWatcherName</span></span>
<span data-ttu-id="4fd5d-129">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd5d-130">-ResourceGroupName</span></span>
<span data-ttu-id="4fd5d-131">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-131">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5d-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4fd5d-132">-ResourceId</span></span>
<span data-ttu-id="4fd5d-133">Die Ressourcen-ID des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-133">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="4fd5d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd5d-134">CommonParameters</span></span>
<span data-ttu-id="4fd5d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd5d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4fd5d-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd5d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd5d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4fd5d-137">INPUTS</span></span>

### <span data-ttu-id="4fd5d-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4fd5d-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4fd5d-139">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="4fd5d-139">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="4fd5d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4fd5d-140">OUTPUTS</span></span>

### <span data-ttu-id="4fd5d-141">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorQueryResult</span><span class="sxs-lookup"><span data-stu-id="4fd5d-141">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorQueryResult</span></span>

## <span data-ttu-id="4fd5d-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4fd5d-142">NOTES</span></span>
<span data-ttu-id="4fd5d-143">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="4fd5d-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="4fd5d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4fd5d-144">RELATED LINKS</span></span>

[<span data-ttu-id="4fd5d-145">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4fd5d-145">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="4fd5d-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4fd5d-146">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="4fd5d-147">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4fd5d-147">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="4fd5d-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4fd5d-148">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="4fd5d-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4fd5d-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="4fd5d-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4fd5d-150">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="4fd5d-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4fd5d-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="4fd5d-152">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4fd5d-152">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="4fd5d-153">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4fd5d-153">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="4fd5d-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4fd5d-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="4fd5d-155">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4fd5d-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="4fd5d-156">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4fd5d-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="4fd5d-157">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4fd5d-157">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="4fd5d-158">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4fd5d-158">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="4fd5d-159">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4fd5d-159">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="4fd5d-160">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4fd5d-160">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="4fd5d-161">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4fd5d-161">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="4fd5d-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4fd5d-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
