---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006216"
---
# <span data-ttu-id="8e461-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8e461-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="8e461-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e461-102">SYNOPSIS</span></span>
<span data-ttu-id="8e461-103">Definiert einen neuen Pig-Job für einen HDInsight-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8e461-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="8e461-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e461-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8e461-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e461-105">DESCRIPTION</span></span>
<span data-ttu-id="8e461-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="8e461-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8e461-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="8e461-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8e461-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8e461-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8e461-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="8e461-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8e461-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="8e461-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8e461-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8e461-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8e461-112">Der **New-AzureHDInsightPigJobDefinition** definiert einen Pig-Job für einen Azure HDInsight-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8e461-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="8e461-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e461-113">EXAMPLES</span></span>

### <span data-ttu-id="8e461-114">Beispiel 1: Definieren eines neuen Pig-Auftrags</span><span class="sxs-lookup"><span data-stu-id="8e461-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="8e461-115">Der erste Befehl deklariert einen Zeichenfolgenwert und speichert dann in der $0-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8e461-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="8e461-116">Der zweite Befehl erstellt eine Schweine Auftrags Abfrage und speichert Sie dann in der $QueryString Variablen.</span><span class="sxs-lookup"><span data-stu-id="8e461-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="8e461-117">Der endgültige Befehl erstellt eine Pig-Auftragsdefinition, die die Abfrage in $QueryString verwendet, und speichert dann die Auftragsdefinition in der $PigJobDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="8e461-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="8e461-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e461-118">PARAMETERS</span></span>

### <span data-ttu-id="8e461-119">-Argumente</span><span class="sxs-lookup"><span data-stu-id="8e461-119">-Arguments</span></span>
<span data-ttu-id="8e461-120">Gibt ein Array von Argumenten für einen Pig-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="8e461-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="8e461-121">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="8e461-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="8e461-122">-Datei</span><span class="sxs-lookup"><span data-stu-id="8e461-122">-File</span></span>
<span data-ttu-id="8e461-123">Gibt den Pfad zu einer Datei an, die eine auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="8e461-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="8e461-124">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e461-124">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e461-125">-Dateien</span><span class="sxs-lookup"><span data-stu-id="8e461-125">-Files</span></span>
<span data-ttu-id="8e461-126">Gibt eine Sammlung von Dateien an, die einem Pig-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8e461-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="8e461-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="8e461-127">-Profile</span></span>
<span data-ttu-id="8e461-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8e461-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8e461-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8e461-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8e461-130">-Query</span><span class="sxs-lookup"><span data-stu-id="8e461-130">-Query</span></span>
<span data-ttu-id="8e461-131">Gibt eine Schweine Auftrags Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="8e461-131">Specifies a Pig job query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e461-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="8e461-132">-StatusFolder</span></span>
<span data-ttu-id="8e461-133">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält, einschließlich des Exit-Codes und der Aufgaben Protokolle.</span><span class="sxs-lookup"><span data-stu-id="8e461-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="8e461-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e461-134">CommonParameters</span></span>
<span data-ttu-id="8e461-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e461-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e461-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e461-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e461-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e461-137">INPUTS</span></span>

## <span data-ttu-id="8e461-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e461-138">OUTPUTS</span></span>

## <span data-ttu-id="8e461-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e461-139">NOTES</span></span>

## <span data-ttu-id="8e461-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e461-140">RELATED LINKS</span></span>

[<span data-ttu-id="8e461-141">Neu – AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8e461-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="8e461-142">Neu – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8e461-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="8e461-143">Neu – AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8e461-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="8e461-144">Neu – AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8e461-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


