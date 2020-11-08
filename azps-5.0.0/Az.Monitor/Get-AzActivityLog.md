---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178818"
---
# Get-AzActivityLog

## Synopsis
Abrufen von Aktivitätsprotokoll Ereignissen

## Syntax

### GetByCorrelationId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Get-AzActivityLog-Cmdlet ruft Aktivitätsprotokoll Ereignisse ab. Die Ereignisse können der aktuellen Abonnement-ID, Korrelations-ID, Ressourcengruppe, Ressourcen-ID oder dem Ressourcenanbieter zugeordnet werden.

## Beispiele

### Beispiel 1: Abrufen eines Ereignisprotokolls nach Abonnement-ID
```
PS C:\>Get-ActivityAzLog
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 2: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

Dieser Befehl listet höchstens 100-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 3: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer Startzeit
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die mit der Abonnement-ID des Benutzers verbunden sind, die am oder nach 2017-06-01T10:30 Ortszeit erfolgt ist, wenn dieses Datum/die Uhrzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.

### Beispiel 4: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit Anfangs-und Endzeit
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Dieser Befehl listet höchstens 1000 der Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die am oder nach 2017-04-01T10:30 Ortszeit und vor 2017-04-14T11:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

### Beispiel 5: Abrufen eines Ereignisprotokolls nach Korrelations-ID
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand. 
**Hinweis** : Dies ist normalerweise nur ein Ereignis.

### Beispiel 6: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand. 
**Hinweis** : Dies ist normalerweise nur ein Ereignis.

### Beispiel 7: Abrufen eines Ereignisprotokolls nach Korrelations-ID und Startzeit
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt ist, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.
**Hinweis** : Dies ist normalerweise nur ein Ereignis.

### Beispiel 8: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit Anfangs-und Endzeit
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

### Beispiel 9: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Dieser Befehl listet höchstens 1000 die Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 10: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 11: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe nach Anfangszeit
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit stattfand, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.

### Beispiel 12: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit Anfangs-und Endzeit
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

### Beispiel 13: Abrufen eines Ereignisprotokolls nach Ressourcen-ID
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 14: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 15: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer Startzeit
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.

### Beispiel 16: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit Anfangs-und Endzeit
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

### Beispiel 17: Abrufen eines Ereignisprotokolls nach dem Ressourcenanbieter
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 18: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

Dieser Befehl listet die meisten 100-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.

### Beispiel 19: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer Startzeit
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Dieser Befehl listet höchstens 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der sich am oder nach 2017-05-22T04:30:00 Ortszeit befindet, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.

### Beispiel 20: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit Anfangs-und Endzeit
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegen, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.

## Parameter

### -Anrufer
Der Aufrufer des abzurufenden Ereignisses

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
Die CorrelationId

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

### -DetailedOutput
Gibt das Objekt mit allen Details der Ereignisse zurück (der Standardwert ist, nur einige Attribute zurückzugeben, also keine Details).

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
Die EndTime der Abfrage

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
Die maximale Anzahl von Datensätzen, die abgerufen werden sollen.
Alias: maxRecords, MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe

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
Die Resourcen--Nr

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
Der Name des ResourceProvider

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
Die CorrelationId der Abfrage

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Der Status der abzurufenden Ereignisse

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

### System. Management. Automation. Switchparameter

### System. Int32

## Ausgaben

### Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData

## Notizen

## Verwandte Links
