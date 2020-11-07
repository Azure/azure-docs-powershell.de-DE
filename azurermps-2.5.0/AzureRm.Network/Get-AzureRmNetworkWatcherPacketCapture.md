---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: aeadada7c6e2e2d7cb94a484e7ca3223e03b4426
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848459"
---
# <span data-ttu-id="53dd4-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="53dd4-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="53dd4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="53dd4-103">Ruft Informationen und Eigenschaften sowie den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="53dd4-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53dd4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53dd4-104">SYNTAX</span></span>

### <span data-ttu-id="53dd4-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="53dd4-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53dd4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="53dd4-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53dd4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53dd4-107">DESCRIPTION</span></span>
<span data-ttu-id="53dd4-108">Die Get-AzureRmNetworkWatcherPacketCapture ruft die Eigenschaften und den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="53dd4-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="53dd4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53dd4-109">EXAMPLES</span></span>

### <span data-ttu-id="53dd4-110">---Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern und Abrufen des Status---</span><span class="sxs-lookup"><span data-stu-id="53dd4-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="53dd4-111">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="53dd4-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="53dd4-112">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="53dd4-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="53dd4-113">Anschließend rufen wir Get-AzureRmNetworkWatcherPacketCapture auf, um den Status der Aufnahmesitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="53dd4-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="53dd4-114">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="53dd4-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="53dd4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="53dd4-115">PARAMETERS</span></span>

### <span data-ttu-id="53dd4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53dd4-116">-AsJob</span></span>
<span data-ttu-id="53dd4-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="53dd4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53dd4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53dd4-118">-DefaultProfile</span></span>
<span data-ttu-id="53dd4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53dd4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53dd4-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53dd4-120">-NetworkWatcher</span></span>
<span data-ttu-id="53dd4-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="53dd4-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="53dd4-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="53dd4-122">-NetworkWatcherName</span></span>
<span data-ttu-id="53dd4-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="53dd4-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="53dd4-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="53dd4-124">-PacketCaptureName</span></span>
<span data-ttu-id="53dd4-125">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="53dd4-125">The packet capture name.</span></span>

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

### <span data-ttu-id="53dd4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53dd4-126">-ResourceGroupName</span></span>
<span data-ttu-id="53dd4-127">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="53dd4-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="53dd4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53dd4-128">CommonParameters</span></span>
<span data-ttu-id="53dd4-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53dd4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53dd4-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53dd4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53dd4-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53dd4-131">INPUTS</span></span>

### <span data-ttu-id="53dd4-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53dd4-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="53dd4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="53dd4-133">System.String</span></span>

## <span data-ttu-id="53dd4-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53dd4-134">OUTPUTS</span></span>

### <span data-ttu-id="53dd4-135">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="53dd4-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="53dd4-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="53dd4-136">NOTES</span></span>
<span data-ttu-id="53dd4-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="53dd4-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="53dd4-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53dd4-138">RELATED LINKS</span></span>

[<span data-ttu-id="53dd4-139">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="53dd4-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="53dd4-140">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="53dd4-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="53dd4-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="53dd4-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="53dd4-142">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="53dd4-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="53dd4-143">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53dd4-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="53dd4-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53dd4-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="53dd4-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53dd4-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="53dd4-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="53dd4-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="53dd4-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="53dd4-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="53dd4-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="53dd4-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="53dd4-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="53dd4-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="53dd4-150">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="53dd4-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

