---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006256"
---
# Set-AzureSchedulerStorageQueueJob

## Synopsis
Aktualisiert einen Scheduler-Auftrag mit einer Speicheraktion.

## Syntax

### Erforderlich
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Regelmäßige
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet " **Satz-AzureSchedulerStorageQueueJob** " aktualisiert einen Scheduler-Auftrag mit einer Azure-Speicheraktion.

## Beispiele

### Beispiel 1: Aktualisieren einer Speicher Warteschlangen Nachricht
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

Mit diesem Befehl wird die Warteschlangen Meldung für den Speicherauftrag mit dem Namen Job12 aktualisiert.
Der Befehl gibt den Namen der Auftrags Sammlung und den Speicherort an.

### Beispiel 2: Aktivieren eines Speicher Warteschlangenauftrags
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

Mit diesem Befehl wird der Auftrag mit dem Namen Job16 aktiviert.
Der Befehl ändert den Zustand des Auftrags in enabled, indem dieser Wert für den *JobState* -Parameter angegeben wird.

## Parameter

### -EndTime
Gibt eine Uhrzeit als **DateTime** -Objekt an, damit der Planer den Auftrag nicht mehr initiieren kann.
Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionHeaders
Gibt Header als Hashtabelle an.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorActionMethod
Gibt die Methode für http-und HTTPS-Aktionstypen an.
Gültige Werte sind: 

- Erhalten
- Setzen
- Bereitstellen
- Kopf
- Löschen

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionQueueMessageBody
Gibt den Text für die Speicher Auftragsaktionen an.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionRequestBody
Gibt den Textkörper für Put-und Post-Auftragsaktionen an.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionSASToken
Gibt das Shared Access-Signaturtoken (SAS) für die Speicherwarteschlange an.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorActionStorageAccount
Gibt den Namen des speicherkontos an.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorActionStorageQueue
Gibt den Namen der Speicherwarteschlange an.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorActionURI
Gibt den URI für die Fehler Auftragsaktion an.

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExecutionCount
Gibt die Anzahl der Vorkommen eines Auftrags an, die ausgeführt werden.
Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.

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

### -Häufigkeit
Gibt die maximale Häufigkeit für diesen Scheduler-Auftrag an.

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
Gibt das Intervall der Serie mit der Häufigkeit an, die mithilfe des *Frequency* -Parameters angegeben wird.

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

### -JobCollectionName
Gibt den Namen der Sammlung an, die den Scheduler-Job enthalten soll.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Jobname
Gibt den Namen des Scheduler-Auftrags an, der aktualisiert werden soll.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobState
Gibt den Status für den Scheduler-Auftrag an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standort
Gibt den Namen des Speicherorts an, der den clouddienst hostet.
Gültige Werte sind: 

- Überall in Asien
- Überall in Europa
- Überall in den USA
- Ostasien
- East US
- Nord-Zentral-USA
- Nordeuropa
- Süd-Mittelamerika
- Südostasien
- West Europa
- West-US

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt an, dass dieses Cmdlet ein Objekt zurückgibt, das das Element darstellt, auf dem es ausgeführt wird.
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

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

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SASToken
Gibt das SAS-Token für die Speicherwarteschlange an.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Startzeit
Gibt eine Uhrzeit als **DateTime** -Objekt für den Start des Auftrags an.

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQueueAccount
Gibt den Namen des speicherkontos an.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageQueueMessage
Gibt die Warteschlangen Meldung für den Speicherauftrag an.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQueueName
Gibt den Namen der Speicherwarteschlange an.

```yaml
Type: String
Parameter Sets: Required
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

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureSchedulerStorageQueueJob](./New-AzureSchedulerStorageQueueJob.md)


