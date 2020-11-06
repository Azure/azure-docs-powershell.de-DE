---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 7eec69a441efbf1a4d9f73e85a0385c24a012e34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501629"
---
# Get-AzureRmSchedulerJobHistory

## Synopsis
Ruft den Auftragsverlauf ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmSchedulerJobHistory** " Ruft den Verlauf eines Azure Scheduler-Auftrags ab.

## Beispiele

## Parameter

### -JobCollectionName
Gibt den Namen einer Auftrags Sammlung an.

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

### -JobExecutionStatus
Gibt den Status eines Auftrags an.
Dieses Cmdlet ruft das Protokoll ab, das dem von Ihnen angegebenen Status entspricht.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Abgeschlossen 
- Fehlgeschlagen 
- Verschoben

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Jobname
Gibt den Namen eines Auftrags an, für den das Cmdlet das Protokoll abruft.

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

### Microsoft. Azure. Commands. Scheduler. Models. PSJobHistory

## Notizen

## Verwandte Links

[Get-AzureRmSchedulerJob](./Get-AzureRmSchedulerJob.md)


