---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: d6ab15fffd71776188291c58f2e21bbee5f27423
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469663"
---
# <span data-ttu-id="576d9-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="576d9-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="576d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="576d9-102">SYNOPSIS</span></span>
<span data-ttu-id="576d9-103">Erstellt ein Auftragsobjekt von MapReduce.</span><span class="sxs-lookup"><span data-stu-id="576d9-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="576d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="576d9-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="576d9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="576d9-105">DESCRIPTION</span></span>
<span data-ttu-id="576d9-106">Das **Cmdlet "New-AzHDInsightMapReduceJobDefinition"** definiert einen neuen Auftrag von MapReduce für die Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="576d9-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="576d9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="576d9-107">EXAMPLES</span></span>

### <span data-ttu-id="576d9-108">Beispiel 1: Erstellen einer Auftragsdefinition für MapReduce</span><span class="sxs-lookup"><span data-stu-id="576d9-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="576d9-109">Mit diesem Befehl wird eine Auftragsdefinition für MapReduce erstellt.</span><span class="sxs-lookup"><span data-stu-id="576d9-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="576d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="576d9-110">PARAMETERS</span></span>

### <span data-ttu-id="576d9-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="576d9-111">-Arguments</span></span>
<span data-ttu-id="576d9-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="576d9-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="576d9-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="576d9-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="576d9-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="576d9-114">-ClassName</span></span>
<span data-ttu-id="576d9-115">Gibt die Auftragsklasse in der JAR-Datei an.</span><span class="sxs-lookup"><span data-stu-id="576d9-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="576d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576d9-116">-DefaultProfile</span></span>
<span data-ttu-id="576d9-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="576d9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="576d9-118">-Defines</span><span class="sxs-lookup"><span data-stu-id="576d9-118">-Defines</span></span>
<span data-ttu-id="576d9-119">Gibt die Werte der Hadoop-Konfiguration an, die festgelegt werden müssen, wenn der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="576d9-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="576d9-120">-Files</span><span class="sxs-lookup"><span data-stu-id="576d9-120">-Files</span></span>
<span data-ttu-id="576d9-121">Gibt eine Sammlung von Dateien an, die einem Strukturauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="576d9-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="576d9-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="576d9-122">-JarFile</span></span>
<span data-ttu-id="576d9-123">Gibt die für den Auftrag zu verwendende JAR-Datei an.</span><span class="sxs-lookup"><span data-stu-id="576d9-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="576d9-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="576d9-124">-JobName</span></span>
<span data-ttu-id="576d9-125">Gibt den Namen des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="576d9-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="576d9-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="576d9-126">-LibJars</span></span>
<span data-ttu-id="576d9-127">Gibt die bibliotheks-JARS für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="576d9-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="576d9-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="576d9-128">-StatusFolder</span></span>
<span data-ttu-id="576d9-129">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="576d9-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="576d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576d9-130">CommonParameters</span></span>
<span data-ttu-id="576d9-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576d9-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="576d9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576d9-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="576d9-133">INPUTS</span></span>

### <span data-ttu-id="576d9-134">Keine</span><span class="sxs-lookup"><span data-stu-id="576d9-134">None</span></span>

## <span data-ttu-id="576d9-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="576d9-135">OUTPUTS</span></span>

### <span data-ttu-id="576d9-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="576d9-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="576d9-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="576d9-137">NOTES</span></span>

## <span data-ttu-id="576d9-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="576d9-138">RELATED LINKS</span></span>

[<span data-ttu-id="576d9-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="576d9-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


