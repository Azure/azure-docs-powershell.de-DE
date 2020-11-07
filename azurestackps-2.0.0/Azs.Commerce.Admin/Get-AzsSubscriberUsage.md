---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844891"
---
# Get-AzsSubscriberUsage

## Synopsis
Ruft eine Sammlung von SubscriberUsageAggregates ab, die von Benutzern UsageAggregates werden.

## Syntax

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Beschreibung
Ruft eine Sammlung von SubscriberUsageAggregates ab, die von Benutzern UsageAggregates werden.

## Beispiele

### Beispiel 1: Abrufen von Nutzungsdaten, die nach Tag aggregiert werden
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

Rufen Sie die Nutzungsdaten für den gesamten Tag des 30. Dezember 2019 (in UTC) für alle Mandanten ab, die vom Tag aggregiert werden.
ReportedStartTime und ReportedEndTime müssen auf Tage gerundet werden.
Wenn Sie als Dienstadministrator aufgerufen wird, werden alle Verwendungsdaten für jeden Mandanten effektiv angezeigt.

### Beispiel 2: Abrufen von Nutzungsdaten, die stundenweise aggregiert sind
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

Besorgen Sie sich die Nutzungsdaten zwischen 12.00-02.00 Uhr am 30. Dezember 2019 (in UTC), aggregiert nach Stunden.
ReportedStartTime und ReportedEndTime müssen auf Stunden gerundet werden.
Wenn Sie als Dienstadministrator aufgerufen werden, werden auch alle Verwendungsdaten für jeden Mandanten angezeigt.

## Parameter

### -AggregationGranularity
Die Aggregations Granularität.

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

### -ContinuationToken
Das Fortsetzungstoken.

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
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ReportedEndTime
Die gemeldete Endzeit (exklusiv).

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
Die gemeldete Startzeit (inklusive).

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

### -Abonnenten-Nr
Die Mandanten-Abonnement-ID.

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

### -Abonnement-Nr
Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. Commerce. Models. Api20150601Preview. IUsageAggregate



## Notizen

## Verwandte Links

