---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: c1dab20f44edfd4e3714e4465a0bf295e8e78fb5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651049"
---
# <span data-ttu-id="e83bb-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e83bb-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="e83bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e83bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e83bb-103">Erstellt ein MapReduce-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e83bb-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="e83bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e83bb-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e83bb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e83bb-105">DESCRIPTION</span></span>
<span data-ttu-id="e83bb-106">Das Cmdlet **New-AzHDInsightMapReduceJobDefinition** definiert einen neuen MapReduce-Auftrag für die Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e83bb-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e83bb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e83bb-107">EXAMPLES</span></span>

### <span data-ttu-id="e83bb-108">Beispiel 1: Erstellen einer MapReduce-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="e83bb-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="e83bb-109">Mit diesem Befehl wird eine MapReduce-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="e83bb-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="e83bb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e83bb-110">PARAMETERS</span></span>

### <span data-ttu-id="e83bb-111">-Argumente</span><span class="sxs-lookup"><span data-stu-id="e83bb-111">-Arguments</span></span>
<span data-ttu-id="e83bb-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="e83bb-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="e83bb-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="e83bb-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="e83bb-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="e83bb-114">-ClassName</span></span>
<span data-ttu-id="e83bb-115">Gibt die Auftragsklasse in der JAR-Datei an.</span><span class="sxs-lookup"><span data-stu-id="e83bb-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="e83bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e83bb-116">-DefaultProfile</span></span>
<span data-ttu-id="e83bb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e83bb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e83bb-118">– Definiert</span><span class="sxs-lookup"><span data-stu-id="e83bb-118">-Defines</span></span>
<span data-ttu-id="e83bb-119">Gibt Hadoop-Konfigurationswerte an, die für die Ausführung des Auftrags festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e83bb-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="e83bb-120">-Dateien</span><span class="sxs-lookup"><span data-stu-id="e83bb-120">-Files</span></span>
<span data-ttu-id="e83bb-121">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e83bb-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="e83bb-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="e83bb-122">-JarFile</span></span>
<span data-ttu-id="e83bb-123">Gibt die JAR-Datei an, die für den Auftrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e83bb-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="e83bb-124">-Jobname</span><span class="sxs-lookup"><span data-stu-id="e83bb-124">-JobName</span></span>
<span data-ttu-id="e83bb-125">Gibt den Namen des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="e83bb-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="e83bb-126">-Libjar</span><span class="sxs-lookup"><span data-stu-id="e83bb-126">-LibJars</span></span>
<span data-ttu-id="e83bb-127">Gibt die lib-Tiegel für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="e83bb-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="e83bb-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="e83bb-128">-StatusFolder</span></span>
<span data-ttu-id="e83bb-129">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="e83bb-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="e83bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83bb-130">CommonParameters</span></span>
<span data-ttu-id="e83bb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e83bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83bb-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e83bb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83bb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e83bb-133">INPUTS</span></span>

### <span data-ttu-id="e83bb-134">Keine</span><span class="sxs-lookup"><span data-stu-id="e83bb-134">None</span></span>

## <span data-ttu-id="e83bb-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e83bb-135">OUTPUTS</span></span>

### <span data-ttu-id="e83bb-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e83bb-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="e83bb-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e83bb-137">NOTES</span></span>

## <span data-ttu-id="e83bb-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e83bb-138">RELATED LINKS</span></span>

[<span data-ttu-id="e83bb-139">Anfang-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e83bb-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


