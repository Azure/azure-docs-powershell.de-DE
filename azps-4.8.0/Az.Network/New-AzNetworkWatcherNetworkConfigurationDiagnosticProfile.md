---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165219"
---
# <span data-ttu-id="e05d8-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="e05d8-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="e05d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e05d8-102">SYNOPSIS</span></span>
<span data-ttu-id="e05d8-103">Erstellt ein neues Diagnose Profilobjekt für die Netzwerkkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e05d8-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="e05d8-104">Dieses Objekt wird verwendet, um die Netzwerkkonfiguration während einer Diagnosesitzung unter Verwendung der angegebenen Kriterien zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="e05d8-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="e05d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e05d8-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e05d8-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e05d8-106">DESCRIPTION</span></span>
<span data-ttu-id="e05d8-107">Mit dem New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile-Cmdlet wird ein neues Diagnostic profile-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="e05d8-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="e05d8-108">Dieses Objekt wird verwendet, um die Netzwerkkonfiguration während einer Netzwerk Konfigurationsdiagnose Sitzung unter Verwendung der angegebenen Kriterien zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="e05d8-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="e05d8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e05d8-109">EXAMPLES</span></span>

### <span data-ttu-id="e05d8-110">Beispiel 1: Aufrufen der Netzwerkkonfigurations-Diagnosesitzung für VM und festgelegtes Netzwerkprofil</span><span class="sxs-lookup"><span data-stu-id="e05d8-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="e05d8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e05d8-111">PARAMETERS</span></span>

### <span data-ttu-id="e05d8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05d8-112">-DefaultProfile</span></span>
<span data-ttu-id="e05d8-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e05d8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05d8-114">-Ziel</span><span class="sxs-lookup"><span data-stu-id="e05d8-114">-Destination</span></span>
<span data-ttu-id="e05d8-115">Traffic-Ziel.</span><span class="sxs-lookup"><span data-stu-id="e05d8-115">Traffic destination.</span></span>
<span data-ttu-id="e05d8-116">Akzeptierte Werte sind: "\*", IP-Adresse/CIDR, Service-Tag.</span><span class="sxs-lookup"><span data-stu-id="e05d8-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="e05d8-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e05d8-117">-DestinationPort</span></span>
<span data-ttu-id="e05d8-118">Ziel-Port für den Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="e05d8-118">Traffic destination port.</span></span>
<span data-ttu-id="e05d8-119">Akzeptierte Werte sind "\*", Port (beispielsweise 3389) und Portbereich (beispielsweise 80-100).</span><span class="sxs-lookup"><span data-stu-id="e05d8-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="e05d8-120">-Richtung</span><span class="sxs-lookup"><span data-stu-id="e05d8-120">-Direction</span></span>
<span data-ttu-id="e05d8-121">Die Richtung des Datenverkehrs.</span><span class="sxs-lookup"><span data-stu-id="e05d8-121">The direction of the traffic.</span></span>
<span data-ttu-id="e05d8-122">Akzeptierte Werte sind "eingehend" und "ausgehend"</span><span class="sxs-lookup"><span data-stu-id="e05d8-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="e05d8-123">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e05d8-123">-Protocol</span></span>
<span data-ttu-id="e05d8-124">Protokoll, das überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="e05d8-124">Protocol to be verified on.</span></span>
<span data-ttu-id="e05d8-125">Akzeptierte Werte sind "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="e05d8-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="e05d8-126">-Source</span><span class="sxs-lookup"><span data-stu-id="e05d8-126">-Source</span></span>
<span data-ttu-id="e05d8-127">Datenverkehrs Quelle.</span><span class="sxs-lookup"><span data-stu-id="e05d8-127">Traffic source.</span></span>
<span data-ttu-id="e05d8-128">Akzeptierte Werte sind "\*", IP-Adresse/CIDR, Service-Tag.</span><span class="sxs-lookup"><span data-stu-id="e05d8-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="e05d8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05d8-129">CommonParameters</span></span>
<span data-ttu-id="e05d8-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05d8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05d8-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05d8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05d8-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e05d8-132">INPUTS</span></span>

### <span data-ttu-id="e05d8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e05d8-133">System.String</span></span>

## <span data-ttu-id="e05d8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e05d8-134">OUTPUTS</span></span>

### <span data-ttu-id="e05d8-135">Microsoft. Azure. Commands. Network. Models. PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="e05d8-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="e05d8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e05d8-136">NOTES</span></span>
<span data-ttu-id="e05d8-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Watcher, Diagnose, Profil</span><span class="sxs-lookup"><span data-stu-id="e05d8-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="e05d8-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e05d8-138">RELATED LINKS</span></span>

[<span data-ttu-id="e05d8-139">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e05d8-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e05d8-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e05d8-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e05d8-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e05d8-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e05d8-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e05d8-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e05d8-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e05d8-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e05d8-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e05d8-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e05d8-145">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e05d8-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e05d8-146">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e05d8-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e05d8-147">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e05d8-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e05d8-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e05d8-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e05d8-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e05d8-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e05d8-150">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e05d8-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e05d8-151">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e05d8-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e05d8-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e05d8-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e05d8-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e05d8-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e05d8-154">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05d8-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05d8-155">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05d8-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05d8-156">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05d8-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05d8-157">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e05d8-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e05d8-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05d8-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05d8-159">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05d8-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05d8-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e05d8-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e05d8-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e05d8-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e05d8-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e05d8-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e05d8-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e05d8-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e05d8-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e05d8-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e05d8-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05d8-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
