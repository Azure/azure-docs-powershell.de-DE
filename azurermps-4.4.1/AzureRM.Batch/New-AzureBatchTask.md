---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497898"
---
# New-AzureBatchTask

## Synopsis
Erstellt eine Batch Aufgabe unter einem Auftrag.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### JobId_Single (Standard)
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobId_Bulk
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Bulk
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Single
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureBatchTask** erstellt eine Azure-Batch Aufgabe unter dem Auftrag, der durch den *JobID* -Parameter oder den *Job* -Parameter angegeben wird.

## Beispiele

### Beispiel 1: Erstellen einer Batch Aufgabe
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

Mit diesem Befehl wird eine Aufgabe erstellt, die die ID Task23 unter dem Auftrag mit dem Auftrags-000001.
Der Task führt den angegebenen Befehl aus.
Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.

### Beispiel 2: Erstellen einer Batch Aufgabe
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

Dieser Befehl ruft mit dem Cmdlet **Get-AzureBatchJob** den Stapelverarbeitungsauftrag ab, der die ID Job-000001 hat.
Der Befehl übergibt diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Der Befehl erstellt eine Aufgabe mit der ID Task26 unter diesem Auftrag.
Die Aufgabe führt den angegebenen Befehl mithilfe von erhöhten Berechtigungen aus.

### Beispiel 3: Hinzufügen einer Sammlung von Aufgaben zum angegebenen Auftrag mithilfe der Pipeline
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzureRmBatchAccountKeys**.
Der Befehl speichert diesen Objektverweis in der $Context Variablen.

Die nächsten beiden Befehle erstellen **PSCloudTask** -Objekte mithilfe des New-Object-Cmdlets.
Die Befehle speichern die Aufgaben in den Variablen $Task 01 und $Task 02.

Der endgültige Befehl ruft den Stapelverarbeitungsauftrag ab, der die ID Job-000001 mithilfe von **Get-AzureBatchJob**.
Anschließend übergibt der Befehl diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Der Befehl fügt eine Sammlung von Aufgaben unter diesem Auftrag hinzu.
Der Befehl verwendet den in $context gespeicherten Kontext.

### Beispiel 4: Hinzufügen einer Sammlung von Aufgaben zum angegebenen Auftrag
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzureRmBatchAccountKeys**.
Der Befehl speichert diesen Objektverweis in der $Context Variablen.

Die nächsten beiden Befehle erstellen **PSCloudTask** -Objekte mithilfe des New-Object-Cmdlets.
Die Befehle speichern die Aufgaben in den Variablen $Task 01 und $Task 02.

Der letzte Befehl fügt die Aufgaben, die in $Task 01 und $Task 02 gespeichert sind, unter dem Job hinzu, der die ID Job-000001.

## Parameter

### -AffinityInformation
Gibt einen Orts Hinweis an, der vom Stapelverarbeitungs Dienst zum Auswählen eines Knotens verwendet wird, für den die Aufgabe ausgeführt werden soll.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationPackageReferences
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -CommandLine
Gibt die Befehlszeile für die Aufgabe an.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Einschränkungen
Gibt die Ausführungs Einschränkungen an, die für diese Aufgabe gelten.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DependsOn
Gibt an, dass die Aufgabe von anderen Aufgaben abhängt.
Die Aufgabe wird erst geplant, wenn alle abhängigen Aufgaben erfolgreich abgeschlossen wurden.

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Gibt den Anzeigenamen der Aufgabe an.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentSettings
Gibt die Umgebungseinstellungen als Schlüssel-Wert-Paare an, die dieses Cmdlet der Aufgabe hinzufügt.
Der Schlüssel ist der Name der Umgebungseinstellung.
Der Wert ist die Umgebungseinstellung.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExitConditions
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die ID der Aufgabe an.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Gibt den Auftrag an, unter dem dieses Cmdlet die Aufgabe erstellt.
Verwenden Sie das Get-AzureBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Gibt die ID des Auftrags an, unter dem dieses Cmdlet die Aufgabe erstellt.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MultiInstanceSettings
Gibt Informationen dazu an, wie eine Aufgabe mit mehreren Instanzen ausgeführt werden kann.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceFiles
Gibt Ressourcendateien als Schlüssel-Wert-Paare an, die für die Aufgabe erforderlich sind.
Der Schlüssel ist der Ressourcen Dateipfad.
Der Wert ist die BLOB-Quelle der Ressourcendatei.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunElevated
Gibt an, dass der Aufgabenprozess mit Administratorrechten ausgeführt wird.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aufgaben
Gibt die Sammlung von Aufgaben an, die hinzugefügt werden sollen.
Jede Aufgabe muss über eine eindeutige ID verfügen.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
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

### PSCloudJob
Der Parameter ' Job ' akzeptiert den Wert vom Typ ' PSCloudJob ' aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Get-AzureBatchTask](./Get-AzureBatchTask.md)

[Neu – AzureBatchTask](./New-AzureBatchTask.md)

[Remove-AzureBatchTask](./Remove-AzureBatchTask.md)

[Stopp-AzureBatchTask](./Stop-AzureBatchTask.md)

[Azure Batch-Cmdlets](./AzureRM.Batch.md)


