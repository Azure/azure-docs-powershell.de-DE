---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: e879de96f861c5a102077c3d392944f79a293b10
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398069"
---
# <span data-ttu-id="9dabf-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="9dabf-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="9dabf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dabf-102">SYNOPSIS</span></span>
<span data-ttu-id="9dabf-103">Erstellt ein neues Diagnoseprofilobjekt für die Netzwerkkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9dabf-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="9dabf-104">Dieses Objekt wird verwendet, um die Netzwerkkonfiguration während einer Diagnosesitzung mithilfe der angegebenen Kriterien einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="9dabf-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="9dabf-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dabf-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9dabf-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dabf-106">DESCRIPTION</span></span>
<span data-ttu-id="9dabf-107">Das New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet erstellt ein neues Diagnoseprofilobjekt.</span><span class="sxs-lookup"><span data-stu-id="9dabf-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="9dabf-108">Dieses Objekt wird verwendet, um die Netzwerkkonfiguration während einer Netzwerkkonfigurationsdiagnosesitzung mit den angegebenen Kriterien einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="9dabf-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="9dabf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9dabf-109">EXAMPLES</span></span>

### <span data-ttu-id="9dabf-110">Beispiel 1: Aufrufen der Netzwerkkonfigurationsdiagnosesitzung für VM und angegebenes Netzwerkprofil</span><span class="sxs-lookup"><span data-stu-id="9dabf-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="9dabf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dabf-111">PARAMETERS</span></span>

### <span data-ttu-id="9dabf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dabf-112">-DefaultProfile</span></span>
<span data-ttu-id="9dabf-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dabf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dabf-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="9dabf-114">-Destination</span></span>
<span data-ttu-id="9dabf-115">Datenverkehrsziel.</span><span class="sxs-lookup"><span data-stu-id="9dabf-115">Traffic destination.</span></span>
<span data-ttu-id="9dabf-116">Akzeptierte Werte sind: '\*', IP Address/CIDR, Service Tag.</span><span class="sxs-lookup"><span data-stu-id="9dabf-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="9dabf-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9dabf-117">-DestinationPort</span></span>
<span data-ttu-id="9dabf-118">Datenverkehrszielport.</span><span class="sxs-lookup"><span data-stu-id="9dabf-118">Traffic destination port.</span></span>
<span data-ttu-id="9dabf-119">Akzeptierte Werte sind "\*", Port (z. B. 3389) und Portbereich (z. B. 80-100).</span><span class="sxs-lookup"><span data-stu-id="9dabf-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="9dabf-120">-Direction</span><span class="sxs-lookup"><span data-stu-id="9dabf-120">-Direction</span></span>
<span data-ttu-id="9dabf-121">Die Richtung des Verkehrs.</span><span class="sxs-lookup"><span data-stu-id="9dabf-121">The direction of the traffic.</span></span>
<span data-ttu-id="9dabf-122">Akzeptierte Werte sind "Eingebunden" und "Ausgehend".</span><span class="sxs-lookup"><span data-stu-id="9dabf-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dabf-123">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9dabf-123">-Protocol</span></span>
<span data-ttu-id="9dabf-124">Das Protokoll, das überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="9dabf-124">Protocol to be verified on.</span></span>
<span data-ttu-id="9dabf-125">Akzeptierte Werte sind "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="9dabf-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="9dabf-126">-Source</span><span class="sxs-lookup"><span data-stu-id="9dabf-126">-Source</span></span>
<span data-ttu-id="9dabf-127">Datenverkehrsquelle.</span><span class="sxs-lookup"><span data-stu-id="9dabf-127">Traffic source.</span></span>
<span data-ttu-id="9dabf-128">Akzeptierte Werte sind "\*", "IP Address/CIDR", "Service Tag".</span><span class="sxs-lookup"><span data-stu-id="9dabf-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="9dabf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dabf-129">CommonParameters</span></span>
<span data-ttu-id="9dabf-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dabf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dabf-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dabf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dabf-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9dabf-132">INPUTS</span></span>

### <span data-ttu-id="9dabf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9dabf-133">System.String</span></span>

## <span data-ttu-id="9dabf-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9dabf-134">OUTPUTS</span></span>

### <span data-ttu-id="9dabf-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="9dabf-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="9dabf-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9dabf-136">NOTES</span></span>
<span data-ttu-id="9dabf-137">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="9dabf-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="9dabf-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9dabf-138">RELATED LINKS</span></span>

[<span data-ttu-id="9dabf-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dabf-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9dabf-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dabf-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9dabf-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dabf-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9dabf-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9dabf-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9dabf-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9dabf-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9dabf-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9dabf-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9dabf-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9dabf-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9dabf-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dabf-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dabf-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9dabf-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9dabf-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dabf-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dabf-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dabf-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dabf-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dabf-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dabf-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9dabf-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9dabf-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9dabf-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9dabf-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9dabf-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9dabf-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dabf-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dabf-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dabf-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dabf-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dabf-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dabf-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9dabf-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9dabf-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dabf-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dabf-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dabf-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dabf-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9dabf-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9dabf-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9dabf-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9dabf-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9dabf-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9dabf-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9dabf-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9dabf-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9dabf-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="9dabf-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dabf-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
