---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: f8e51258a56051edf99aa1ec0cfa5e252e0ac0d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821524"
---
# <span data-ttu-id="4b4ab-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4b4ab-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="4b4ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b4ab-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4ab-103">Erstellt ein neues Filterobjekt für die Paketsammlung.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="4b4ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b4ab-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b4ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b4ab-105">DESCRIPTION</span></span>
<span data-ttu-id="4b4ab-106">Das New-AzPacketCaptureFilterConfig-Cmdlet erstellt ein neues Filterobjekt für die Paketsammlung.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="4b4ab-107">Dieses Objekt wird verwendet, um den Typ der Pakete zu beschränken, die während einer Paket Aufnahmesitzung mithilfe der angegebenen Kriterien erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="4b4ab-108">Das New-AzNetworkWatcherPacketCapture-Cmdlet kann mehrere Filterobjekte akzeptieren, um kompostierbare Aufnahmesitzungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="4b4ab-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b4ab-109">EXAMPLES</span></span>

### <span data-ttu-id="4b4ab-110">Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern</span><span class="sxs-lookup"><span data-stu-id="4b4ab-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="4b4ab-111">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="4b4ab-112">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="4b4ab-113">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="4b4ab-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b4ab-114">PARAMETERS</span></span>

### <span data-ttu-id="4b4ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4ab-115">-DefaultProfile</span></span>
<span data-ttu-id="4b4ab-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b4ab-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="4b4ab-117">-LocalIPAddress</span></span>
<span data-ttu-id="4b4ab-118">Gibt die lokale IP-Adresse an, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="4b4ab-119">Beispieleingaben: "127.0.0.1" für einen einzelnen Adresseintrag.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="4b4ab-120">"127.0.0.1-127.0.0.255" für Range.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="4b4ab-121">"127.0.0.1; 127.0.0.5;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ab-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="4b4ab-122">-LocalPort</span></span>
<span data-ttu-id="4b4ab-123">Gibt die lokale IP-Adresse an, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="4b4ab-124">Beispieleingaben: "127.0.0.1" für einen einzelnen Adresseintrag.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="4b4ab-125">"127.0.0.1-127.0.0.255" für Range.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="4b4ab-126">"127.0.0.1; 127.0.0.5;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ab-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4b4ab-127">-Protocol</span></span>
<span data-ttu-id="4b4ab-128">Gibt das Protokoll an, nach dem gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="4b4ab-129">Zulässige Werte "TCP"; "UDP"; "Any"</span><span class="sxs-lookup"><span data-stu-id="4b4ab-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ab-130">-Remote</span><span class="sxs-lookup"><span data-stu-id="4b4ab-130">-RemoteIPAddress</span></span>
<span data-ttu-id="4b4ab-131">Gibt die Remote-IP-Adresse an, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="4b4ab-132">Beispieleingaben: "127.0.0.1" für einen einzelnen Adresseintrag.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="4b4ab-133">"127.0.0.1-127.0.0.255" für Range.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="4b4ab-134">"127.0.0.1; 127.0.0.5;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ab-135">-Remoteport</span><span class="sxs-lookup"><span data-stu-id="4b4ab-135">-RemotePort</span></span>
<span data-ttu-id="4b4ab-136">Gibt den Remote Anschluss an, nach dem gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="4b4ab-137">Beispiel Eingänge für Remote-Port: "80" für den Single Port-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="4b4ab-138">"80-85" für Range.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-138">"80-85" for range.</span></span>
<span data-ttu-id="4b4ab-139">"80; 443;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-139">"80;443;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4ab-140">CommonParameters</span></span>
<span data-ttu-id="4b4ab-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4ab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4ab-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b4ab-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4ab-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b4ab-143">INPUTS</span></span>

### <span data-ttu-id="4b4ab-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4b4ab-144">System.String</span></span>

## <span data-ttu-id="4b4ab-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b4ab-145">OUTPUTS</span></span>

### <span data-ttu-id="4b4ab-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="4b4ab-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="4b4ab-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b4ab-147">NOTES</span></span>
<span data-ttu-id="4b4ab-148">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Watcher, Paket, Capture, Traffic, Filter</span><span class="sxs-lookup"><span data-stu-id="4b4ab-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="4b4ab-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b4ab-149">RELATED LINKS</span></span>

[<span data-ttu-id="4b4ab-150">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b4ab-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4b4ab-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b4ab-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4b4ab-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b4ab-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4b4ab-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4b4ab-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4b4ab-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4b4ab-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4b4ab-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4b4ab-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4b4ab-156">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4b4ab-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4b4ab-157">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b4ab-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b4ab-158">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4b4ab-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4b4ab-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b4ab-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b4ab-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b4ab-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b4ab-161">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b4ab-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b4ab-162">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b4ab-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4b4ab-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4b4ab-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4b4ab-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4b4ab-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4b4ab-165">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b4ab-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b4ab-166">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b4ab-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b4ab-167">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b4ab-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b4ab-168">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4b4ab-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4b4ab-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b4ab-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b4ab-170">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b4ab-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b4ab-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4b4ab-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4b4ab-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4b4ab-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4b4ab-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4b4ab-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4b4ab-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4b4ab-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4b4ab-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4b4ab-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4b4ab-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b4ab-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)