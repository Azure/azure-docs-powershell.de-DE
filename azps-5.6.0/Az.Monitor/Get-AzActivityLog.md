---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932715"
---
# Get-AzActivityLog

## SYNOPSIS
Abrufen von Aktivitätsprotokollereignissen

## SYNTAX

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

## BESCHREIBUNG
Das Get-AzActivityLog cmdlet ruft Aktivitätsprotokollereignisse ab. Die Ereignisse können der aktuellen Abonnement-ID, Korrelations-ID, Ressourcengruppe, Ressourcen-ID oder Ressourcenanbieter zugeordnet werden.

## BEISPIELE

### Beispiel 1: Erhalten eines Ereignisprotokolls nach Abonnement-ID
```
PS C:\>Get-AzActivityLog
```

Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.

### Beispiel 2: Erhalten eines Ereignisprotokolls nach Abonnement-ID mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

Mit diesem Befehl werden mindestens 100 Ereignisse aufgeführt, die der Abonnement-ID des Benutzers zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.

### Beispiel 3: Erhalten eines Ereignisprotokolls nach Abonnement-ID mit einer Startzeit.
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

Dieser Befehl listet mindestens 1.000 Ereignisse auf, die mit der Abonnement-ID des Benutzers verknüpft sind, die am oder nach dem 06.06.2017 um 10:30 Uhr Ortszeit stattgefunden haben, wenn dieses Datum/diese Uhrzeit nicht älter als 90 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit ist.

### Beispiel 4: Erhalten eines Ereignisprotokolls nach Abonnement-ID mit einer Start- und Endzeit.
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Dieser Befehl listet mindestens 1.000 der Ereignisse auf, die mit der Abonnement-ID des Benutzers verbunden sind, die am oder nach dem 04.04.2017 und vor dem 04.04.2017 und nach 2017-14T11:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/uhrzeit ist, d. h.: der Aufbewahrungszeitraum.

### Beispiel 5: Erhalten eines Ereignisprotokolls nach Korrelations-ID
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Mit diesem Befehl werden mindestens 1.000 Ereignisse aufgeführt, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben. 
**HINWEIS:** Dies ist normalerweise nur ein Ereignis.

### Beispiel 6: Erhalten eines Ereignisprotokolls nach Korrelations-ID mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

Dieser Befehl listet mindestens 100 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben. 
**HINWEIS:** Dies ist normalerweise nur ein Ereignis.

### Beispiel 7: Erhalten eines Ereignisprotokolls nach Korrelations-ID und Startzeit
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach dem 2017-05-22T04:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist.
**HINWEIS:** Dies ist normalerweise nur ein Ereignis.

### Beispiel 8: Erhalten eines Ereignisprotokolls nach Korrelations-ID mit Start- und Endzeit
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach dem 15.04.2017,04:30 Ortszeit, jedoch vor dem 2017-04-25T12:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/Uhrzeit ist, d. h.: der Aufbewahrungszeitraum.

### Beispiel 9: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Dieser Befehl listet mindestens 1000 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.

### Beispiel 10: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

Dieser Befehl listet mindestens 100 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.

### Beispiel 11: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe zur Startzeit
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Dieser Befehl listet mindestens 1000 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach dem 2017-05-22T04:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist.

### Beispiel 12: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe mit einer Start- und Endzeit
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Dieser Befehl listet mindestens 1000 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach dem 04.04.2017,15.04.30 Ortszeit, jedoch vor dem 2017-04-25T12:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/Uhrzeit ist, d. h.: der Aufbewahrungszeitraum.

### Beispiel 13: Erhalten eines Ereignisprotokolls nach Ressourcen-ID
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.

### Beispiel 14: Erhalten eines Ereignisprotokolls nach Ressourcen-ID mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

Dieser Befehl listet mindestens 100 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.

### Beispiel 15: Erhalten eines Ereignisprotokolls nach Ressourcen-ID mit einer Startzeit
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach dem 2017-05-22T04:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist.

### Beispiel 16: Erhalten eines Ereignisprotokolls nach Ressourcen-ID mit einer Start- und Endzeit
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach dem 15.04.2017,04:30 Ortszeit, jedoch vor dem 2017-04-25T12:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/Uhrzeit ist, d. h.: der Aufbewahrungszeitraum.

### Beispiel 17: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

Dieser Befehl listet mindestens 1.000 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.

### Beispiel 18: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter mit einer maximalen Anzahl von Ereignissen
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

Dieser Befehl listet mindestens 100 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.

### Beispiel 19: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter mit einer Startzeit
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Dieser Befehl listet mindestens 1000 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach dem 2017-05-22T04:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist.

### Beispiel 20: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter mit einer Start- und Endzeit
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Dieser Befehl listet mindestens 1.000 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach dem 15.04.2017,04:30 Ortszeit, jedoch vor dem 2017-04-25T12:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/Uhrzeit ist, d. h.: der Aufbewahrungszeitraum.

## PARAMETER

### -Anrufer
Der Aufrufer der ereignisse, die abgerufen werden müssen

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
Die Korrelations-Id

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

### -DetailedOutput
Rückgabeobjekt mit allen Details der Ereignisse (standardmäßig werden nur einige Attribute, d. h. keine Details, zurückgeben)

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
Die EndZeit der Abfrage

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
Die maximale Anzahl von Datensätzen, die abgerufen werden müssen.
Alias: MaxRecords, MaxEvents

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
Name der Ressourcengruppe

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

### -ResourceId
Die ResourceId

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
Name des ResourceProviders

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

### -StartTime
Die Korrelations-Id der Abfrage

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
Der Status der zu abrufende Ereignisse

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

## AUSGABEN

### Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData

## NOTIZEN

## VERWANDTE LINKS
