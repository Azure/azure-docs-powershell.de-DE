---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841563"
---
# <span data-ttu-id="a7f4f-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7f4f-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a7f4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f4f-103">Ruft Informationen und Eigenschaften sowie den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a7f4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7f4f-104">SYNTAX</span></span>

### <span data-ttu-id="a7f4f-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7f4f-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7f4f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a7f4f-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7f4f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7f4f-107">DESCRIPTION</span></span>
<span data-ttu-id="a7f4f-108">Die Get-AzNetworkWatcherPacketCapture ruft die Eigenschaften und den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a7f4f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7f4f-109">EXAMPLES</span></span>

### <span data-ttu-id="a7f4f-110">---Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern und Abrufen des Status---</span><span class="sxs-lookup"><span data-stu-id="a7f4f-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a7f4f-111">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="a7f4f-112">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="a7f4f-113">Anschließend rufen wir Get-AzNetworkWatcherPacketCapture auf, um den Status der Aufnahmesitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="a7f4f-114">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="a7f4f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7f4f-115">PARAMETERS</span></span>

### <span data-ttu-id="a7f4f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7f4f-116">-AsJob</span></span>
<span data-ttu-id="a7f4f-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a7f4f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7f4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4f-118">-DefaultProfile</span></span>
<span data-ttu-id="a7f4f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f4f-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7f4f-120">-NetworkWatcher</span></span>
<span data-ttu-id="a7f4f-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="a7f4f-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a7f4f-122">-NetworkWatcherName</span></span>
<span data-ttu-id="a7f4f-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-123">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f4f-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a7f4f-124">-PacketCaptureName</span></span>
<span data-ttu-id="a7f4f-125">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-125">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f4f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f4f-126">-ResourceGroupName</span></span>
<span data-ttu-id="a7f4f-127">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a7f4f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f4f-128">CommonParameters</span></span>
<span data-ttu-id="a7f4f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f4f-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f4f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f4f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7f4f-131">INPUTS</span></span>

### <span data-ttu-id="a7f4f-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7f4f-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a7f4f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a7f4f-133">System.String</span></span>

## <span data-ttu-id="a7f4f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7f4f-134">OUTPUTS</span></span>

### <span data-ttu-id="a7f4f-135">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a7f4f-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="a7f4f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7f4f-136">NOTES</span></span>
<span data-ttu-id="a7f4f-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="a7f4f-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="a7f4f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7f4f-138">RELATED LINKS</span></span>

[<span data-ttu-id="a7f4f-139">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7f4f-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7f4f-140">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a7f4f-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a7f4f-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7f4f-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7f4f-142">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7f4f-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7f4f-143">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7f4f-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a7f4f-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7f4f-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a7f4f-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7f4f-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a7f4f-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a7f4f-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a7f4f-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a7f4f-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a7f4f-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a7f4f-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a7f4f-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a7f4f-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a7f4f-150">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a7f4f-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

