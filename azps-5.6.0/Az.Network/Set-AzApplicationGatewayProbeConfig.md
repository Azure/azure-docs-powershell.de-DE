---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 79fec34cee74dff5253724f91e07393fa65edad2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942403"
---
# Set-AzApplicationGatewayProbeConfig

## SYNOPSIS
Legt die Integritätstestkonfiguration für ein vorhandenes Anwendungsgateway fest.

## SYNTAX

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das Set-AzApplicationGatewayProbeConfig-Cmdlet legt die Integritätstestkonfiguration für ein vorhandenes Anwendungsgateway fest.

## BEISPIELE

### Beispiel 1: Festlegen der Konfiguration für einen Integritätstest auf einem Anwendungsgateway
```powershell
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

Mit diesem Befehl wird die Konfiguration für einen Integritätstest namens Probe05 für das Anwendungsgateway mit dem Namen Gateway bestimmt.
Der Befehl legt außerdem den Schwellenwert für fehlerhafte Fehler auf 8 Wiederholungen und einen Zeitsprung nach 120 Sekunden fest.

### Beispiel 2

Legt die Integritätstestkonfiguration für ein vorhandenes Anwendungsgateway fest. (automatisch generiert)

<!-- Aladdin Generated Example -->
```powershell
Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Interval 30 -Match <PSApplicationGatewayProbeHealthResponseMatch> -Name 'Probe05' -Path '/path/custompath.htm' -PickHostNameFromBackendHttpSettings -Protocol https -Timeout 120 -UnhealthyThreshold 8
```

## PARAMETER

### -ApplicationGateway
Gibt das Anwendungsgateway an, an das dieses Cmdlet einen Prüfpunkt sendet.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -HostName
Gibt den Hostnamen an, an den dieses Cmdlet den Prüfpunkt sendet.

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

### -Interval
Gibt das Sondenintervall in Sekunden an.
Dies ist das Zeitintervall zwischen zwei aufeinander folgenden Sonden.
Dieser Wert liegt zwischen 1 Sekunde und 86400 Sekunden.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Match
Textkörper, der in der Integritätsantwort enthalten sein muss.
Standardwert ist leer

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinServers
Mindestanzahl von Servern, die immer als fehlerfrei gekennzeichnet sind.
Standardwert ist 0

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

### -Name
Gibt den Namen des Prüfpunkts an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Gibt den relativen Pfad des Prüfpunkts an.
Gültige Pfade beginnen mit dem Schrägstrich (/).
Der Prüfpunkt wird an \<Protocol\> :// \<host\> gesendet: \<port\> \<path\> .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PickHostNameFromBackendHttpSettings
Gibt an, ob der Hostheader aus den Http-Einstellungen des Back-Ends ausgewählt werden soll.
Standardwert ist falsch

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

### -Protocol
Gibt das Protokoll an, das zum Senden von Prüfpunkt verwendet wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timeout
Gibt das Testtimeout in Sekunden an.
Dieses Cmdlet kennzeichnet den Prüfpunkt als fehlgeschlagen, wenn bei diesem Timeoutzeitraum keine gültige Antwort empfangen wird.
Gültige Werte liegen zwischen 1 Sekunde und 86400 Sekunden.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnhealthyThreshold
Gibt die Anzahl der Wiederholungsversuche an.
Der Back-End-Server ist nach dem Erreichen des Schwellenwerts für fehlerhafte Tests nach unten gekennzeichnet.
Gültige Werte liegen zwischen 1 Sekunde und 20 Sekunden.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## NOTIZEN

## VERWANDTE LINKS

[Add-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[Get-AzApplicationGatewayProbeConfig](./Get-AzApplicationGatewayProbeConfig.md)

[New-AzApplicationGatewayProbeConfig](./New-AzApplicationGatewayProbeConfig.md)

[Remove-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

