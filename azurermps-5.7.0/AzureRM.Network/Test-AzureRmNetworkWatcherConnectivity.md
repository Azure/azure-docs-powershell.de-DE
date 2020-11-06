---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
ms.openlocfilehash: 36a584be829cd3d85d900c1e0b251dc7d49e95e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496381"
---
# <span data-ttu-id="d80e0-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d80e0-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="d80e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d80e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d80e0-103">Gibt Verbindungsinformationen für eine angegebene Quell-VM und ein Ziel zurück.</span><span class="sxs-lookup"><span data-stu-id="d80e0-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d80e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d80e0-104">SYNTAX</span></span>

### <span data-ttu-id="d80e0-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d80e0-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d80e0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d80e0-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d80e0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d80e0-107">DESCRIPTION</span></span>
<span data-ttu-id="d80e0-108">Das Test-AzureRmNetworkWatcherConnectivity-Cmdlet gibt Verbindungsinformationen für eine angegebene Quell-VM und ein Ziel zurück.</span><span class="sxs-lookup"><span data-stu-id="d80e0-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="d80e0-109">Wenn die Verbindung zwischen Quelle und Ziel nicht hergestellt werden kann, gibt das Cmdlet Details zu dem Problem zurück.</span><span class="sxs-lookup"><span data-stu-id="d80e0-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="d80e0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d80e0-110">EXAMPLES</span></span>

### <span data-ttu-id="d80e0-111">---------------Beispiel 1: Testen der Netzwerk Überwachungs Konnektivität von einem virtuellen Computer zu einer Website---------------</span><span class="sxs-lookup"><span data-stu-id="d80e0-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="d80e0-112">In diesem Beispiel wird die Konnektivität von einem virtuellen Computer in Azure zu www.Bing.com getestet.</span><span class="sxs-lookup"><span data-stu-id="d80e0-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="d80e0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d80e0-113">PARAMETERS</span></span>

### <span data-ttu-id="d80e0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d80e0-114">-AsJob</span></span>
<span data-ttu-id="d80e0-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d80e0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d80e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80e0-116">-DefaultProfile</span></span>
<span data-ttu-id="d80e0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d80e0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d80e0-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d80e0-118">-DestinationAddress</span></span>
<span data-ttu-id="d80e0-119">Die IP-Adresse oder der URI, in dem die Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d80e0-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="d80e0-120">-Ziel-Nr</span><span class="sxs-lookup"><span data-stu-id="d80e0-120">-DestinationId</span></span>
<span data-ttu-id="d80e0-121">Die ID der Ressource, in der ein Verbindungsversuch erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="d80e0-121">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="d80e0-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d80e0-122">-DestinationPort</span></span>
<span data-ttu-id="d80e0-123">Port, auf dem die Verbindungsprüfung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d80e0-123">Port on which check connectivity will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80e0-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d80e0-124">-NetworkWatcher</span></span>
<span data-ttu-id="d80e0-125">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="d80e0-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="d80e0-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d80e0-126">-NetworkWatcherName</span></span>
<span data-ttu-id="d80e0-127">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d80e0-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d80e0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d80e0-128">-ResourceGroupName</span></span>
<span data-ttu-id="d80e0-129">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d80e0-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d80e0-130">-Quellpfad</span><span class="sxs-lookup"><span data-stu-id="d80e0-130">-SourceId</span></span>
<span data-ttu-id="d80e0-131">Die ID der Ressource, aus der eine Verbindungsüberprüfung initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="d80e0-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d80e0-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="d80e0-132">-SourcePort</span></span>
<span data-ttu-id="d80e0-133">Der Quell-Port, von dem eine Verbindungsüberprüfung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d80e0-133">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d80e0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80e0-134">CommonParameters</span></span>
<span data-ttu-id="d80e0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d80e0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80e0-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d80e0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80e0-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d80e0-137">INPUTS</span></span>

### <span data-ttu-id="d80e0-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d80e0-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d80e0-139">System. String System. Int32</span><span class="sxs-lookup"><span data-stu-id="d80e0-139">System.String System.Int32</span></span>

## <span data-ttu-id="d80e0-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d80e0-140">OUTPUTS</span></span>

### <span data-ttu-id="d80e0-141">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="d80e0-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="d80e0-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d80e0-142">NOTES</span></span>
<span data-ttu-id="d80e0-143">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="d80e0-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="d80e0-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d80e0-144">RELATED LINKS</span></span>

<span data-ttu-id="d80e0-145">[Neu – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="d80e0-145">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="d80e0-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="d80e0-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="d80e0-147">[Neu – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Neu – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="d80e0-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
