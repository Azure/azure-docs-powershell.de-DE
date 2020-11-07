---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843599"
---
# <span data-ttu-id="e339d-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e339d-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="e339d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e339d-102">SYNOPSIS</span></span>
<span data-ttu-id="e339d-103">Konfiguriert die Fluss Protokollierung für eine Zielressource.</span><span class="sxs-lookup"><span data-stu-id="e339d-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="e339d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e339d-104">SYNTAX</span></span>

### <span data-ttu-id="e339d-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="e339d-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e339d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e339d-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e339d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e339d-107">DESCRIPTION</span></span>
<span data-ttu-id="e339d-108">Die Set-AzNetworkWatcherConfigFlowLog konfiguriert die Fluss Protokollierung für eine Zielressource.</span><span class="sxs-lookup"><span data-stu-id="e339d-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="e339d-109">Zu konfigurierende Eigenschaften: gibt an, ob die Fluss Protokollierung für die bereitgestellte Ressource aktiviert ist, das konfigurierte Speicherkonto zum Senden von Protokollen und die Aufbewahrungsrichtlinie für die Protokolle.</span><span class="sxs-lookup"><span data-stu-id="e339d-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="e339d-110">Zurzeit werden Netzwerk Sicherheitsgruppen für die Fluss Protokollierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e339d-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="e339d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e339d-111">EXAMPLES</span></span>

### <span data-ttu-id="e339d-112">---Beispiel 1: Konfigurieren der Fluss Protokollierung für ein angegebenes NSG---</span><span class="sxs-lookup"><span data-stu-id="e339d-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="e339d-113">In diesem Beispiel wird der Fluss Protokollierungsstatus für eine Netzwerksicherheitsgruppe konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e339d-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="e339d-114">In der Antwort sehen wir, dass der angegebene NSG die Fluss Protokollierung aktiviert hat und keine Aufbewahrungsrichtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e339d-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="e339d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e339d-115">PARAMETERS</span></span>

### <span data-ttu-id="e339d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e339d-116">-AsJob</span></span>
<span data-ttu-id="e339d-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e339d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e339d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e339d-118">-DefaultProfile</span></span>
<span data-ttu-id="e339d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e339d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e339d-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="e339d-120">-EnableFlowLog</span></span>
<span data-ttu-id="e339d-121">Kennzeichnen, um die Fluss Protokollierung zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e339d-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e339d-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="e339d-122">-EnableRetention</span></span>
<span data-ttu-id="e339d-123">Flag zum Aktivieren/Deaktivieren der Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="e339d-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e339d-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e339d-124">-NetworkWatcher</span></span>
<span data-ttu-id="e339d-125">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="e339d-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="e339d-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e339d-126">-NetworkWatcherName</span></span>
<span data-ttu-id="e339d-127">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="e339d-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="e339d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e339d-128">-ResourceGroupName</span></span>
<span data-ttu-id="e339d-129">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e339d-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e339d-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e339d-130">-RetentionInDays</span></span>
<span data-ttu-id="e339d-131">Die Anzahl der Tage, an denen Fluss Protokolldatensätze beibehalten werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e339d-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="e339d-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e339d-132">-StorageAccountId</span></span>
<span data-ttu-id="e339d-133">Die ID des speicherkontos, das zum Speichern des Fluss Protokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e339d-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="e339d-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e339d-134">-TargetResourceId</span></span>
<span data-ttu-id="e339d-135">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e339d-135">The target resource ID.</span></span>

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

### <span data-ttu-id="e339d-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e339d-136">-Confirm</span></span>
<span data-ttu-id="e339d-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e339d-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e339d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e339d-138">-WhatIf</span></span>
<span data-ttu-id="e339d-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e339d-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e339d-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e339d-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e339d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e339d-141">CommonParameters</span></span>
<span data-ttu-id="e339d-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e339d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e339d-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e339d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e339d-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e339d-144">INPUTS</span></span>

### <span data-ttu-id="e339d-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e339d-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e339d-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="e339d-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="e339d-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e339d-147">OUTPUTS</span></span>

### <span data-ttu-id="e339d-148">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="e339d-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="e339d-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="e339d-149">NOTES</span></span>
<span data-ttu-id="e339d-150">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Netzwerk, Netzwerk, Watcher, Fluss, Protokolle, flowlog, Protokollierung</span><span class="sxs-lookup"><span data-stu-id="e339d-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="e339d-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e339d-151">RELATED LINKS</span></span>

[<span data-ttu-id="e339d-152">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e339d-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e339d-153">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e339d-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e339d-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e339d-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e339d-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e339d-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e339d-156">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e339d-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e339d-157">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e339d-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e339d-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e339d-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e339d-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e339d-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e339d-160">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e339d-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e339d-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e339d-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e339d-162">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e339d-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e339d-163">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e339d-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e339d-164">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e339d-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e339d-165">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e339d-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e339d-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e339d-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
