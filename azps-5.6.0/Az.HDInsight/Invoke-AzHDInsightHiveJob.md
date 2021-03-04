---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 2846848394cf6f376bd6b4064e193640806f81b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922435"
---
# <span data-ttu-id="c2bf4-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="c2bf4-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="c2bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="c2bf4-103">Sendet eine Hive-Abfrage an einen HDInsight-Cluster und ruft Abfrageergebnisse in einem Einzigen Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="c2bf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2bf4-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2bf4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="c2bf4-106">Das **Cmdlet Invoke-AzHDInsightHiveJob** sendet eine Hive-Abfrage an einen Azure HDInsight-Cluster und ruft Abfrageergebnisse in einem Einzigen Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="c2bf4-107">Verwenden Sie Use-AzHDInsightCluster-Cmdlet, bevor **Sie Invoke-AzHDInsightHiveJob aufrufen,** um anzugeben, welcher Cluster für die Abfrage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="c2bf4-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2bf4-108">EXAMPLES</span></span>

### <span data-ttu-id="c2bf4-109">Beispiel 1: Übermitteln einer Hive-Abfrage an einen Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="c2bf4-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="c2bf4-110">Mit diesem Befehl wird die Abfrage TABELLEN ANZEIGEN an den Cluster mit dem Namen your-hadoop-001 übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c2bf4-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c2bf4-111">PARAMETERS</span></span>

### <span data-ttu-id="c2bf4-112">-Arguments</span><span class="sxs-lookup"><span data-stu-id="c2bf4-112">-Arguments</span></span>
<span data-ttu-id="c2bf4-113">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="c2bf4-114">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="c2bf4-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="c2bf4-115">-DefaultContainer</span></span>
<span data-ttu-id="c2bf4-116">Gibt den Namen des Standardcontainers im Standardmäßigen Azure Storage-Konto an, das von einem HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="c2bf4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2bf4-117">-DefaultProfile</span></span>
<span data-ttu-id="c2bf4-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c2bf4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2bf4-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c2bf4-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="c2bf4-120">Gibt den Kontoschlüssel für das Standardspeicherkonto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="c2bf4-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2bf4-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="c2bf4-122">Gibt den Namen des Standardspeicherkontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="c2bf4-123">-Defines</span><span class="sxs-lookup"><span data-stu-id="c2bf4-123">-Defines</span></span>
<span data-ttu-id="c2bf4-124">Gibt Hadoop-Konfigurationswerte an, die festgelegt werden müssen, wenn ein Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="c2bf4-125">-Datei</span><span class="sxs-lookup"><span data-stu-id="c2bf4-125">-File</span></span>
<span data-ttu-id="c2bf4-126">Gibt den Pfad zu einer Datei in Azure Storage an, die die zu ausführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="c2bf4-127">Sie können diesen Parameter anstelle des *Abfrageparameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="c2bf4-128">-Dateien</span><span class="sxs-lookup"><span data-stu-id="c2bf4-128">-Files</span></span>
<span data-ttu-id="c2bf4-129">Gibt eine Sammlung von Dateien an, die für einen Hive-Auftrag erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-129">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="c2bf4-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="c2bf4-130">-JobName</span></span>
<span data-ttu-id="c2bf4-131">Gibt den Namen eines Hive-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="c2bf4-132">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardwert: "Hive: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="c2bf4-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="c2bf4-133">-Query</span><span class="sxs-lookup"><span data-stu-id="c2bf4-133">-Query</span></span>
<span data-ttu-id="c2bf4-134">Gibt die Hive-Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="c2bf4-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="c2bf4-135">-RunAsFileJob</span></span>
<span data-ttu-id="c2bf4-136">Gibt an, dass mit diesem Cmdlet eine Datei im Azure-Standardspeicherkonto erstellt wird, in dem eine Abfrage gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="c2bf4-137">Dieses Cmdlet übermittelt den Auftrag, der auf diese Datei als Skript verweist, um ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="c2bf4-138">Sie können diese Funktion verwenden, um Sonderzeichen wie Prozentzeichen (%) zu behandeln. Dies würde bei einer Auftragsübermittlung über Templeton fehlschlagen, da Templeton eine Abfrage mit einem Prozentzeichen als URL-Parameter interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="c2bf4-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="c2bf4-139">-StatusFolder</span></span>
<span data-ttu-id="c2bf4-140">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="c2bf4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2bf4-141">CommonParameters</span></span>
<span data-ttu-id="c2bf4-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2bf4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2bf4-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2bf4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2bf4-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2bf4-144">INPUTS</span></span>

### <span data-ttu-id="c2bf4-145">Keine</span><span class="sxs-lookup"><span data-stu-id="c2bf4-145">None</span></span>

## <span data-ttu-id="c2bf4-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2bf4-146">OUTPUTS</span></span>

### <span data-ttu-id="c2bf4-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c2bf4-147">System.String</span></span>

## <span data-ttu-id="c2bf4-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c2bf4-148">NOTES</span></span>

## <span data-ttu-id="c2bf4-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c2bf4-149">RELATED LINKS</span></span>

[<span data-ttu-id="c2bf4-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c2bf4-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


