---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 510d0ee001e4c291dad3cc024f593d1f29c7ddca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840983"
---
# Get-UsageAggregates

## Synopsis
Ruft die gemeldeten Azure-Abonnement Nutzungsdetails ab.

## Syntax

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-UsageAggregates** " ruft aggregierte Azure-Abonnement Nutzungsdaten mit den folgenden Eigenschaften ab: 
- Anfangs-und Endzeiten für den Zeitpunkt, zu dem die Verwendung gemeldet wurde.
- Aggregations Genauigkeit, entweder täglich oder stündlich.
- Details der Instanzebene für mehrere Instanzen der gleichen Ressource.
Für konsistente Ergebnisse basieren die zurückgegebenen Daten auf dem Zeitpunkt, zu dem die Nutzungsdetails von der Azure-Ressource gemeldet wurden.
Weitere Informationen finden Sie unter Referenz zu Azure Billing-Ruhe-API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in der Microsoft Developer Network Library.

## Beispiele

### Beispiel 1: Abrufen von Abonnementdaten
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Dieser Befehl ruft die gemeldeten Nutzungsdaten für das Abonnement zwischen 5/2/2015 und 5/5/2015 ab.

## Parameter

### -AggregationGranularity
Gibt die Aggregations Genauigkeit der Daten an.
Gültige Werte sind: täglich und stündlich.
Der Standardwert ist Daily.

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
Bei einem umfangreichen Resultset werden Antworten mithilfe von Fortsetzungstoken ausgelagert.
Das Fortsetzungstoken dient als Textmarke für den Fortschritt.
Wenn Sie diesen Parameter nicht angeben, werden die Daten aus dem Anfang des in *ReportedStartTime* angegebenen Tages oder der Stunde abgerufen.
Wir empfehlen, dass Sie dem nächsten Link auf der Seite Antwort auf die Daten folgen.

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

### -ReportedEndTime
Gibt die gemeldete Endzeit für den Zeitpunkt an, zu dem die Ressourcenverwendung im Azure-Abrechnungssystem aufgezeichnet wurde.
Azure ist ein verteiltes System, das mehrere Rechenzentren in der ganzen Welt umfasst, sodass eine Verzögerung zwischen dem Zeitpunkt der tatsächlichen Nutzung der Ressource, der Ressourcen Nutzungszeit und dem Erreichen des Abrechnungssystems, dem Zeitpunkt, zu dem die Ressourcenverwendung gemeldet wurde, besteht.
Um alle nutzungsereignisse für ein Abonnement abzurufen, die für einen Zeitraum gemeldet werden, können Sie nach gemeldeter Zeit Abfragen.
Obwohl Sie nach der angegebenen Zeit Abfragen, aggregiert das Cmdlet die Antwortdaten nach der Ressourcen Nutzungszeit.
Die Ressourcen Nutzungsdaten sind der hilfreiche Drehpunkt für die Datenanalyse.

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
Gibt die gemeldete Startzeit für den Zeitpunkt an, zu dem die Ressourcenverwendung im Azure-Abrechnungssystem aufgezeichnet wurde.

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

### -Show Details
Gibt an, ob dieses Cmdlet Details auf Instanzebene mit den Nutzungsdaten zurückgibt.
Der Standardwert ist $true.
Wenn $false, aggregiert der Dienst die Ergebnisse auf der Serverseite und gibt daher weniger Aggregat Gruppen zurück.
Wenn Sie beispielsweise drei Websites ausführen, erhalten Sie standardmäßig drei Einzelposten für die Websitenutzung.
Wenn der Wert jedoch $false ist, werden alle Daten für die gleiche **Abonnement** -, **Mess** -, **usageStartTime** und **usageEndTime** in einer einzelnen Zeile reduziert.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse

## Notizen

## Verwandte Links