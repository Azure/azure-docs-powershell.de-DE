---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 737ccdbd742b3c4cc12518262423e846678cf599
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155580"
---
# Invoke-AzHDInsightHiveJob

## SYNOPSIS
Übermittelt eine Strukturabfrage an einen HDInsight-Cluster und ruft die Abfrageergebnisse in einem Vorgang ab.

## SYNTAX

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Invoke-AzHDInsightHiveJob** übermittelt eine Strukture-Abfrage an einen Azure HDInsight-Cluster und ruft in einem Vorgang Abfrageergebnisse ab.
Verwenden Sie das Use-AzHDInsightCluster-Cmdlet, bevor **Sie Invoke-AzHDInsightHiveJob** aufrufen, um anzugeben, welcher Cluster für die Abfrage verwendet wird.

## BEISPIELE

### Beispiel 1: Übermitteln einer Strukturabfrage an einen Azure -HDInsight-Cluster
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

Mit diesem Befehl wird die Abfrage SHOW TABLES an den Cluster "your-hadoop-001" übermittelt.

## PARAMETERS

### -Arguments
Gibt ein Array von Argumenten für den Auftrag an.
Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultContainer
Gibt den Namen des Standardcontainers im Standardmäßigen Azure Storage-Konto an, das von einem Cluster "HDInsight" verwendet wird.

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

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountKey
Gibt den Kontoschlüssel für das Standardspeicherkonto an, das vom Cluster "HDInsight" verwendet wird.

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

### -DefaultStorageAccountName
Gibt den Namen des Standardspeicherkontos an, das vom Cluster "HDInsight" verwendet wird.

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

### -Defines
Gibt die Werte für die Konfiguration von Hadoop an, die beim Ausgeführten eines Auftrags festgelegt werden.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -File
Gibt den Pfad zu einer Datei in Azure Storage an, die die zu ausführende Abfrage enthält.
Sie können diesen Parameter anstelle des *Abfrageparameters* verwenden.

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

### -Files
Gibt eine Sammlung von Dateien an, die für einen Strukturauftrag erforderlich sind.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Gibt den Namen eines Strukturauftrags an.
Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardwert" "Struktur: \<first 100 characters of Query\> ".

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

### -Query
Gibt die Strukturabfrage an.

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

### -RunAsFileJob
Gibt an, dass dieses Cmdlet eine Datei im Standardmäßigen Azure -Speicherkonto erstellt, in dem eine Abfrage gespeichert werden soll.
Dieses Cmdlet übermittelt den Auftrag, der auf diese Datei verweist, als auszuführende Skript.
Sie können diese Funktion verwenden, um Sonderzeichen wie Prozentzeichen (%) zu behandeln. die bei einer Auftragsübermittlung über Templeton fehlschlagen würden, da Templeton eine Abfrage mit einem Prozentzeichen als einen URL-Parameter interpretiert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatusFolder
Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### System.String

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Use-AzHDInsightCluster](./Use-AzHDInsightCluster.md)


