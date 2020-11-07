---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847532"
---
# <span data-ttu-id="cb8c8-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb8c8-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="cb8c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8c8-103">Erstellt ein Streaming-MapReduce-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="cb8c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb8c8-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb8c8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb8c8-105">DESCRIPTION</span></span>
<span data-ttu-id="cb8c8-106">Das Cmdlet **New-AzHDInsightStreamingMapReduceJobDefinition** definiert ein Streaming-MapReduce-Auftragsobjekt zur Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cb8c8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb8c8-107">EXAMPLES</span></span>

### <span data-ttu-id="cb8c8-108">Beispiel 1: Erstellen einer Streaming-MapReduce-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="cb8c8-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="cb8c8-109">Dieser Befehl erstellt eine Streaming-MapReduce-Auftragsdefinition.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="cb8c8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb8c8-110">PARAMETERS</span></span>

### <span data-ttu-id="cb8c8-111">-Argumente</span><span class="sxs-lookup"><span data-stu-id="cb8c8-111">-Arguments</span></span>
<span data-ttu-id="cb8c8-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="cb8c8-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="cb8c8-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb8c8-114">-CommandEnvironment</span></span>
<span data-ttu-id="cb8c8-115">Gibt ein Array mit Befehlszeilen Umgebungsvariablen an, die festgelegt werden sollen, wenn ein Auftrag auf Worker-Knoten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="cb8c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8c8-116">-DefaultProfile</span></span>
<span data-ttu-id="cb8c8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cb8c8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb8c8-118">– Definiert</span><span class="sxs-lookup"><span data-stu-id="cb8c8-118">-Defines</span></span>
<span data-ttu-id="cb8c8-119">Gibt Hadoop-Konfigurationswerte an, die für die Ausführung des Auftrags festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="cb8c8-120">-Datei</span><span class="sxs-lookup"><span data-stu-id="cb8c8-120">-File</span></span>
<span data-ttu-id="cb8c8-121">Gibt den Pfad zu einer Datei an, die eine auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="cb8c8-122">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="cb8c8-123">-Dateien</span><span class="sxs-lookup"><span data-stu-id="cb8c8-123">-Files</span></span>
<span data-ttu-id="cb8c8-124">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="cb8c8-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="cb8c8-125">-InputPath</span></span>
<span data-ttu-id="cb8c8-126">Gibt den Pfad zu den Eingabedateien an.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="cb8c8-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="cb8c8-127">-Mapper</span></span>
<span data-ttu-id="cb8c8-128">Gibt einen Mapper-Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="cb8c8-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="cb8c8-129">-OutputPath</span></span>
<span data-ttu-id="cb8c8-130">Gibt den Pfad für die Auftragsausgabe an.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="cb8c8-131">-Reduzierstück</span><span class="sxs-lookup"><span data-stu-id="cb8c8-131">-Reducer</span></span>
<span data-ttu-id="cb8c8-132">Gibt einen Reduzierer-Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="cb8c8-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="cb8c8-133">-StatusFolder</span></span>
<span data-ttu-id="cb8c8-134">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="cb8c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8c8-135">CommonParameters</span></span>
<span data-ttu-id="cb8c8-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8c8-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb8c8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8c8-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb8c8-138">INPUTS</span></span>

### <span data-ttu-id="cb8c8-139">Keine</span><span class="sxs-lookup"><span data-stu-id="cb8c8-139">None</span></span>

## <span data-ttu-id="cb8c8-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb8c8-140">OUTPUTS</span></span>

### <span data-ttu-id="cb8c8-141">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb8c8-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="cb8c8-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb8c8-142">NOTES</span></span>

## <span data-ttu-id="cb8c8-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb8c8-143">RELATED LINKS</span></span>

[<span data-ttu-id="cb8c8-144">Anfang-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cb8c8-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


