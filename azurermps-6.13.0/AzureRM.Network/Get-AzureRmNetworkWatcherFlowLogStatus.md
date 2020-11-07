---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: a045acd86141b57d02fef9931cfb01ff8b783e8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662679"
---
# Get-AzureRmNetworkWatcherFlowLogStatus

## Synopsis
Ruft den Status der Fluss Protokollierung für eine Ressource ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SetByResource (Standard)
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByName
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByLocation
```
Get-AzureRmNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Get-AzureRmNetworkWatcherFlowLogStatus-Cmdlet ruft den Status der Fluss Protokollierung für eine Ressource ab. Der Status umfasst, ob die Fluss Protokollierung für die bereitgestellte Ressource aktiviert ist, das konfigurierte Speicherkonto zum Senden von Protokollen und die Aufbewahrungsrichtlinie für die Protokolle. Zurzeit werden Netzwerk Sicherheitsgruppen für die Fluss Protokollierung unterstützt. 

## Beispiele

### Beispiel 1: Abrufen des Fluss Protokollierungs Status für eine angegebene NSG
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

In diesem Beispiel wird der Fluss Protokollierungsstatus für eine Netzwerksicherheitsgruppe abgerufen. Für den angegebenen NSG ist die Fluss Protokollierung aktiviert, und es wurde keine Aufbewahrungsrichtlinie festgelegt.

### Beispiel 2: Abrufen der Fluss Protokollierung und des Datenverkehrsanalyse Status für eine angegebene NSG
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName"
            }
          }
```

In diesem Beispiel wird der Fluss Protokollierungs-und Datenverkehrsanalyse Status für eine Netzwerksicherheitsgruppe abgerufen. In der angegebenen NSG sind Fluss Protokollierung und Datenverkehrsanalyse aktiviert, und es wurde keine Aufbewahrungsrichtlinie festgelegt.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Accept pipeline input: True (ByValue)
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

### -TargetResourceId
Die Ziel Ressourcen-ID.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher
Parameter: NetworkWatcher (ByValue)

### System. String
Parameter: NetworkWatcherName (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSFlowLog

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Netzwerk, Netzwerk, Watcher, Fluss, Protokolle, flowlog, Protokollierung

## Verwandte Links

[Neu – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)

[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)

[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)

[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)

[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)

[Anfang-AzureRmNetworkWatcherResourceTroubleshooting](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[Neu – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)

[Neu – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)

[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)

[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[Neu – AzureRmNetworkWatcherProtocolConfiguration](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[Test-AzureRmNetworkWatcherIPFlow](./Test-AzureRmNetworkWatcherIPFlow.md)

[Test-AzureRmNetworkWatcherConnectivity](./Test-AzureRmNetworkWatcherConnectivity.md)

[Stopp-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[Anfang-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[Satz-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[Satz-AzureRmNetworkWatcherConfigFlowLog](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[Neu – AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[Get-AzureRMNetworkWatcherReachabilityReport](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[Get-AzureRmNetworkWatcherReachabilityProvidersList](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[Get-AzureRmNetworkWatcherFlowLogStatus](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor)
