---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006123"
---
# <span data-ttu-id="a0fd2-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a0fd2-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="a0fd2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fd2-103">Definiert einen neuen Hive-Auftrag für einen HDInsight-Dienst.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="a0fd2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0fd2-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a0fd2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="a0fd2-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="a0fd2-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="a0fd2-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="a0fd2-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="a0fd2-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="a0fd2-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="a0fd2-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="a0fd2-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a0fd2-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="a0fd2-112">Das Cmdlet **New-AzureHDInsightHiveJobDefinition** definiert einen Hive-Auftrag für einen Azure HDInsight-Dienst.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="a0fd2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0fd2-113">EXAMPLES</span></span>

### <span data-ttu-id="a0fd2-114">Beispiel 1: Erstellen einer Hive-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="a0fd2-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="a0fd2-115">Mit diesem Befehl wird eine Hive-Auftragsdefinition erstellt, die eine vordefinierte Abfragezeichenfolge verwendet und diese dann in der $HiveJobDefinition-Variablen speichert.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="a0fd2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0fd2-116">PARAMETERS</span></span>

### <span data-ttu-id="a0fd2-117">-Argumente</span><span class="sxs-lookup"><span data-stu-id="a0fd2-117">-Arguments</span></span>
<span data-ttu-id="a0fd2-118">Gibt ein Array von Argumenten für einen Hadoop-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="a0fd2-119">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="a0fd2-120">– Definiert</span><span class="sxs-lookup"><span data-stu-id="a0fd2-120">-Defines</span></span>
<span data-ttu-id="a0fd2-121">Gibt Hadoop-Konfigurationswerte an, die beim Ausführen eines Auftrags festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fd2-122">-Datei</span><span class="sxs-lookup"><span data-stu-id="a0fd2-122">-File</span></span>
<span data-ttu-id="a0fd2-123">Gibt den Pfad zu einer Datei an, die eine auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="a0fd2-124">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="a0fd2-125">-Dateien</span><span class="sxs-lookup"><span data-stu-id="a0fd2-125">-Files</span></span>
<span data-ttu-id="a0fd2-126">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="a0fd2-127">-Jobname</span><span class="sxs-lookup"><span data-stu-id="a0fd2-127">-JobName</span></span>
<span data-ttu-id="a0fd2-128">Gibt den Namen des zu definierenden Hive-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="a0fd2-129">Wenn Sie diesen Parameter nicht angeben, wird der Standardname verwendet: "Hive: \<first 100 characters of query\> ".</span><span class="sxs-lookup"><span data-stu-id="a0fd2-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fd2-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="a0fd2-130">-Profile</span></span>
<span data-ttu-id="a0fd2-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a0fd2-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a0fd2-133">-Query</span><span class="sxs-lookup"><span data-stu-id="a0fd2-133">-Query</span></span>
<span data-ttu-id="a0fd2-134">Gibt eine Hive-Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-134">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="a0fd2-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="a0fd2-135">-RunAsFileJob</span></span>
<span data-ttu-id="a0fd2-136">Gibt an, dass dieses Cmdlet eine Datei im standardmäßigen Azure-Speicherkonto erstellt, in dem eine Abfrage gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="a0fd2-137">Dieses Cmdlet übermittelt den Auftrag, der auf diese Datei verweist, als Skript, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="a0fd2-138">Sie können diese Funktion zum Behandeln von Sonderzeichen wie Prozentzeichen (%) verwenden. Dies würde bei einer Auftragsübermittlung über Templeton fehlschlagen, da Templeton eine Abfrage mit einem Prozentzeichen als URL-Parameter interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="a0fd2-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="a0fd2-139">-StatusFolder</span></span>
<span data-ttu-id="a0fd2-140">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält, einschließlich des Exit-Codes und der Aufgaben Protokolle.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="a0fd2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fd2-141">CommonParameters</span></span>
<span data-ttu-id="a0fd2-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0fd2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fd2-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0fd2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fd2-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0fd2-144">INPUTS</span></span>

## <span data-ttu-id="a0fd2-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0fd2-145">OUTPUTS</span></span>

## <span data-ttu-id="a0fd2-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0fd2-146">NOTES</span></span>

## <span data-ttu-id="a0fd2-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0fd2-147">RELATED LINKS</span></span>

[<span data-ttu-id="a0fd2-148">Neu – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a0fd2-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="a0fd2-149">Neu – AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a0fd2-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="a0fd2-150">Neu – AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a0fd2-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="a0fd2-151">Neu – AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a0fd2-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


