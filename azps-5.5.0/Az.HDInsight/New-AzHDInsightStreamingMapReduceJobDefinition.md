---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 4f9fe1ef3ab16812553eb6ea22909ce37bd5ee69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167444"
---
# <span data-ttu-id="b3005-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b3005-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="b3005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3005-102">SYNOPSIS</span></span>
<span data-ttu-id="b3005-103">Erstellt ein Streaming-MapReduce-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="b3005-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="b3005-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3005-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3005-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3005-105">DESCRIPTION</span></span>
<span data-ttu-id="b3005-106">Das **Cmdlet "New-AzHDInsightStreamingMapReduceJobDefinition"** definiert ein Auftragsobjekt für "Streaming MapReduce" zur Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="b3005-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b3005-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3005-107">EXAMPLES</span></span>

### <span data-ttu-id="b3005-108">Beispiel 1: Erstellen einer Auftragsdefinition für "Streaming MapReduce"</span><span class="sxs-lookup"><span data-stu-id="b3005-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="b3005-109">Mit diesem Befehl wird eine Auftragsdefinition für Streaming MapReduce erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3005-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="b3005-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3005-110">PARAMETERS</span></span>

### <span data-ttu-id="b3005-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="b3005-111">-Arguments</span></span>
<span data-ttu-id="b3005-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="b3005-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b3005-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="b3005-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b3005-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="b3005-114">-CommandEnvironment</span></span>
<span data-ttu-id="b3005-115">Gibt ein Array von Befehlszeilenumgebungsvariablen an, die festgelegt werden müssen, wenn ein Auftrag auf Workerknoten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3005-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="b3005-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3005-116">-DefaultProfile</span></span>
<span data-ttu-id="b3005-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b3005-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3005-118">-Defines</span><span class="sxs-lookup"><span data-stu-id="b3005-118">-Defines</span></span>
<span data-ttu-id="b3005-119">Gibt die Werte der Hadoop-Konfiguration an, die festgelegt werden müssen, wenn der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3005-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="b3005-120">-File</span><span class="sxs-lookup"><span data-stu-id="b3005-120">-File</span></span>
<span data-ttu-id="b3005-121">Gibt den Pfad zu einer Datei an, die eine Abfrage enthält, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3005-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="b3005-122">Sie können diesen Parameter anstelle des *Abfrageparameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3005-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b3005-123">-Files</span><span class="sxs-lookup"><span data-stu-id="b3005-123">-Files</span></span>
<span data-ttu-id="b3005-124">Gibt eine Sammlung von Dateien an, die einem Strukturauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b3005-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b3005-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="b3005-125">-InputPath</span></span>
<span data-ttu-id="b3005-126">Gibt den Pfad zu den Eingabedateien an.</span><span class="sxs-lookup"><span data-stu-id="b3005-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="b3005-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="b3005-127">-Mapper</span></span>
<span data-ttu-id="b3005-128">Gibt den Namen einer Mapper-Datei an.</span><span class="sxs-lookup"><span data-stu-id="b3005-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="b3005-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b3005-129">-OutputPath</span></span>
<span data-ttu-id="b3005-130">Gibt den Pfad für die Auftragsausgabe an.</span><span class="sxs-lookup"><span data-stu-id="b3005-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="b3005-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="b3005-131">-Reducer</span></span>
<span data-ttu-id="b3005-132">Gibt den Dateinamen "Reducer" an.</span><span class="sxs-lookup"><span data-stu-id="b3005-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="b3005-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b3005-133">-StatusFolder</span></span>
<span data-ttu-id="b3005-134">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="b3005-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b3005-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3005-135">CommonParameters</span></span>
<span data-ttu-id="b3005-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3005-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3005-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3005-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3005-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3005-138">INPUTS</span></span>

### <span data-ttu-id="b3005-139">Keine</span><span class="sxs-lookup"><span data-stu-id="b3005-139">None</span></span>

## <span data-ttu-id="b3005-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3005-140">OUTPUTS</span></span>

### <span data-ttu-id="b3005-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b3005-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="b3005-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3005-142">NOTES</span></span>

## <span data-ttu-id="b3005-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3005-143">RELATED LINKS</span></span>

[<span data-ttu-id="b3005-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b3005-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


