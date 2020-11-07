---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 50f54d258e6b5575983d8cd35f487783ea922eb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843683"
---
# Set-AzApplicationGatewayProbeConfig

## Synopsis
Legt die Konfiguration des Integritäts Prüfpunkts für ein vorhandenes Anwendungs Gateway fest.

## Syntax

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Set-AzApplicationGatewayProbeConfig-Cmdlet legt die Konfiguration des Integritäts Prüfpunkts für ein vorhandenes Anwendungs Gateway fest.

## Beispiele

### Beispiel 1: Einrichten der Konfiguration für einen Integritäts Prüf Punkt auf einem Anwendungsgateway
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

Mit diesem Befehl wird die Konfiguration für einen Integritäts Prüf Punkt mit dem Namen "Probe05" für das Application Gateway mit dem Namen Gateway festgelegt.
Der Befehl legt auch die fehlerhafte Schwelle auf 8 Wiederholungen und Timeouts nach 120 Sekunden fest.

## Parameter

### -ApplicationGateway
Gibt das Anwendungsgateway an, an das dieses Cmdlet eine Sonde sendet.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Hostname
Gibt den Hostnamen an, an den dieses Cmdlet die Sonde sendet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Intervall
Gibt das Prüf punktintervall in Sekunden an.
Dies ist das Zeitintervall zwischen zwei aufeinanderfolgenden Prüfpunkten.
Dieser Wert liegt zwischen 1 Sekunde und 86400 Sekunden.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vergleich
Body, der in der Integritäts Antwort enthalten sein muss.
Der Standardwert ist leer

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinServers
Minimale Anzahl von Servern, die immer als "fehlerfrei" gekennzeichnet sind.
Der Standardwert ist 0.

```yaml
Type: Int32
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
Type: String
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
Die Sonde wird an das \< Protokoll \> :// \< Host \> : \< Port \> \< path gesendet \> .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PickHostNameFromBackendHttpSettings
Gibt an, ob der Hostheader über die HTTP-Back-End-Einstellungen ausgewählt werden soll.
Der Standardwert ist "false".

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

### -Protokoll
Gibt das zum Senden der Sonde verwendete Protokoll an.

```yaml
Type: String
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
Gibt das Prüfpunkt-Timeout in Sekunden an.
Dieses Cmdlet kennzeichnet die Prüfspitze als fehlerhaft, wenn bei diesem Timeoutzeitraum keine gültige Antwort empfangen wird.
Gültige Werte liegen zwischen 1 Sekunde und 86400 Sekunden.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnhealthyThreshold
Gibt die Anzahl der Prüf Punkt Wiederholungen an.
Der Back-End-Server wird markiert, nachdem der Fehlerzähler für aufeinanderfolgende Prüfpunkte den ungesunden Schwellenwert erreicht hat.
Gültige Werte liegen zwischen 1 Sekunde und 20 Sekunden.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSApplicationGateway
Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Notizen

## Verwandte Links

[Add-AzApplicationGatewayProbeConfig]()

[Get-AzApplicationGatewayProbeConfig]()

[Neu – AzApplicationGatewayProbeConfig]()

[Remove-AzApplicationGatewayProbeConfig]()

