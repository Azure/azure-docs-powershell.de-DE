---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 3357eb154f21bc57de6ef60b243571e05bc0c22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663830"
---
# Get-AzureRmSchedulerJob

## Synopsis
Ruft Scheduler-Aufträge ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmSchedulerJob** " ruft Azure Scheduler-Aufträge ab.

## Beispiele

## Parameter

### -JobCollectionName
Gibt den Namen einer Auftrags Sammlung an, die abzurufende Aufträge enthält.

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
Gibt den Namen des abzurufenden Auftrags an.

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

### -JobState
Gibt den Auftragsstatus der abzurufenden Aufträge an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Aktiviert 
- Deaktiviert 
- Faulted 
- Abgeschlossen

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe der Aufträge an, die abgerufen werden sollen.

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

[Neu – AzureRmSchedulerStorageQueueJob](./New-AzureRmSchedulerStorageQueueJob.md)

[Remove-AzureRmSchedulerJob](./Remove-AzureRmSchedulerJob.md)

[Satz-AzureRmSchedulerHttpJob](./Set-AzureRmSchedulerHttpJob.md)

[Satz-AzureRmSchedulerServiceBusQueueJob](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[Satz-AzureRmSchedulerServiceBusTopicJob](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[Satz-AzureRmSchedulerStorageQueueJob](./Set-AzureRmSchedulerStorageQueueJob.md)


