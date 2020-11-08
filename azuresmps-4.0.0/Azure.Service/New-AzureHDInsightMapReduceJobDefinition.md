---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006122"
---
# New-AzureHDInsightMapReduceJobDefinition

## Synopsis
Definiert einen neuen MapReduce-Auftrag.

## Syntax

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Version von Azure PowerShell-HDInsight ist veraltet.
Diese Cmdlets werden vom 1. Januar 2017 entfernt.
Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.

Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Das Cmdlet **New-AzureHDInsightMapReduceJobDefinition** definiert einen neuen MapReduce-Auftrag, der auf einem Azure HDInsight-Cluster ausgeführt werden soll.

## Beispiele

### Beispiel 1: Definieren eines MapReduce-Auftrags, Ausführen des Auftrags und Abrufen der Ausgabe
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

Der erste Befehl ruft die ID des aktuellen Abonnements ab und speichert ihn dann in der $SubId-Variablen.

Der zweite Befehl weist den Namen mycluster der $Clustername-Variablen zu.

Der dritte Befehl verwendet das Cmdlet **New-AzureHDInsightMapReduceJobDefinition** , um eine MapReduce-Auftragsdefinition zu erstellen und diese dann in der $WordCountJob-Variable zu speichern.

Der vierte Befehl führt eine Abfolge von Vorgängen mithilfe dieser Cmdlets aus: 

- **Start-AzureHDInsightJob** , um den Auftrag auf $Clustername zu starten. 
- **Warten** Sie, bis der Vorgang abgeschlossen ist, und zeigen Sie den Fortschritt in Richtung AzureHDInsightJob an.
- **Get-AzureHDInsightJobOutput** , um die Ausgabe des Auftrags zu erhalten.

## Parameter

### -Argumente
Gibt ein Array von Argumenten für einen Hadoop-Auftrag an.
Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClassName
Gibt den Namen der Auftragsklasse in der Java-Archivdatei (jar) an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Definiert
Gibt Hadoop-Konfigurationswerte an, die beim Ausführen des Auftrags festgelegt werden sollen.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dateien
Gibt ein Array von WASB-Dateien an, die für einen Auftrag erforderlich sind.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JarFile
Gibt den vollqualifizierten Namen einer JAR-Datei an, die den Code und die Abhängigkeiten eines MapReduce-Auftrags enthält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jobname
Gibt den Namen eines MapReduce-Auftrags an.
Dieser Parameter ist optional.
Wenn Sie diesen Parameter nicht angeben, wird der Wert des *className* -Parameters verwendet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Libjar
Gibt ein Array von LibJar-verweisen des Auftrags an.

```yaml
Type: String[]
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

### -StatusFolder
Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält, einschließlich des Exit-Codes und der Aufgaben Protokolle.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureHDInsightJobOutput](./Get-AzureHDInsightJobOutput.md)

[Neu – AzureHDInsightHiveJobDefinition](./New-AzureHDInsightHiveJobDefinition.md)

[Neu – AzureHDInsightPigJobDefinition](./New-AzureHDInsightPigJobDefinition.md)

[Neu – AzureHDInsightSqoopJobDefinition](./New-AzureHDInsightSqoopJobDefinition.md)

[Anfang-AzureHDInsightJob](./Start-AzureHDInsightJob.md)

[Wait-AzureHDInsightJob](./Wait-AzureHDInsightJob.md)


