---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500073"
---
# Submit-AzureRmDataLakeAnalyticsJob

## Synopsis
Sendet einen Job.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Auftrag mit Skriptpfad für U-SQL übermitteln
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### U-SQL-Auftrag einreichen
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Job mit Skriptpfad für U-SQL mit reucurrence-Informationen übermitteln
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Senden eines U-SQL-Auftrags mit Serieninformationen
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Auftrag mit Skriptpfad für U-SQL mit reucurrence und Pipelineinformationen übermitteln
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Senden eines U-SQL-Auftrags mit Serien-und Pipelineinformationen
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Mit dem **Submit-AzureRmDataLakeAnalyticsJob-** Cmdlet wird ein Azure Data Lake-Analyse Auftrag übermittelt.

## Beispiele

### Beispiel 1: Einreichen eines Auftrags
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

Mit diesem Befehl wird ein Data Lake-Analyse Auftrag übermittelt.

## Parameter

### -Konto
Gibt den Namen des Daten Lake Analytics-Kontos an.

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

### -CompileMode
Gibt den Kompilierungsmodus des Auftrags an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Semantik
- Voll
- Singlebox

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CompileOnly
Gibt an, dass dieses Cmdlet den Auftrag ohne Ausführung kompiliert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DegreeOfParallelism
Gibt die Daten Lake Analytics Units (DLAU) des Auftrags an, die die maximal zulässige Parallelität des Auftrags angeben.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Auftragsnamen an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pipeline-Nr
Eine ID, die angibt, dass die Übermittlung dieses Auftrags Teil einer Reihe von wiederkehrenden Aufträgen und auch einer Job-Pipeline zugeordnet ist.

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pipelinename
Ein optionaler Anzeigename für die Pipeline, die diesem Auftrag zugeordnet ist.

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineUri
Ein optionaler URI, der mit dem Ursprungs Dienst verknüpft ist, der dieser Pipeline zugeordnet ist.

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priorität
Gibt die Priorität des Auftrags an.
Wenn keine Angabe erfolgt, lautet die Priorität 1000.
Eine niedrige Zahl kennzeichnet eine höhere Auftragspriorität.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Serien-Nr
Eine ID, die angibt, dass die Übermittlung dieses Auftrags Teil einer Reihe von wiederkehrenden Aufträgen mit derselben Serien-ID ist.

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Serienname
Ein optionaler Anzeigename für die Serien Korrelation zwischen Aufträgen.

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunId
Eine ID, die diese bestimmte Durchlauf Iteration der Pipeline identifiziert.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Runtime
Gibt die Laufzeitversion des Auftrags an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skript
Gibt den Inhalt des Skripts an, das ausgeführt werden soll.

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ScriptPath
Gibt den lokalen Dateipfad für das auszuführende Skript an.

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
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

### Zeichenfolge
Der Parameter "Script" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

### JobInformation
Die anfänglichen Auftragsdetails für den gesendeten Auftrag.

## Notizen

## Verwandte Links

[Get-AzureRmDataLakeAnalyticsJob](./Get-AzureRmDataLakeAnalyticsJob.md)

[Stopp-AzureRmDataLakeAnalyticsJob](./Stop-AzureRmDataLakeAnalyticsJob.md)

[Wait-AzureRmDataLakeAnalyticsJob](./Wait-AzureRmDataLakeAnalyticsJob.md)


