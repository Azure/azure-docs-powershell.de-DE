---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165153"
---
# Remove-AzNetworkWatcher

## Synopsis
Entfernt einen Netzwerkmonitor.

## Syntax

### SetByResource
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByLocation
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Remove-AzNetworkWatcher-Cmdlet entfernt eine Network Watcher-Ressource.

## Beispiele

### Beispiel 1: Erstellen und Löschen eines Netzwerkmonitors
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

In diesem Beispiel wird ein Netzwerkmonitor in einer Ressourcengruppe erstellt und anschließend sofort gelöscht. Beachten Sie, dass pro Abonnement nur ein Netzwerkmonitor pro Region erstellt werden kann.
Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Netzwerks zu unterdrücken.

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

### -Name
Der Ressourcenname.

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher

### System. String

## Ausgaben

### System. Boolean

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor

## Verwandte Links

[Neu – AzNetworkWatcher](./New-AzNetworkWatcher.md)

[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)

[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)

[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)

[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)

[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)

[Anfang-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[Neu – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)

[Neu – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)

[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)

[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)

[Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)

[Neu – AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)

[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)

[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)

[Stopp-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)

[Anfang-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)

[Satz-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)

[Satz-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)

[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)

[Neu – AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)

[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)

[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)

[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)

[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)
