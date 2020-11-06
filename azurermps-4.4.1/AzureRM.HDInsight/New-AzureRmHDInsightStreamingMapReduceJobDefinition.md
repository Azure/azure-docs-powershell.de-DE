---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 526f2005f1c6594128af7e259e2ccb0aa296a71b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504165"
---
# <span data-ttu-id="362cf-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="362cf-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="362cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="362cf-102">SYNOPSIS</span></span>
<span data-ttu-id="362cf-103">Erstellt ein Streaming-MapReduce-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="362cf-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="362cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="362cf-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="362cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="362cf-105">DESCRIPTION</span></span>
<span data-ttu-id="362cf-106">Das Cmdlet **New-AzureRmHDInsightStreamingMapReduceJobDefinition** definiert ein Streaming-MapReduce-Auftragsobjekt zur Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="362cf-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="362cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="362cf-107">EXAMPLES</span></span>

### <span data-ttu-id="362cf-108">Beispiel 1: Erstellen einer Streaming-MapReduce-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="362cf-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="362cf-109">Dieser Befehl erstellt eine Streaming-MapReduce-Auftragsdefinition.</span><span class="sxs-lookup"><span data-stu-id="362cf-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="362cf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="362cf-110">PARAMETERS</span></span>

### <span data-ttu-id="362cf-111">-Argumente</span><span class="sxs-lookup"><span data-stu-id="362cf-111">-Arguments</span></span>
<span data-ttu-id="362cf-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="362cf-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="362cf-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="362cf-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="362cf-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="362cf-114">-CommandEnvironment</span></span>
<span data-ttu-id="362cf-115">Gibt ein Array mit Befehlszeilen Umgebungsvariablen an, die festgelegt werden sollen, wenn ein Auftrag auf Worker-Knoten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="362cf-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="362cf-116">– Definiert</span><span class="sxs-lookup"><span data-stu-id="362cf-116">-Defines</span></span>
<span data-ttu-id="362cf-117">Gibt Hadoop-Konfigurationswerte an, die für die Ausführung des Auftrags festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="362cf-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="362cf-118">-Datei</span><span class="sxs-lookup"><span data-stu-id="362cf-118">-File</span></span>
<span data-ttu-id="362cf-119">Gibt den Pfad zu einer Datei an, die eine auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="362cf-119">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="362cf-120">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="362cf-120">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="362cf-121">-Dateien</span><span class="sxs-lookup"><span data-stu-id="362cf-121">-Files</span></span>
<span data-ttu-id="362cf-122">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="362cf-122">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="362cf-123">-InputPath</span><span class="sxs-lookup"><span data-stu-id="362cf-123">-InputPath</span></span>
<span data-ttu-id="362cf-124">Gibt den Pfad zu den Eingabedateien an.</span><span class="sxs-lookup"><span data-stu-id="362cf-124">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="362cf-125">-Mapper</span><span class="sxs-lookup"><span data-stu-id="362cf-125">-Mapper</span></span>
<span data-ttu-id="362cf-126">Gibt einen Mapper-Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="362cf-126">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="362cf-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="362cf-127">-OutputPath</span></span>
<span data-ttu-id="362cf-128">Gibt den Pfad für die Auftragsausgabe an.</span><span class="sxs-lookup"><span data-stu-id="362cf-128">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="362cf-129">-Reduzierstück</span><span class="sxs-lookup"><span data-stu-id="362cf-129">-Reducer</span></span>
<span data-ttu-id="362cf-130">Gibt einen Reduzierer-Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="362cf-130">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="362cf-131">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="362cf-131">-StatusFolder</span></span>
<span data-ttu-id="362cf-132">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="362cf-132">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="362cf-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362cf-133">-DefaultProfile</span></span>
<span data-ttu-id="362cf-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="362cf-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="362cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362cf-135">CommonParameters</span></span>
<span data-ttu-id="362cf-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362cf-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="362cf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362cf-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="362cf-138">INPUTS</span></span>

## <span data-ttu-id="362cf-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="362cf-139">OUTPUTS</span></span>

### <span data-ttu-id="362cf-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="362cf-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="362cf-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="362cf-141">NOTES</span></span>

## <span data-ttu-id="362cf-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="362cf-142">RELATED LINKS</span></span>

[<span data-ttu-id="362cf-143">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="362cf-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


