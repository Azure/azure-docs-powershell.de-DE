---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
ms.openlocfilehash: 96d3bea781b0c595b54387a9b07b085f173d7b0a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848780"
---
# <span data-ttu-id="6b8ea-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6b8ea-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="6b8ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8ea-103">Ruft den Status der Fluss Protokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b8ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b8ea-104">SYNTAX</span></span>

### <span data-ttu-id="6b8ea-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b8ea-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b8ea-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6b8ea-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b8ea-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b8ea-107">DESCRIPTION</span></span>
<span data-ttu-id="6b8ea-108">Das Get-AzureRmNetworkWatcherFlowLogStatus-Cmdlet ruft den Status der Fluss Protokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="6b8ea-109">Der Status umfasst, ob die Fluss Protokollierung für die bereitgestellte Ressource aktiviert ist, das konfigurierte Speicherkonto zum Senden von Protokollen und die Aufbewahrungsrichtlinie für die Protokolle.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="6b8ea-110">Zurzeit werden Netzwerk Sicherheitsgruppen für die Fluss Protokollierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="6b8ea-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b8ea-111">EXAMPLES</span></span>

### <span data-ttu-id="6b8ea-112">---Beispiel 1: Abrufen des Fluss Protokollierungs Status für eine angegebene NSG---</span><span class="sxs-lookup"><span data-stu-id="6b8ea-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="6b8ea-113">In diesem Beispiel wird der Fluss Protokollierungsstatus für eine Netzwerksicherheitsgruppe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="6b8ea-114">Für den angegebenen NSG ist die Fluss Protokollierung aktiviert, und es wurde keine Aufbewahrungsrichtlinie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="6b8ea-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b8ea-115">PARAMETERS</span></span>

### <span data-ttu-id="6b8ea-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b8ea-116">-AsJob</span></span>
<span data-ttu-id="6b8ea-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6b8ea-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b8ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8ea-118">-DefaultProfile</span></span>
<span data-ttu-id="6b8ea-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b8ea-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b8ea-120">-NetworkWatcher</span></span>
<span data-ttu-id="6b8ea-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="6b8ea-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6b8ea-122">-NetworkWatcherName</span></span>
<span data-ttu-id="6b8ea-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="6b8ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b8ea-125">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6b8ea-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6b8ea-126">-TargetResourceId</span></span>
<span data-ttu-id="6b8ea-127">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-127">The target resource ID.</span></span>

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

### <span data-ttu-id="6b8ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8ea-128">CommonParameters</span></span>
<span data-ttu-id="6b8ea-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8ea-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b8ea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8ea-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b8ea-131">INPUTS</span></span>

### <span data-ttu-id="6b8ea-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b8ea-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6b8ea-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6b8ea-133">System.String</span></span>

## <span data-ttu-id="6b8ea-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b8ea-134">OUTPUTS</span></span>

### <span data-ttu-id="6b8ea-135">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="6b8ea-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="6b8ea-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b8ea-136">NOTES</span></span>
<span data-ttu-id="6b8ea-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Netzwerk, Netzwerk, Watcher, Fluss, Protokolle, flowlog, Protokollierung</span><span class="sxs-lookup"><span data-stu-id="6b8ea-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="6b8ea-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b8ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="6b8ea-139">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6b8ea-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6b8ea-140">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b8ea-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6b8ea-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b8ea-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6b8ea-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b8ea-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6b8ea-143">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b8ea-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b8ea-144">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6b8ea-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6b8ea-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b8ea-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b8ea-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b8ea-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b8ea-147">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b8ea-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b8ea-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6b8ea-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6b8ea-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6b8ea-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6b8ea-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6b8ea-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6b8ea-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6b8ea-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6b8ea-152">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6b8ea-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6b8ea-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6b8ea-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
