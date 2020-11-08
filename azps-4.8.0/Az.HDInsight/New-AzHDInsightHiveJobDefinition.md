---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009270"
---
# New-AzHDInsightHiveJobDefinition

## Synopsis
Erstellt ein Hive-Auftragsobjekt.

## Syntax

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzHDInsightHiveJobDefinition** definiert ein Hive Job-Objekt zur Verwendung mit einem Azure HDInsight-Cluster.

## Beispiele

### Beispiel 1: Erstellen einer Hive-Auftragsdefinition
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

Mit diesem Befehl wird eine Hive-Auftragsdefinition erstellt.

## Parameter

### -Argumente
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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### – Definiert
Gibt Hadoop-Konfigurationswerte an, die für die Ausführung des Auftrags festgelegt werden sollen.

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

### -Datei
Gibt den Pfad zu einer Datei an, die die auszuführende Abfrage enthält.
Die Datei muss auf dem dem Cluster zugeordneten Speicherkonto verfügbar sein.
Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.

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

### -Dateien
Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.

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

### -Jobname
Gibt den Namen des Auftrags an.

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
Gibt die Hive-Abfrage an.

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
Gibt an, dass dieses Cmdlet eine Datei im standardmäßigen Azure-Speicherkonto erstellt, in dem eine Abfrage gespeichert werden soll.
Dieses Cmdlet übermittelt den Auftrag, der auf diese Datei verweist, als Skript, das ausgeführt werden soll.
Sie können diese Funktion zum Behandeln von Sonderzeichen wie Prozentzeichen (%) verwenden. Dies würde bei einer Auftragsübermittlung über Templeton fehlschlagen, da Templeton eine Abfrage mit einem Prozentzeichen als URL-Parameter interpretiert.

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
Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightHiveJobDefinition

## Notizen

## Verwandte Links

[Anfang-AzHDInsightJob](./Start-AzHDInsightJob.md)


