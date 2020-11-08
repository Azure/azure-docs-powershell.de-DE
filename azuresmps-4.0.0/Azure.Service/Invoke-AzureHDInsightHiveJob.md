---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006454"
---
# <span data-ttu-id="9104d-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="9104d-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="9104d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9104d-102">SYNOPSIS</span></span>
<span data-ttu-id="9104d-103">Sendet Hive-Abfragen an einen HDInsight-Cluster, zeigt den Fortschritt der Abfrageausführung an und ruft Abfrageergebnisse in einem Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="9104d-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="9104d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9104d-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9104d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9104d-105">DESCRIPTION</span></span>
<span data-ttu-id="9104d-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="9104d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="9104d-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="9104d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="9104d-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9104d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="9104d-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="9104d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="9104d-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="9104d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="9104d-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9104d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="9104d-112">Das Cmdlet **Invoke-AzureHDInsightHiveJob** sendet Hive-Abfragen an einen HDInsight-Cluster, zeigt den Fortschritt der Abfrageausführung an und ruft die Abfrageergebnisse in einem Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="9104d-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="9104d-113">Sie müssen das Use-AzureHDInsightCluster-Cmdlet ausführen, bevor Sie **Invoke-AzureHDInsightHiveJob** ausführen, um den HDInsight-Cluster anzugeben, für den eine Abfrage gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9104d-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="9104d-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9104d-114">EXAMPLES</span></span>

### <span data-ttu-id="9104d-115">Beispiel 1: Übermitteln einer Hive-Abfrage</span><span class="sxs-lookup"><span data-stu-id="9104d-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="9104d-116">Der erste Befehl verwendet das Cmdlet **use-AzureHDInsightCluster** , um einen Cluster im aktuellen Abonnement anzugeben, der für eine Hive-Abfrage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9104d-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="9104d-117">Der zweite Befehl verwendet das **Invoke-AzureHDInsightHiveJob-** Cmdlet, um die Hive-Abfrage zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="9104d-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="9104d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="9104d-118">PARAMETERS</span></span>

### <span data-ttu-id="9104d-119">-Argumente</span><span class="sxs-lookup"><span data-stu-id="9104d-119">-Arguments</span></span>
<span data-ttu-id="9104d-120">Gibt ein Array von Argumenten für einen Hadoop-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="9104d-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="9104d-121">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="9104d-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="9104d-122">– Definiert</span><span class="sxs-lookup"><span data-stu-id="9104d-122">-Defines</span></span>
<span data-ttu-id="9104d-123">Gibt Hadoop-Konfigurationswerte an, die beim Ausführen eines Auftrags festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9104d-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="9104d-124">-Datei</span><span class="sxs-lookup"><span data-stu-id="9104d-124">-File</span></span>
<span data-ttu-id="9104d-125">Gibt den Windows Azure Storage BLOB (WASB)-Pfad zu einer Datei im Azure BLOB-Speicher an, die die auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="9104d-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="9104d-126">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="9104d-126">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="9104d-127">-Dateien</span><span class="sxs-lookup"><span data-stu-id="9104d-127">-Files</span></span>
<span data-ttu-id="9104d-128">Gibt eine Sammlung von Dateien an, die für einen Hive-Auftrag erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9104d-128">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="9104d-129">-Jobname</span><span class="sxs-lookup"><span data-stu-id="9104d-129">-JobName</span></span>
<span data-ttu-id="9104d-130">Gibt den Namen eines Hive-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="9104d-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="9104d-131">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardwert: "Hive: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="9104d-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="9104d-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="9104d-132">-Profile</span></span>
<span data-ttu-id="9104d-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9104d-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9104d-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9104d-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9104d-135">-Query</span><span class="sxs-lookup"><span data-stu-id="9104d-135">-Query</span></span>
<span data-ttu-id="9104d-136">Gibt eine Hive-Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="9104d-136">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="9104d-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="9104d-137">-RunAsFileJob</span></span>
<span data-ttu-id="9104d-138">Gibt an, dass dieses Cmdlet eine Datei im standardmäßigen Azure-Speicherkonto erstellt, in dem eine Abfrage gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9104d-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="9104d-139">Dieses Cmdlet übermittelt den Auftrag, der auf diese Datei verweist, als Skript, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9104d-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="9104d-140">Sie können diese Funktion zum Behandeln von Sonderzeichen wie Prozentzeichen (%) verwenden. Dies würde bei einer Auftragsübermittlung über Templeton fehlschlagen, da Templeton eine Abfrage mit einem Prozentzeichen als URL-Parameter interpretiert.</span><span class="sxs-lookup"><span data-stu-id="9104d-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="9104d-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="9104d-141">-StatusFolder</span></span>
<span data-ttu-id="9104d-142">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält, einschließlich des Exit-Codes und der Aufgaben Protokolle.</span><span class="sxs-lookup"><span data-stu-id="9104d-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="9104d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9104d-143">CommonParameters</span></span>
<span data-ttu-id="9104d-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9104d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9104d-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9104d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9104d-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9104d-146">INPUTS</span></span>

## <span data-ttu-id="9104d-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9104d-147">OUTPUTS</span></span>

## <span data-ttu-id="9104d-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="9104d-148">NOTES</span></span>

## <span data-ttu-id="9104d-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9104d-149">RELATED LINKS</span></span>

[<span data-ttu-id="9104d-150">Neu – AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9104d-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="9104d-151">Verwenden von-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9104d-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


