---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841568"
---
# <span data-ttu-id="60172-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="60172-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="60172-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60172-102">SYNOPSIS</span></span>
<span data-ttu-id="60172-103">Ruft den Status der Fluss Protokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="60172-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="60172-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60172-104">SYNTAX</span></span>

### <span data-ttu-id="60172-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="60172-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60172-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="60172-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60172-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60172-107">DESCRIPTION</span></span>
<span data-ttu-id="60172-108">Das Get-AzNetworkWatcherFlowLogStatus-Cmdlet ruft den Status der Fluss Protokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="60172-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="60172-109">Der Status umfasst, ob die Fluss Protokollierung für die bereitgestellte Ressource aktiviert ist, das konfigurierte Speicherkonto zum Senden von Protokollen und die Aufbewahrungsrichtlinie für die Protokolle.</span><span class="sxs-lookup"><span data-stu-id="60172-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="60172-110">Zurzeit werden Netzwerk Sicherheitsgruppen für die Fluss Protokollierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60172-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="60172-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60172-111">EXAMPLES</span></span>

### <span data-ttu-id="60172-112">---Beispiel 1: Abrufen des Fluss Protokollierungs Status für eine angegebene NSG---</span><span class="sxs-lookup"><span data-stu-id="60172-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="60172-113">In diesem Beispiel wird der Fluss Protokollierungsstatus für eine Netzwerksicherheitsgruppe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="60172-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="60172-114">Für den angegebenen NSG ist die Fluss Protokollierung aktiviert, und es wurde keine Aufbewahrungsrichtlinie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60172-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="60172-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="60172-115">PARAMETERS</span></span>

### <span data-ttu-id="60172-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60172-116">-AsJob</span></span>
<span data-ttu-id="60172-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="60172-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60172-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60172-118">-DefaultProfile</span></span>
<span data-ttu-id="60172-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60172-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60172-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60172-120">-NetworkWatcher</span></span>
<span data-ttu-id="60172-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="60172-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="60172-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="60172-122">-NetworkWatcherName</span></span>
<span data-ttu-id="60172-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="60172-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="60172-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60172-124">-ResourceGroupName</span></span>
<span data-ttu-id="60172-125">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="60172-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="60172-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="60172-126">-TargetResourceId</span></span>
<span data-ttu-id="60172-127">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="60172-127">The target resource ID.</span></span>

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

### <span data-ttu-id="60172-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60172-128">CommonParameters</span></span>
<span data-ttu-id="60172-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60172-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60172-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60172-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60172-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60172-131">INPUTS</span></span>

### <span data-ttu-id="60172-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60172-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="60172-133">System. String</span><span class="sxs-lookup"><span data-stu-id="60172-133">System.String</span></span>

## <span data-ttu-id="60172-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60172-134">OUTPUTS</span></span>

### <span data-ttu-id="60172-135">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="60172-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="60172-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="60172-136">NOTES</span></span>
<span data-ttu-id="60172-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Netzwerk, Netzwerk, Watcher, Fluss, Protokolle, flowlog, Protokollierung</span><span class="sxs-lookup"><span data-stu-id="60172-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="60172-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60172-138">RELATED LINKS</span></span>

[<span data-ttu-id="60172-139">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="60172-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="60172-140">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60172-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="60172-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60172-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="60172-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60172-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="60172-143">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60172-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="60172-144">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="60172-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="60172-145">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60172-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="60172-146">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60172-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="60172-147">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60172-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="60172-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="60172-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="60172-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="60172-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="60172-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="60172-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="60172-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="60172-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="60172-152">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="60172-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="60172-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="60172-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
