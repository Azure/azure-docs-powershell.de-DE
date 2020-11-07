---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843527"
---
# <span data-ttu-id="cdab6-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cdab6-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="cdab6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdab6-102">SYNOPSIS</span></span>
<span data-ttu-id="cdab6-103">Startet die Problembehandlung für eine Netzwerkressource in Azure.</span><span class="sxs-lookup"><span data-stu-id="cdab6-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="cdab6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdab6-104">SYNTAX</span></span>

### <span data-ttu-id="cdab6-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="cdab6-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdab6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cdab6-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdab6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdab6-107">DESCRIPTION</span></span>
<span data-ttu-id="cdab6-108">Das Start-AzNetworkWatcherResourceTroubleshooting-Cmdlet startet die Problembehandlung für eine Netzwerkressource in Azure und gibt Informationen zu potenziellen Problemen und Abschwächungen zurück.</span><span class="sxs-lookup"><span data-stu-id="cdab6-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="cdab6-109">Derzeit werden virtuelle Netzwerkgateways und-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdab6-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="cdab6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdab6-110">EXAMPLES</span></span>

### <span data-ttu-id="cdab6-111">---Beispiel 1: Starten der Problembehandlung auf einem virtuellen Netzwerk Gateway---</span><span class="sxs-lookup"><span data-stu-id="cdab6-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="cdab6-112">Im obigen Beispiel wird die Problembehandlung auf einem virtuellen Netzwerkgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="cdab6-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="cdab6-113">Es kann einige Minuten dauern, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cdab6-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="cdab6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdab6-114">PARAMETERS</span></span>

### <span data-ttu-id="cdab6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdab6-115">-DefaultProfile</span></span>
<span data-ttu-id="cdab6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdab6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdab6-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdab6-117">-NetworkWatcher</span></span>
<span data-ttu-id="cdab6-118">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="cdab6-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="cdab6-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cdab6-119">-NetworkWatcherName</span></span>
<span data-ttu-id="cdab6-120">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="cdab6-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="cdab6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdab6-121">-ResourceGroupName</span></span>
<span data-ttu-id="cdab6-122">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="cdab6-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cdab6-123">-Speicher-Nr</span><span class="sxs-lookup"><span data-stu-id="cdab6-123">-StorageId</span></span>
<span data-ttu-id="cdab6-124">Die Speicher-ID.</span><span class="sxs-lookup"><span data-stu-id="cdab6-124">The storage ID.</span></span>

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

### <span data-ttu-id="cdab6-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="cdab6-125">-StoragePath</span></span>
<span data-ttu-id="cdab6-126">Der Speicherpfad.</span><span class="sxs-lookup"><span data-stu-id="cdab6-126">The storage path.</span></span>

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

### <span data-ttu-id="cdab6-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="cdab6-127">-TargetResourceId</span></span>
<span data-ttu-id="cdab6-128">Gibt die Ressourcen-ID der zu behandelnden Ressource an.</span><span class="sxs-lookup"><span data-stu-id="cdab6-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="cdab6-129">Beispielformat: "/Subscriptions/$ {Subscription-Nr}/resourceGroups/$ {resourceGroupName}/Providers/Microsoft.Network/Connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="cdab6-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="cdab6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdab6-130">CommonParameters</span></span>
<span data-ttu-id="cdab6-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdab6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdab6-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdab6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdab6-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdab6-133">INPUTS</span></span>

### <span data-ttu-id="cdab6-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdab6-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="cdab6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cdab6-135">System.String</span></span>

## <span data-ttu-id="cdab6-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdab6-136">OUTPUTS</span></span>

### <span data-ttu-id="cdab6-137">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="cdab6-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="cdab6-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdab6-138">NOTES</span></span>
<span data-ttu-id="cdab6-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Problembehandlung, VPN, Verbindung</span><span class="sxs-lookup"><span data-stu-id="cdab6-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="cdab6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdab6-140">RELATED LINKS</span></span>

[<span data-ttu-id="cdab6-141">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cdab6-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cdab6-142">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdab6-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cdab6-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdab6-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cdab6-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdab6-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cdab6-145">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdab6-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdab6-146">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cdab6-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cdab6-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdab6-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdab6-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdab6-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdab6-149">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdab6-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdab6-150">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cdab6-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cdab6-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cdab6-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cdab6-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cdab6-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cdab6-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cdab6-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
