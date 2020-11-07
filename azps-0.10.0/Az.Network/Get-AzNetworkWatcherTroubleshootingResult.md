---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841555"
---
# <span data-ttu-id="5ee6d-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5ee6d-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="5ee6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ee6d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee6d-103">Ruft das Ergebnis der Problembehandlung aus dem zuvor ausgeführten oder zurzeit ausgeführten Problem behandlungsvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="5ee6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ee6d-104">SYNTAX</span></span>

### <span data-ttu-id="5ee6d-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ee6d-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ee6d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5ee6d-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ee6d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ee6d-107">DESCRIPTION</span></span>
<span data-ttu-id="5ee6d-108">Das Get-AzNetworkWatcherTroubleshootingResult-Cmdlet ruft das Ergebnis der Problembehandlung aus dem zuvor ausgeführten oder aktuell ausgeführten Start-AzNetworkWatcherResourceTroubleshooting Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="5ee6d-109">Wenn der Problem behandlungsvorgang gerade ausgeführt wird, kann dieser Vorgang einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="5ee6d-110">Derzeit werden virtuelle Netzwerkgateways und-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="5ee6d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ee6d-111">EXAMPLES</span></span>

### <span data-ttu-id="5ee6d-112">---Beispiel 1: Starten der Problembehandlung auf einem virtuellen Netzwerk Gateway und Abrufen des Ergebnis---</span><span class="sxs-lookup"><span data-stu-id="5ee6d-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="5ee6d-113">Im obigen Beispiel wird die Problembehandlung auf einem virtuellen Netzwerkgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="5ee6d-114">Es kann einige Minuten dauern, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="5ee6d-115">Nachdem die Problembehandlung begonnen hat, wird ein Get-AzNetworkWatcherTroubleshootingResult Aufruf an die Ressource durchgeführt, um das Ergebnis dieses Anrufs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="5ee6d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ee6d-116">PARAMETERS</span></span>

### <span data-ttu-id="5ee6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee6d-117">-DefaultProfile</span></span>
<span data-ttu-id="5ee6d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ee6d-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ee6d-119">-NetworkWatcher</span></span>
<span data-ttu-id="5ee6d-120">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="5ee6d-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5ee6d-121">-NetworkWatcherName</span></span>
<span data-ttu-id="5ee6d-122">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="5ee6d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee6d-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ee6d-124">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5ee6d-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5ee6d-125">-TargetResourceId</span></span>
<span data-ttu-id="5ee6d-126">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-126">The target resource ID.</span></span>

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

### <span data-ttu-id="5ee6d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee6d-127">CommonParameters</span></span>
<span data-ttu-id="5ee6d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee6d-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee6d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee6d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ee6d-130">INPUTS</span></span>

### <span data-ttu-id="5ee6d-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ee6d-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5ee6d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5ee6d-132">System.String</span></span>

## <span data-ttu-id="5ee6d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ee6d-133">OUTPUTS</span></span>

### <span data-ttu-id="5ee6d-134">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="5ee6d-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="5ee6d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ee6d-135">NOTES</span></span>
<span data-ttu-id="5ee6d-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Problembehandlung, VPN, Verbindung</span><span class="sxs-lookup"><span data-stu-id="5ee6d-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="5ee6d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ee6d-137">RELATED LINKS</span></span>

[<span data-ttu-id="5ee6d-138">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5ee6d-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5ee6d-139">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ee6d-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5ee6d-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ee6d-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5ee6d-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ee6d-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5ee6d-142">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ee6d-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5ee6d-143">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5ee6d-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5ee6d-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ee6d-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5ee6d-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ee6d-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5ee6d-146">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ee6d-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5ee6d-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5ee6d-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5ee6d-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5ee6d-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5ee6d-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5ee6d-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5ee6d-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5ee6d-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
