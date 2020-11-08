---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005846"
---
# Get-AzureHDInsightJobOutput

## Synopsis
Ruft die Protokollausgabe für einen Auftrag ab.

## Syntax

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Version von Azure PowerShell-HDInsight ist veraltet.
Diese Cmdlets werden vom 1. Januar 2017 entfernt.
Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.

Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter Erstellen von Linux-basierten Clustern in [HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).
Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).
Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).

Das Cmdlet " **Get-AzureHDInsightJobOutput** " Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem Cluster zugeordnet ist.
Sie können verschiedene Arten von Auftragsprotokollen abrufen, darunter Standardausgabe, Standardfehler, Vorgangsprotokolle und eine Zusammenfassung der Vorgangsprotokolle.

## Beispiele

### Beispiel 1: Abrufen der Auftragsausgabe
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

Der erste Befehl ruft die ID des aktuellen Abonnements ab und speichert ihn dann in der $SubId-Variablen.

Der zweite Befehl speichert den Namen mycluster in der $Clustername-Variablen.

Der dritte Befehl erstellt eine MapReduce-Auftragsdefinition und speichert Sie dann in der $WordCountJob-Variablen.
Der Befehl übergibt den Auftrag in $WordCountJob an das Cmdlet **Start-AzureHDInsightJob** , um den Auftrag zu starten.
Es übergibt auch $WordCountJob an das **Wait-AzureHDInsightJob-** Cmdlet, um auf den Abschluss des Auftrags zu warten, und dann wird **Get-AzureHDInsightJobOutput** verwendet, um die Ausgabe des Auftrags abzurufen.

## Parameter

### -Zertifikat
Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cluster
Gibt einen Cluster an.
Dieses Cmdlet ruft Auftragsprotokolle aus dem Cluster ab, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DownloadTaskLogs
Gibt an, dass dieses Cmdlet die Vorgangsprotokolle für einen Auftrag abruft.

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

### -Endpunkt
Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.
Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Gibt den Namespace eines HDInsight-Diensts an, wenn Sie den Standardnamespace nicht verwenden möchten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSslErrors
Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Gibt die ID des abzurufenden Auftrags an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -StandardError
Gibt an, dass dieses Cmdlet die StdErr-Ausgabe eines Auftrags abruft.

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

### -StandardOutput
Gibt an, dass dieses Cmdlet die SdtOut-Ausgabe eines Auftrags abruft.

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

### -Abonnement
Gibt das Abonnement an, das den abzurufenden HDInsight-Cluster enthält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskLogsDirectory
Gibt einen lokalen Ordner an, in dem Aufgaben Protokolle gespeichert werden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSummary
Gibt an, dass diese Cmdlets die Zusammenfassung des Vorgangs Protokolls abrufen.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureHDInsightMapReduceJobDefinition](./New-AzureHDInsightMapReduceJobDefinition.md)

[Anfang-AzureHDInsightJob](./Start-AzureHDInsightJob.md)

[Wait-AzureHDInsightJob](./Wait-AzureHDInsightJob.md)
