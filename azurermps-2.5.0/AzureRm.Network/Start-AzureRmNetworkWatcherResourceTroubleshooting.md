---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
ms.openlocfilehash: 411b70fb6018b71b1c1c7fbf67816d0c86e6d3b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848691"
---
# <span data-ttu-id="4b4a6-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4b4a6-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="4b4a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4a6-103">Startet die Problembehandlung für eine Netzwerkressource in Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b4a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b4a6-104">SYNTAX</span></span>

### <span data-ttu-id="4b4a6-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b4a6-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b4a6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4b4a6-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b4a6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b4a6-107">DESCRIPTION</span></span>
<span data-ttu-id="4b4a6-108">Das Start-AzureRmNetworkWatcherResourceTroubleshooting-Cmdlet startet die Problembehandlung für eine Netzwerkressource in Azure und gibt Informationen zu potenziellen Problemen und Abschwächungen zurück.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="4b4a6-109">Derzeit werden virtuelle Netzwerkgateways und-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="4b4a6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b4a6-110">EXAMPLES</span></span>

### <span data-ttu-id="4b4a6-111">---Beispiel 1: Starten der Problembehandlung auf einem virtuellen Netzwerk Gateway---</span><span class="sxs-lookup"><span data-stu-id="4b4a6-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="4b4a6-112">Im obigen Beispiel wird die Problembehandlung auf einem virtuellen Netzwerkgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="4b4a6-113">Es kann einige Minuten dauern, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="4b4a6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b4a6-114">PARAMETERS</span></span>

### <span data-ttu-id="4b4a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4a6-115">-DefaultProfile</span></span>
<span data-ttu-id="4b4a6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b4a6-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b4a6-117">-NetworkWatcher</span></span>
<span data-ttu-id="4b4a6-118">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="4b4a6-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4b4a6-119">-NetworkWatcherName</span></span>
<span data-ttu-id="4b4a6-120">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="4b4a6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b4a6-121">-ResourceGroupName</span></span>
<span data-ttu-id="4b4a6-122">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4b4a6-123">-Speicher-Nr</span><span class="sxs-lookup"><span data-stu-id="4b4a6-123">-StorageId</span></span>
<span data-ttu-id="4b4a6-124">Die Speicher-ID.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-124">The storage ID.</span></span>

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

### <span data-ttu-id="4b4a6-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="4b4a6-125">-StoragePath</span></span>
<span data-ttu-id="4b4a6-126">Der Speicherpfad.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-126">The storage path.</span></span>

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

### <span data-ttu-id="4b4a6-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4b4a6-127">-TargetResourceId</span></span>
<span data-ttu-id="4b4a6-128">Gibt die Ressourcen-ID der zu behandelnden Ressource an.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="4b4a6-129">Beispielformat: "/Subscriptions/$ {Subscription-Nr}/resourceGroups/$ {resourceGroupName}/Providers/Microsoft.Network/Connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="4b4a6-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="4b4a6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4a6-130">CommonParameters</span></span>
<span data-ttu-id="4b4a6-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4a6-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b4a6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4a6-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b4a6-133">INPUTS</span></span>

### <span data-ttu-id="4b4a6-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b4a6-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4b4a6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4b4a6-135">System.String</span></span>

## <span data-ttu-id="4b4a6-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b4a6-136">OUTPUTS</span></span>

### <span data-ttu-id="4b4a6-137">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="4b4a6-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="4b4a6-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b4a6-138">NOTES</span></span>
<span data-ttu-id="4b4a6-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Problembehandlung, VPN, Verbindung</span><span class="sxs-lookup"><span data-stu-id="4b4a6-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="4b4a6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b4a6-140">RELATED LINKS</span></span>

[<span data-ttu-id="4b4a6-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4b4a6-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4b4a6-142">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b4a6-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4b4a6-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b4a6-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4b4a6-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b4a6-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4b4a6-145">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b4a6-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b4a6-146">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4b4a6-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4b4a6-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b4a6-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b4a6-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b4a6-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b4a6-149">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b4a6-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b4a6-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4b4a6-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4b4a6-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4b4a6-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4b4a6-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4b4a6-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4b4a6-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4b4a6-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
