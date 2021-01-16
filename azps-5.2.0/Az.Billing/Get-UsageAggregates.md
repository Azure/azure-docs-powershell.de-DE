---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295618"
---
# Get-UsageAggregates

## SYNOPSIS
Ruft die gemeldeten Nutzungsdetails für das Azure-Abonnement ab.

## SYNTAX

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-UsageAggregates"** ruft nach den folgenden Eigenschaften aggregierte Nutzungsdaten für das Azure-Abonnement ab: 
- Start- und Endzeit, zu der die Nutzung gemeldet wurde.
- Aggregationsgenauigkeit, entweder täglich oder stündlich.
- Detailinformationen auf Instanzenebene für mehrere Instanzen derselben Ressource.
Um konsistente Ergebnisse zu erzielen, basieren die zurückgegebenen Daten darauf, wann die Nutzungsdetails von der Azure-Ressource gemeldet wurden.
Weitere Informationen finden Sie in der Rest-API-Referenz zur Azure-Abrechnung https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) (in der Microsoft Developer Network-Bibliothek).

## BEISPIELE

### Beispiel 1: Abrufen von Abonnementdaten
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Mit diesem Befehl werden die gemeldeten Nutzungsdaten für das Abonnement zwischen dem 02.05.2015 und dem 05.05.2015 abgerufen.

## PARAMETERS

### -AggregationSfunktionen
Gibt die Aggregationsgenauigkeit der Daten an.
Gültige Werte sind: Täglich und stündlich.
Der Standardwert ist "Täglich".

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
Gibt das Fortsetzungstoken an, das im vorherigen Aufruf aus dem Antworttext abgerufen wurde.
Bei einem großen Ergebnissatz werden Antworten mithilfe von Fortsetzungstoken paged angezeigt.
Das Fortsetzungstoken dient als Lesezeichen für den Fortschritt.
Wenn Sie diesen Parameter nicht angeben, werden die Daten vom Anfang des in *ReportedStartTime* angegebenen Tages oder der angegebenen Stunde abgerufen.
Es wird empfohlen, dass Sie den nächsten Link in der Antwort auf die Seite mit den Daten befolgen.

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

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -ReportedEndTime
Gibt die gemeldete Endzeit für die Aufzeichnung der Ressourcennutzung im Azure-Abrechnungssystem an.
Azure ist ein verteiltes System, das sich über mehrere Rechenzentren auf der ganzen Welt erstreckt. Daher gibt es eine Verzögerung zwischen dem tatsächlichen Verbrauch der Ressource, d. h. der Zeit für die Ressourcennutzung und dem Zeitpunkt, zu dem das Verwendungsereignis das Abrechnungssystem erreicht hat. Dies ist die gemeldete Zeit für die Ressourcennutzung.
Um alle Nutzungsereignisse für ein Abonnement zu erhalten, die für einen Zeitraum gemeldet werden, fragen Sie nach der gemeldeten Uhrzeit ab.
Obwohl Sie nach der gemeldeten Zeit abfragen, aggregiert das Cmdlet die Antwortdaten nach der Ressourcennutzungszeit.
Die Ressourcennutzungsdaten sind das nützliche Pivot zum Analysieren der Daten.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Gibt die gemeldete Startzeit für die Aufzeichnung der Ressourcennutzung im Abrechnungssystem von Azure an.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowDetails
Gibt an, ob dieses Cmdlet Details auf Instanzebene mit den Nutzungsdaten zurückgibt.
Der Standardwert ist $True.
Wenn $False, aggregiert der Dienst die Ergebnisse auf serverseitig und gibt daher weniger Aggregatgruppen zurück.
Wenn Sie beispielsweise drei Websites ausführen, erhalten Sie standardmäßig drei Positionen für die Nutzung der Website.
Wenn der Wert jedoch $False, werden alle Daten für dieselbe **subscriptionId,** **meterId,** **usageStartTime** und **usageEndTime** in einer einzelnen Position reduziert.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
