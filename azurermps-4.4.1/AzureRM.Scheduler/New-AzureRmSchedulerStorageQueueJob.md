---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: ba8d917c33f2ab7ac6c82db303df08c01c648bf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501617"
---
# New-AzureRmSchedulerStorageQueueJob

## Synopsis
Erstellt einen Speicher Warteschlangenauftrag.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmSchedulerStorageQueueJob** erstellt einen Speicher Warteschlangenauftrag in Azure Scheduler.

Dieses Cmdlet unterstützt dynamische Parameter auf Grundlage des *ErrorActionType* -Parameters.
Dynamische Parameter werden auf Grundlage anderer Parameterwerte zur Verfügung gestellt.

Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, nachdem Sie die anderen Parameter angegeben haben, geben Sie einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.
Wenn Sie keinen erforderlichen Parameter angeben, werden Sie vom Cmdlet aufgefordert, den Wert zu überspringen.

## Beispiele

## Parameter

### -EndTime
Gibt eine Endzeit als **DateTime** -Objekt für den Auftrag an.
Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionType
Gibt eine Fehler Aktionseinstellung für den Auftrag an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Http 
- HTTPS 
- StorageQueue 
- ServiceBusQueue 
- ServiceBusTopic

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExecutionCount
Gibt an, wie oft der Auftrag ausgeführt wird.
Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Häufigkeit
Gibt eine Häufigkeit für den Auftrag an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Minuten 
- Stunde 
- Tag 
- Woche 
- Monat

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Intervall
Gibt ein Wiederholungsintervall für den Auftrag an.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Gibt den Namen der Auftrags Sammlung an, zu der der Auftrag gehört.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Jobname
Gibt einen Namen für den Auftrag an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobState
Gibt den Status des Auftrags an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Aktiviert 
- Deaktiviert

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, zu der der Auftrag gehört.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Startzeit
Gibt die Startzeit als **DateTime** -Objekt für den Auftrag an.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQueueAccount
Gibt den Namen eines speicherkontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageQueueMessage
Gibt eine Warteschlangen Meldung für den Speicherauftrag an.

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

### -StorageQueueName
Gibt den Namen einer Speicherwarteschlange an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageSASToken
Gibt ein freigegebenes zugriffssignatur Token für eine Speicherwarteschlange an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition

## Notizen

## Verwandte Links

[Neu – AzureRmSchedulerHttpJob](./New-AzureRmSchedulerHttpJob.md)

[Neu – AzureRmSchedulerJobCollection](./New-AzureRmSchedulerJobCollection.md)

[Neu – AzureRmSchedulerServiceBusQueueJob](./New-AzureRmSchedulerServiceBusQueueJob.md)

[Neu – AzureRmSchedulerServiceBusTopicJob](./New-AzureRmSchedulerServiceBusTopicJob.md)

[Satz-AzureRmSchedulerHttpJob](./Set-AzureRmSchedulerHttpJob.md)

[Satz-AzureRmSchedulerJobCollection](./Set-AzureRmSchedulerJobCollection.md)

[Satz-AzureRmSchedulerServiceBusQueueJob](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[Satz-AzureRmSchedulerServiceBusTopicJob](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[Satz-AzureRmSchedulerStorageQueueJob](./Set-AzureRmSchedulerStorageQueueJob.md)


