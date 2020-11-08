---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: 8d3a714f2798c4866df39cd63c664228f078c37c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166217"
---
# Test-AzNetworkWatcherConnectivity

## Synopsis
Gibt Verbindungsinformationen für eine angegebene Quell-VM und ein Ziel zurück.

## Syntax

### SetByResource (Standard)
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByName
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByLocation
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Test-AzNetworkWatcherConnectivity-Cmdlet gibt Verbindungsinformationen für eine angegebene Quell-VM und ein Ziel zurück. Wenn die Verbindung zwischen Quelle und Ziel nicht hergestellt werden kann, gibt das Cmdlet Details zu dem Problem zurück.

## Beispiele

### Beispiel 1: Testen der Netzwerk Überwachungs Konnektivität von einem virtuellen Computer zu einer Website
```powershell
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

In diesem Beispiel wird die Konnektivität von einem virtuellen Computer in Azure zu www.Bing.com getestet.

### Beispiel 2

Gibt Verbindungsinformationen für eine angegebene Quell-VM und ein Ziel zurück. automatisch

<!-- Aladdin Generated Example -->
```powershell
Test-AzNetworkWatcherConnectivity -DestinationAddress 'bing.com' -DestinationPort 80 -NetworkWatcher <PSNetworkWatcher> -SourceId '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0'
```

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -DestinationAddress
Die IP-Adresse oder der URI, in dem die Verbindung hergestellt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ziel-Nr
Die ID der Ressource, in der ein Verbindungsversuch erfolgen soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPort
Port, auf dem die Verbindungsprüfung durchgeführt wird.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Der Speicherort des Netzwerkmonitors.

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkWatcher
Die Netzwerk Überwachungsressource.

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

### -NetworkWatcherName
Der Name des Netzwerkmonitors.

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProtocolConfiguration
Protokollkonfiguration, auf der die Verbindungsprüfung durchgeführt wird.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Netzwerk Überwachungsressourcen Gruppe.

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

### -Quellpfad
Die ID der Ressource, aus der eine Verbindungsüberprüfung initiiert wird.

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

### -SourcePort
Der Quell-Port, von dem eine Verbindungsüberprüfung durchgeführt wird.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher

### System. String

### System. Int32

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor

## Verwandte Links

[Neu – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)

[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)

[Neu – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Neu – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)


[Anfang-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [Neu – AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Stopp-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Anfang-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Satz-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Satz-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Neu – AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)
