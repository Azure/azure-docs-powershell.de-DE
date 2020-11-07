---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: cfc5d0999ed9c77e38b83eee99eabbd19dd1e493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665070"
---
# Get-AzureRmDataLakeAnalyticsJobRecurrence

## Synopsis
Ruft einen Daten See-Analyse Auftrags Serien-oder-Seriendruck ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Alle im Konto (Standard)
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Spezifisches Auftrags Rezidiv
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Die **Get-AzureRmDataLakeAnalyticsJobRecurrence-** Funktion Ruft eine angegebene Azure Data Lake Analytics-auftragsserie oder eine Liste der Serie ab.

## Beispiele

### Beispiel 1: Abrufen einer angegebenen Serie
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

Dieser Befehl ruft die angegebene auftragsserie mit der ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' im Konto ' contosoadla ' ab.

### Beispiel 2: Abrufen einer Liste aller Serien im Konto
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

Dieser Befehl ruft eine Liste aller Wiederholungen im Konto "contosoadla" ab.

## Parameter

### -Konto
Name des Daten Lake Analytics-Kontonamens, unter dem die auftragsserie abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Serien-Nr
Die ID der jeweiligen auftragsserie, für die Informationen zurückgegeben werden sollen.

```yaml
Type: System.Guid
Parameter Sets: Specific Job Recurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SubmittedAfter
Ein optionaler Filter, der Auftrags Serien (n) zurückgibt, die nur nach der angegebenen Zeit übermittelt wurden.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedBefore
Ein optionaler Filter, der Auftrags Serien (n) zurückgibt, die nur vor der angegebenen Zeit übermittelt wurden.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String
System. GUID

## Ausgaben

### Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation

## Notizen

## Verwandte Links

