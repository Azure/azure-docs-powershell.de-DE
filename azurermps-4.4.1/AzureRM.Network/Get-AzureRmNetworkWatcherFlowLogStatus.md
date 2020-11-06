---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 1c7e67eacc52e995632a526514c84bf7a9f45425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501741"
---
# <span data-ttu-id="586d4-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="586d4-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="586d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="586d4-102">SYNOPSIS</span></span>
<span data-ttu-id="586d4-103">Ruft den Status der Fluss Protokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="586d4-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="586d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="586d4-104">SYNTAX</span></span>

### <span data-ttu-id="586d4-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="586d4-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="586d4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="586d4-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="586d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="586d4-107">DESCRIPTION</span></span>
<span data-ttu-id="586d4-108">Das Get-AzureRmNetworkWatcherFlowLogStatus-Cmdlet ruft den Status der Fluss Protokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="586d4-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="586d4-109">Der Status umfasst, ob die Fluss Protokollierung für die bereitgestellte Ressource aktiviert ist, das konfigurierte Speicherkonto zum Senden von Protokollen und die Aufbewahrungsrichtlinie für die Protokolle.</span><span class="sxs-lookup"><span data-stu-id="586d4-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="586d4-110">Zurzeit werden Netzwerk Sicherheitsgruppen für die Fluss Protokollierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="586d4-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="586d4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="586d4-111">EXAMPLES</span></span>

### <span data-ttu-id="586d4-112">---Beispiel 1: Abrufen des Fluss Protokollierungs Status für eine angegebene NSG---</span><span class="sxs-lookup"><span data-stu-id="586d4-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
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

<span data-ttu-id="586d4-113">In diesem Beispiel wird der Fluss Protokollierungsstatus für eine Netzwerksicherheitsgruppe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="586d4-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="586d4-114">Für den angegebenen NSG ist die Fluss Protokollierung aktiviert, und es wurde keine Aufbewahrungsrichtlinie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="586d4-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="586d4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="586d4-115">PARAMETERS</span></span>

### <span data-ttu-id="586d4-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="586d4-116">-NetworkWatcher</span></span>
<span data-ttu-id="586d4-117">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="586d4-117">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="586d4-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="586d4-118">-NetworkWatcherName</span></span>
<span data-ttu-id="586d4-119">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="586d4-119">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="586d4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="586d4-120">-ResourceGroupName</span></span>
<span data-ttu-id="586d4-121">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="586d4-121">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586d4-122">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="586d4-122">-TargetResourceId</span></span>
<span data-ttu-id="586d4-123">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="586d4-123">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586d4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="586d4-124">-DefaultProfile</span></span>
<span data-ttu-id="586d4-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="586d4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="586d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="586d4-126">CommonParameters</span></span>
<span data-ttu-id="586d4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="586d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="586d4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="586d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="586d4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="586d4-129">INPUTS</span></span>

### <span data-ttu-id="586d4-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="586d4-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="586d4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="586d4-131">System.String</span></span>

## <span data-ttu-id="586d4-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="586d4-132">OUTPUTS</span></span>

### <span data-ttu-id="586d4-133">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="586d4-133">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="586d4-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="586d4-134">NOTES</span></span>
<span data-ttu-id="586d4-135">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Netzwerk, Netzwerk, Watcher, Fluss, Protokolle, flowlog, Protokollierung</span><span class="sxs-lookup"><span data-stu-id="586d4-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="586d4-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="586d4-136">RELATED LINKS</span></span>

[<span data-ttu-id="586d4-137">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="586d4-137">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="586d4-138">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="586d4-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="586d4-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="586d4-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="586d4-140">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="586d4-140">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="586d4-141">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="586d4-141">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="586d4-142">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="586d4-142">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="586d4-143">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="586d4-143">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="586d4-144">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="586d4-144">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="586d4-145">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="586d4-145">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="586d4-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="586d4-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="586d4-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="586d4-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="586d4-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="586d4-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="586d4-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="586d4-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="586d4-150">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="586d4-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="586d4-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="586d4-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
