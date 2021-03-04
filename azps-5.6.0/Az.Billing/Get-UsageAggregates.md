---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 1947b060f6b1d2fcf7e4380d3a1ece808ea29785
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937155"
---
# Get-UsageAggregates

## SYNOPSIS
Ruft die gemeldeten Details zur Nutzung des Azure-Abonnements ab.

## SYNTAX

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Get-UsageAggregates** ruft aggregierte Azure-Abonnementnutzungsdaten nach den folgenden Eigenschaften ab: 
- Start- und Endzeiten, zu denen die Nutzung gemeldet wurde.
- Aggregationsgenauigkeit( täglich oder stündlich).
- Details auf Instanzebene für mehrere Instanzen derselben Ressource.
Für konsistente Ergebnisse basieren die zurückgegebenen Daten darauf, wann die Nutzungsdetails von der Azure-Ressource gemeldet wurden.
Weitere Informationen finden Sie unter Azure Billing REST API Reference https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( in der Microsoft Developer https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Network-Bibliothek.

## BEISPIELE

### Beispiel 1: Abrufen von Abonnementdaten
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Mit diesem Befehl werden die gemeldeten Nutzungsdaten für das Abonnement zwischen dem 02.05.2015 und dem 05.05.2015 abgerufen.

## PARAMETER

### -AggregationGranularity
Gibt die Aggregationsgenauigkeit der Daten an.
Gültige Werte sind: Täglich und Stündlich.
Der Standardwert ist Täglich.

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
Bei einem großen Ergebnissatz werden Antworten mithilfe von Fortsetzungstoken aus seiteiert.
Das Fortsetzungstoken dient als Lesezeichen für den Fortschritt.
Wenn Sie diesen Parameter nicht angeben, werden die Daten vom Anfang des Tages oder der Stunde abgerufen, der in *ReportedStartTime angegeben ist.*
Es wird empfohlen, den nächsten Link in der Antwort auf die Seite mit den Daten zu folgen.

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

### -ReportedEndTime
Gibt die gemeldete Endzeit für den Zeitpunkt an, zu dem die Ressourcennutzung im Azure-Abrechnungssystem aufgezeichnet wurde.
Azure ist ein verteiltes System, das sich über mehrere Rechenzentren auf der ganzen Welt erstreckt. Daher gibt es eine Verzögerung zwischen dem tatsächlichen Verbrauch der Ressource, d. h. der Ressourcennutzungszeit, und dem Zeitpunkt, zu dem das Nutzungsereignis das Abrechnungssystem erreicht hat. Dabei handelt es sich um die gemeldete Zeit für den Ressourceneinsatz.
Um alle Nutzungsereignisse für ein Abonnement zu erhalten, die für einen Zeitraum gemeldet werden, fragen Sie nach gemeldeter Zeit ab.
Obwohl Sie die Abfrage nach gemeldeter Zeit ausführen, aggregiert das Cmdlet die Antwortdaten nach der Ressourcennutzungszeit.
Die Ressourcennutzungsdaten sind das nützliche Pivot für die Analyse der Daten.

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
Gibt die gemeldete Startzeit für den Zeitpunkt an, zu dem die Ressourcennutzung im Azure-Abrechnungssystem aufgezeichnet wurde.

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
Gibt an, ob dieses Cmdlet Details auf Instanzebene mit den Verwendungsdaten zurückgibt.
Der Standardwert ist $True.
Wenn $False, aggregiert der Dienst die Ergebnisse auf der Serverseite und gibt daher weniger Aggregatgruppen zurück.
Wenn Sie beispielsweise drei Websites ausführen, erhalten Sie standardmäßig drei Zeilenelemente für den Websiteverbrauch.
Wenn der Wert jedoch $False wird, werden alle Daten für das gleiche **AbonnementId,** **meterId,** **usageStartTime** und **usageEndTime** in einem einzigen Zeilenelement reduziert.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## NOTIZEN

## VERWANDTE LINKS
