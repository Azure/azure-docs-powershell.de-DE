---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497901"
---
# New-AzureBatchJobSchedule

## Synopsis
Erstellt einen Auftragszeitplan im Stapelverarbeitungs Dienst.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureBatchJobSchedule** erstellt einen Auftragszeitplan im Azure-Stapelverarbeitungs Dienst.
Der Parameter *BatchAccountContext* gibt das Konto an, in dem dieses Cmdlet den Terminplan erstellt.

## Beispiele

### Beispiel 1: Erstellen eines Auftragszeitplans
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

In diesem Beispiel wird ein Auftragszeitplan erstellt.

Mit den ersten fünf Befehlen werden **PSSchedule** -, **PSJobSpecification** -und **PSPoolInformation** -Objekte erstellt und geändert.
Die Befehle verwenden das New-Object-Cmdlet und die standardmäßige Azure PowerShell-Syntax.
Die Befehle speichern diese Objekte in den Variablen $Schedule und $JobSpecification.

Der endgültige Befehl erstellt einen Auftragszeitplan mit der ID JobSchedule17.
Dieser Zeitplan erstellt Aufträge mit einem Serienintervall von einem Tag.
Die im Pool ausgeführten Aufträge, die die ID-ContosoPool06 aufweisen, wie im fünften Befehl angegeben.
Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.

## Parameter

### -Batchcontext
Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.
Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DisplayName
Gibt einen Anzeigenamen für den Auftragszeitplan an.

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

### -ID
Gibt die ID des vom Cmdlet erstellten Auftragszeitplans an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobSpecification
Gibt die Details der Aufträge an, die dieses Cmdlet in den Auftragszeitplan einschließt.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadaten
Gibt Metadaten als Schlüssel-Wert-Paare an, die dem Auftragszeitplan hinzugefügt werden sollen.
Der Schlüssel ist der Name der Metadaten.
Der Wert ist der Wert für Metadaten.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Terminplan
Gibt den Zeitplan an, der festlegt, wann Aufträge erstellt werden sollen.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
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

### BatchAccountContext
Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Deaktivieren-AzureBatchJobSchedule](./Disable-AzureBatchJobSchedule.md)

[Enable-AzureBatchJobSchedule](./Enable-AzureBatchJobSchedule.md)

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJobSchedule](./Get-AzureBatchJobSchedule.md)

[Remove-AzureBatchJobSchedule](./Remove-AzureBatchJobSchedule.md)

[Stopp-AzureBatchJobSchedule](./Stop-AzureBatchJobSchedule.md)

[Azure Batch-Cmdlets](./AzureRM.Batch.md)


