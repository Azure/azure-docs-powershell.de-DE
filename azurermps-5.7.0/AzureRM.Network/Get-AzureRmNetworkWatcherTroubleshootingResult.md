---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: ef730b8ee6e6c35408b9d57d9dc23b0ab51a63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479734"
---
# <span data-ttu-id="9eb93-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9eb93-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="9eb93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9eb93-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb93-103">Ruft das Ergebnis der Problembehandlung aus dem zuvor ausgeführten oder zurzeit ausgeführten Problem behandlungsvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="9eb93-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eb93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9eb93-104">SYNTAX</span></span>

### <span data-ttu-id="9eb93-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9eb93-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eb93-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9eb93-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eb93-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9eb93-107">DESCRIPTION</span></span>
<span data-ttu-id="9eb93-108">Das Get-AzureRmNetworkWatcherTroubleshootingResult-Cmdlet ruft das Ergebnis der Problembehandlung aus dem zuvor ausgeführten oder aktuell ausgeführten Start-AzureRmNetworkWatcherResourceTroubleshooting Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="9eb93-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="9eb93-109">Wenn der Problem behandlungsvorgang gerade ausgeführt wird, kann dieser Vorgang einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="9eb93-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="9eb93-110">Derzeit werden virtuelle Netzwerkgateways und-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9eb93-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="9eb93-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9eb93-111">EXAMPLES</span></span>

### <span data-ttu-id="9eb93-112">---Beispiel 1: Starten der Problembehandlung auf einem virtuellen Netzwerk Gateway und Abrufen des Ergebnis---</span><span class="sxs-lookup"><span data-stu-id="9eb93-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="9eb93-113">Im obigen Beispiel wird die Problembehandlung auf einem virtuellen Netzwerkgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="9eb93-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="9eb93-114">Es kann einige Minuten dauern, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9eb93-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="9eb93-115">Nachdem die Problembehandlung begonnen hat, wird ein Get-AzureRmNetworkWatcherTroubleshootingResult Aufruf an die Ressource durchgeführt, um das Ergebnis dieses Anrufs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9eb93-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="9eb93-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eb93-116">PARAMETERS</span></span>

### <span data-ttu-id="9eb93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb93-117">-DefaultProfile</span></span>
<span data-ttu-id="9eb93-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9eb93-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eb93-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9eb93-119">-NetworkWatcher</span></span>
<span data-ttu-id="9eb93-120">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="9eb93-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="9eb93-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9eb93-121">-NetworkWatcherName</span></span>
<span data-ttu-id="9eb93-122">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="9eb93-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="9eb93-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb93-123">-ResourceGroupName</span></span>
<span data-ttu-id="9eb93-124">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9eb93-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9eb93-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9eb93-125">-TargetResourceId</span></span>
<span data-ttu-id="9eb93-126">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9eb93-126">The target resource ID.</span></span>

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

### <span data-ttu-id="9eb93-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb93-127">CommonParameters</span></span>
<span data-ttu-id="9eb93-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eb93-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb93-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eb93-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb93-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9eb93-130">INPUTS</span></span>

### <span data-ttu-id="9eb93-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9eb93-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9eb93-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9eb93-132">System.String</span></span>

## <span data-ttu-id="9eb93-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9eb93-133">OUTPUTS</span></span>

### <span data-ttu-id="9eb93-134">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="9eb93-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="9eb93-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9eb93-135">NOTES</span></span>
<span data-ttu-id="9eb93-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Problembehandlung, VPN, Verbindung</span><span class="sxs-lookup"><span data-stu-id="9eb93-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="9eb93-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9eb93-137">RELATED LINKS</span></span>

[<span data-ttu-id="9eb93-138">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9eb93-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9eb93-139">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9eb93-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9eb93-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9eb93-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9eb93-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9eb93-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9eb93-142">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9eb93-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9eb93-143">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9eb93-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="9eb93-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9eb93-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9eb93-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9eb93-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9eb93-146">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9eb93-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9eb93-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9eb93-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="9eb93-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9eb93-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="9eb93-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9eb93-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9eb93-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9eb93-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
