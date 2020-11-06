---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: ad6d2baaccdc17ec6ca414ae4b0cee84db20c94b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481878"
---
# <span data-ttu-id="cc3c4-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cc3c4-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="cc3c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc3c4-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3c4-103">Erstellt ein neues Filterobjekt für die Paketsammlung.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc3c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc3c4-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc3c4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc3c4-105">DESCRIPTION</span></span>
<span data-ttu-id="cc3c4-106">Das New-AzureRmPacketCaptureFilterConfig-Cmdlet erstellt ein neues Filterobjekt für die Paketsammlung.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="cc3c4-107">Dieses Objekt wird verwendet, um den Typ der Pakete zu beschränken, die während einer Paket Aufnahmesitzung mithilfe der angegebenen Kriterien erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="cc3c4-108">Das New-AzureRmNetworkWatcherPacketCapture-Cmdlet kann mehrere Filterobjekte akzeptieren, um kompostierbare Aufnahmesitzungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="cc3c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc3c4-109">EXAMPLES</span></span>

### <span data-ttu-id="cc3c4-110">---Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern---</span><span class="sxs-lookup"><span data-stu-id="cc3c4-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="cc3c4-111">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="cc3c4-112">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="cc3c4-113">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="cc3c4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc3c4-114">PARAMETERS</span></span>

### <span data-ttu-id="cc3c4-115">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="cc3c4-115">-LocalIPAddress</span></span>
<span data-ttu-id="cc3c4-116">Gibt die lokale IP-Adresse an, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-116">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="cc3c4-117">Beispieleingaben: "127.0.0.1" für einen einzelnen Adresseintrag.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-117">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="cc3c4-118">"127.0.0.1-127.0.0.255" für Range.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-118">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="cc3c4-119">"127.0.0.1; 127.0.0.5;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-119">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="cc3c4-120">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="cc3c4-120">-LocalPort</span></span>
<span data-ttu-id="cc3c4-121">Gibt die lokale IP-Adresse an, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-121">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="cc3c4-122">Beispieleingaben: "127.0.0.1" für einen einzelnen Adresseintrag.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-122">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="cc3c4-123">"127.0.0.1-127.0.0.255" für Range.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-123">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="cc3c4-124">"127.0.0.1; 127.0.0.5;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-124">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="cc3c4-125">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="cc3c4-125">-Protocol</span></span>
<span data-ttu-id="cc3c4-126">Gibt den zu filternden Procotol an.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-126">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="cc3c4-127">Zulässige Werte "TCP"; "UDP"; "Any"</span><span class="sxs-lookup"><span data-stu-id="cc3c4-127">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="cc3c4-128">-Remote</span><span class="sxs-lookup"><span data-stu-id="cc3c4-128">-RemoteIPAddress</span></span>
<span data-ttu-id="cc3c4-129">Gibt die Remote-IP-Adresse an, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-129">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="cc3c4-130">Beispieleingaben: "127.0.0.1" für einen einzelnen Adresseintrag.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-130">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="cc3c4-131">"127.0.0.1-127.0.0.255" für Range.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-131">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="cc3c4-132">"127.0.0.1; 127.0.0.5;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-132">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="cc3c4-133">-Remoteport</span><span class="sxs-lookup"><span data-stu-id="cc3c4-133">-RemotePort</span></span>
<span data-ttu-id="cc3c4-134">Gibt den Remote Anschluss an, nach dem gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-134">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="cc3c4-135">Beispiel Eingänge für Remote-Port: "80" für den Single Port-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-135">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="cc3c4-136">"80-85" für Range.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-136">"80-85" for range.</span></span>
<span data-ttu-id="cc3c4-137">"80; 443;" für mehrere Einträge.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-137">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="cc3c4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc3c4-138">-DefaultProfile</span></span>
<span data-ttu-id="cc3c4-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc3c4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3c4-140">CommonParameters</span></span>
<span data-ttu-id="cc3c4-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc3c4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3c4-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc3c4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3c4-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc3c4-143">INPUTS</span></span>

### <span data-ttu-id="cc3c4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cc3c4-144">System.String</span></span>

## <span data-ttu-id="cc3c4-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc3c4-145">OUTPUTS</span></span>

### <span data-ttu-id="cc3c4-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="cc3c4-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="cc3c4-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc3c4-147">NOTES</span></span>
<span data-ttu-id="cc3c4-148">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Watcher, Paket, Capture, Traffic, Filter</span><span class="sxs-lookup"><span data-stu-id="cc3c4-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="cc3c4-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc3c4-149">RELATED LINKS</span></span>

[<span data-ttu-id="cc3c4-150">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc3c4-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cc3c4-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc3c4-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cc3c4-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc3c4-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cc3c4-153">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc3c4-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cc3c4-154">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cc3c4-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cc3c4-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cc3c4-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cc3c4-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cc3c4-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cc3c4-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cc3c4-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="cc3c4-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cc3c4-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="cc3c4-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cc3c4-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cc3c4-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cc3c4-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="cc3c4-161">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cc3c4-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
