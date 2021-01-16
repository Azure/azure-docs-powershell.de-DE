---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 45278426ee25337bd484a46b533c72f49dbe9586
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289708"
---
# <span data-ttu-id="fa213-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fa213-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="fa213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa213-102">SYNOPSIS</span></span>
<span data-ttu-id="fa213-103">Erstellt ein Auftragsobjekt von MapReduce.</span><span class="sxs-lookup"><span data-stu-id="fa213-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="fa213-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa213-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa213-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa213-105">DESCRIPTION</span></span>
<span data-ttu-id="fa213-106">Das **Cmdlet "New-AzHDInsightMapReduceJobDefinition"** definiert einen neuen Auftrag von MapReduce für die Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="fa213-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fa213-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa213-107">EXAMPLES</span></span>

### <span data-ttu-id="fa213-108">Beispiel 1: Erstellen einer Auftragsdefinition für MapReduce</span><span class="sxs-lookup"><span data-stu-id="fa213-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="fa213-109">Mit diesem Befehl wird eine Auftragsdefinition für MapReduce erstellt.</span><span class="sxs-lookup"><span data-stu-id="fa213-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="fa213-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa213-110">PARAMETERS</span></span>

### <span data-ttu-id="fa213-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="fa213-111">-Arguments</span></span>
<span data-ttu-id="fa213-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="fa213-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="fa213-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="fa213-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="fa213-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="fa213-114">-ClassName</span></span>
<span data-ttu-id="fa213-115">Gibt die Auftragsklasse in der JAR-Datei an.</span><span class="sxs-lookup"><span data-stu-id="fa213-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="fa213-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa213-116">-DefaultProfile</span></span>
<span data-ttu-id="fa213-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fa213-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa213-118">-Defines</span><span class="sxs-lookup"><span data-stu-id="fa213-118">-Defines</span></span>
<span data-ttu-id="fa213-119">Gibt die Werte der Hadoop-Konfiguration an, die festgelegt werden müssen, wenn der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa213-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="fa213-120">-Files</span><span class="sxs-lookup"><span data-stu-id="fa213-120">-Files</span></span>
<span data-ttu-id="fa213-121">Gibt eine Sammlung von Dateien an, die einem Strukturauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fa213-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="fa213-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="fa213-122">-JarFile</span></span>
<span data-ttu-id="fa213-123">Gibt die für den Auftrag zu verwendende JAR-Datei an.</span><span class="sxs-lookup"><span data-stu-id="fa213-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="fa213-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="fa213-124">-JobName</span></span>
<span data-ttu-id="fa213-125">Gibt den Namen des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="fa213-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="fa213-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="fa213-126">-LibJars</span></span>
<span data-ttu-id="fa213-127">Gibt die bibliotheks-JARS für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="fa213-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="fa213-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="fa213-128">-StatusFolder</span></span>
<span data-ttu-id="fa213-129">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="fa213-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="fa213-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa213-130">CommonParameters</span></span>
<span data-ttu-id="fa213-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa213-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa213-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa213-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa213-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa213-133">INPUTS</span></span>

### <span data-ttu-id="fa213-134">Keine</span><span class="sxs-lookup"><span data-stu-id="fa213-134">None</span></span>

## <span data-ttu-id="fa213-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa213-135">OUTPUTS</span></span>

### <span data-ttu-id="fa213-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fa213-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="fa213-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fa213-137">NOTES</span></span>

## <span data-ttu-id="fa213-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fa213-138">RELATED LINKS</span></span>

[<span data-ttu-id="fa213-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fa213-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


