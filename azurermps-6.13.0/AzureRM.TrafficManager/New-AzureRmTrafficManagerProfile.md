---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664302"
---
# New-AzureRmTrafficManagerProfile

## Synopsis
Erstellt ein Traffic Manager-Profil.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmTrafficManagerProfile** erstellt ein Azure Traffic Manager-Profil.
Geben Sie den Parameter *Name* und die erforderlichen Einstellungen an.
Dieses Cmdlet gibt ein lokales Objekt zurück, das das neue Profil darstellt.

Dieses Cmdlet konfiguriert keine Datenverkehrs-Manager-Endpunkte.
Sie können das lokale Profilobjekt mithilfe des Add-AzureRmTrafficManagerEndpointConfig-Cmdlets aktualisieren.
Laden Sie dann Änderungen an Traffic Manager mithilfe des Set-AzureRmTrafficManagerProfile-Cmdlets hoch.
Sie können Endpunkte auch mithilfe des New-AzureRmTrafficManagerEndpoint-Cmdlets hinzufügen.

## Beispiele

### Beispiel 1: Erstellen eines Profils
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

Dieser Befehl erstellt ein Azure Traffic Manager-Profil mit dem Namen ContosoProfile in der Ressourcengruppen-ResourceGroup11.
Der DNS-FQDN lautet contosoapp.Trafficmanager.net.

## Parameter

### -CustomHeader
Liste der benutzerdefinierten Headername-und Wert-Paare für Prüf Punkt Anforderungen

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
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

### -ExpectedStatusCodeRange
Liste der erwarteten HTTP-Statuscode Bereiche für Prüf Punkt Anforderungen

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxReturn
Die maximale Anzahl von Antworten, die für Profile mit einer mehrwertigen Routingmethode zurückgegeben wurden.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorIntervalInSeconds
Das Intervall (in Sekunden), in dem der Datenverkehrs-Manager die Integrität der einzelnen Endpunkt in diesem Profil überprüft. Der Standardwert ist 30.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorPath
Gibt den Pfad an, der zum Überwachen des Endpunkt Zustands verwendet wird.
Geben Sie einen Wert relativ zum Endpunkt Domänennamen an.
Dieser Wert muss mit einem Schrägstrich (/) beginnen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorPort
Gibt den TCP-Port an, der zum Überwachen des Endpunkt Zustands verwendet wird.
Gültige Werte sind ganze Zahlen von 1 bis 65535.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorProtocol
Gibt das Protokoll an, das zum Überwachen der Endpunkt Integrität verwendet werden soll.
Gültige Werte sind:

- HTTP
- HTTPS

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorTimeoutInSeconds
Die Zeit (in Sekunden), die der Datenverkehrs-Manager Endpunkten in diesem Profil ermöglicht, auf die Integritätsprüfung zu reagieren. Der Standardwert ist 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorToleratedNumberOfFailures
Die Anzahl der aufeinander folgenden fehlgeschlagenen Integritätsprüfungen, die vom Datenverkehrs Manager toleriert werden, bevor ein Endpunkt in diesem Profil nach der nächsten fehlgeschlagenen Integritätsprüfung in Folgefehler Haft deklariert wird. Der Standardwert ist 3.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für das von diesem Cmdlet erstellte Datenverkehrs-Manager-Profil an.

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

### -ProfileStatus
Gibt den Status des Profils an.
Gültige Werte sind: Enabled und Disabled.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RelativeDnsName
Gibt den relativen DNS-Namen an, der in diesem Datenverkehrs-Manager-Profil bereitgestellt wird.
Traffic Manager kombiniert diesen Wert und den DNS-Domänennamen, den Azure Traffic Manager verwendet, um den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Profils zu bilden.

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

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.
Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe erstellt, die dieser Parameter angibt.

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

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist. Zum Beispiel:

@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficRoutingMethod
Gibt die Datenverkehrs Routingmethode an.
Diese Methode bestimmt, welcher Endpunkt Datenverkehrs-Manager als Antwort auf eingehende DNS-Abfragen zurückgibt.
Gültige Werte sind:

- Leistung
- Gewichteten
- Priorität
- Geografische

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TTL
Gibt den Wert für DNS Time to Live (TTL) an.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Dieses Cmdlet gibt ein neues TrafficManagerProfile-Objekt zurück.

## Notizen

## Verwandte Links

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Deaktivieren-AzureRmTrafficManagerProfile](./Disable-AzureRmTrafficManagerProfile.md)

[Enable-AzureRmTrafficManagerProfile](./Enable-AzureRmTrafficManagerProfile.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)

[Satz-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


