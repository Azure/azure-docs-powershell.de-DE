---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
ms.openlocfilehash: 90f65c7e3db862ca4d24b67187f587511593be4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496101"
---
# Get-AzureRmLog

## Synopsis
Ruft ein Protokoll von Ereignissen ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### GetByCorrelationId
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmLog** " Ruft ein Protokoll von Ereignissen ab.
Die Ereignisse können der aktuellen Abonnement-ID, Korrelations-ID, Ressourcengruppe, Ressourcen-ID oder dem Ressourcenanbieter zugeordnet werden.

## Beispiele

### Beispiel 1: Abrufen eines Ereignisprotokolls nach Abonnement-ID
```
PS C:\>Get-AzureRmLog
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 2: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

Dieser Befehl listet höchstens 100-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 3: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer Startzeit
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die mit der Abonnement-ID des Benutzers verbunden sind, die am oder nach 2017-06-01T10:30 Ortszeit erfolgt ist, wenn dieses Datum/die Uhrzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.

### Beispiel 4: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit Anfangs-und Endzeit
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Dieser Befehl listet höchstens 1000 der Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die am oder nach 2017-04-01T10:30 Ortszeit und vor 2017-04-14T11:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

### Beispiel 5: Abrufen eines Ereignisprotokolls nach Korrelations-ID
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand. 
**Hinweis** : Dies ist normalerweise nur ein Ereignis.

### Beispiel 6: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand. 
**Hinweis** : Dies ist normalerweise nur ein Ereignis.

### Beispiel 7: Abrufen eines Ereignisprotokolls nach Korrelations-ID und Startzeit
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt ist, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.
**Hinweis** : Dies ist normalerweise nur ein Ereignis.

### Beispiel 8: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit Anfangs-und Endzeit
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

### Beispiel 9: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe
```
PS C:\>Get-AzureRmLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Dieser Befehl listet höchstens 1000 die Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 10: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 11: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe nach Anfangszeit
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Dieser Befehl listet höchstens 1000 Evetns auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.

### Beispiel 12: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit Anfangs-und Endzeit
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

### Beispiel 13: Abrufen eines Ereignisprotokolls nach Ressourcen-ID
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 14: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 15: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer Startzeit
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.

### Beispiel 16: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit Anfangs-und Endzeit
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

### Beispiel 17: Abrufen eines Ereignisprotokolls nach dem Ressourcenanbieter
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 18: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

Dieser Befehl listet die meisten 100-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 19: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer Startzeit
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der sich am oder nach 2017-05-22T04:30:00 Ortszeit befindet, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.

### Beispiel 20: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit Anfangs-und Endzeit
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegen, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

## Parameter

### -Anrufer
Gibt einen Anrufer an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CorrelationId
Gibt die Korrelations-ID an.
Dieser Parameter ist erforderlich.

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -DetailedOutput
Gibt an, dass dieses Cmdlet eine detaillierte Ausgabe anzeigt.
Standardmäßig wird die Ausgabe zusammengefasst.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
Gibt die Endzeit der Abfrage in Ortszeit an.
Der Standardwert ist die aktuelle Uhrzeit.
Der Wert muss nach dem *Start* Zeitpunkt liegen.
Sie können das Get-Date-Cmdlet verwenden, um ein **DateTime** -Objekt abzurufen.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
Gibt die Gesamtanzahl der Datensätze an, die für den angegebenen Filter abgerufen werden sollen.
Der Standardwert ist 1000, und der maximal zulässige Wert ist 100000. Negative Werte und 0 werden ignoriert, und der Standardwert wird verwendet.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Gibt die Ressourcen-ID an.

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
Gibt einen Filter nach Ressourcenanbieter an.

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Startzeit
Gibt die Startzeit der Abfrage in Ortszeit an.
Der Standardwert ist *EndTime* minus sieben Tage.
Sie können das Get-Date-Cmdlet verwenden, um ein **DateTime** -Objekt abzurufen.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Gibt den Status an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. String

### System. Management. Automation. Switchparameter

### System. Int32

## Ausgaben

### Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData

## Notizen

## Verwandte Links
