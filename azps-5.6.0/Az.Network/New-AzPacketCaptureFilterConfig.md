---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: b3732167d26f35b0e3e8ac6c29f187138cde0b18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919571"
---
# <span data-ttu-id="a0ec0-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a0ec0-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="a0ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ec0-103">Erstellt ein neues Paketaufnahmefilterobjekt.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="a0ec0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0ec0-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0ec0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ec0-105">DESCRIPTION</span></span>
<span data-ttu-id="a0ec0-106">Das New-AzPacketCaptureFilterConfig-Cmdlet erstellt ein neues Paketaufnahmefilterobjekt.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="a0ec0-107">Dieses Objekt wird verwendet, um den Typ von Paketen einzuschränken, die während einer Paketaufnahmesitzung mithilfe der angegebenen Kriterien erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="a0ec0-108">Das New-AzNetworkWatcherPacketCapture-Cmdlet kann mehrere Filterobjekte akzeptieren, um komposierbare Aufnahmesitzungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="a0ec0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0ec0-109">EXAMPLES</span></span>

### <span data-ttu-id="a0ec0-110">Beispiel 1: Erstellen einer Paketaufnahme mit mehreren Filtern</span><span class="sxs-lookup"><span data-stu-id="a0ec0-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="a0ec0-111">In diesem Beispiel erstellen wir eine Paketaufnahme mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="a0ec0-112">Sobald die Sitzung abgeschlossen ist, wird sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="a0ec0-113">Hinweis: Die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketaufzeichnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="a0ec0-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a0ec0-114">PARAMETERS</span></span>

### <span data-ttu-id="a0ec0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ec0-115">-DefaultProfile</span></span>
<span data-ttu-id="a0ec0-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0ec0-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="a0ec0-117">-LocalIPAddress</span></span>
<span data-ttu-id="a0ec0-118">Gibt die lokale IP-Adresse an, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="a0ec0-119">Beispieleingaben: "127.0.0.1" für einen einzelnen Adresseintrag.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="a0ec0-120">"127.0.0.1-127.0.0.255" für Bereich.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="a0ec0-121">"127.0.0.1;127.0.0.5;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="a0ec0-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="a0ec0-122">-LocalPort</span></span>
<span data-ttu-id="a0ec0-123">Gibt die lokale IP-Adresse an, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="a0ec0-124">Beispieleingaben: "127.0.0.1" für einen einzelnen Adresseintrag.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="a0ec0-125">"127.0.0.1-127.0.0.255" für Bereich.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="a0ec0-126">"127.0.0.1;127.0.0.5;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="a0ec0-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a0ec0-127">-Protocol</span></span>
<span data-ttu-id="a0ec0-128">Gibt das Protokoll an, nach dem gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="a0ec0-129">Zulässige Werte "TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="a0ec0-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="a0ec0-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="a0ec0-130">-RemoteIPAddress</span></span>
<span data-ttu-id="a0ec0-131">Gibt die Remote-IP-Adresse an, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="a0ec0-132">Beispieleingaben: "127.0.0.1" für einen einzelnen Adresseintrag.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="a0ec0-133">"127.0.0.1-127.0.0.255" für Bereich.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="a0ec0-134">"127.0.0.1;127.0.0.5;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="a0ec0-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="a0ec0-135">-RemotePort</span></span>
<span data-ttu-id="a0ec0-136">Gibt den Remoteport an, nach dem gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="a0ec0-137">Remoteport Beispieleingaben: "80" für die Einzelporteingabe.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="a0ec0-138">"80-85" für Bereich.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-138">"80-85" for range.</span></span>
<span data-ttu-id="a0ec0-139">"80;443;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="a0ec0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ec0-140">CommonParameters</span></span>
<span data-ttu-id="a0ec0-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ec0-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0ec0-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ec0-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0ec0-143">INPUTS</span></span>

### <span data-ttu-id="a0ec0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a0ec0-144">System.String</span></span>

## <span data-ttu-id="a0ec0-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0ec0-145">OUTPUTS</span></span>

### <span data-ttu-id="a0ec0-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="a0ec0-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="a0ec0-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a0ec0-147">NOTES</span></span>
<span data-ttu-id="a0ec0-148">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span><span class="sxs-lookup"><span data-stu-id="a0ec0-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="a0ec0-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a0ec0-149">RELATED LINKS</span></span>

[<span data-ttu-id="a0ec0-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0ec0-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a0ec0-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0ec0-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a0ec0-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0ec0-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a0ec0-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a0ec0-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a0ec0-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a0ec0-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a0ec0-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a0ec0-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a0ec0-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a0ec0-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a0ec0-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0ec0-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0ec0-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a0ec0-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a0ec0-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0ec0-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0ec0-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0ec0-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0ec0-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0ec0-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0ec0-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ec0-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a0ec0-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a0ec0-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a0ec0-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a0ec0-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a0ec0-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0ec0-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0ec0-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0ec0-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0ec0-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0ec0-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0ec0-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a0ec0-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a0ec0-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0ec0-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0ec0-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0ec0-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0ec0-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a0ec0-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a0ec0-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a0ec0-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a0ec0-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a0ec0-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a0ec0-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a0ec0-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a0ec0-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a0ec0-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a0ec0-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0ec0-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
