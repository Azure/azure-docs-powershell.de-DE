---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 127e949bfaa9d54644f7f690cfefbf095d477374
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504985"
---
# <span data-ttu-id="0728a-101">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="0728a-101">Invoke-AzureRmHDInsightHiveJob</span></span>

## <span data-ttu-id="0728a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0728a-102">SYNOPSIS</span></span>
<span data-ttu-id="0728a-103">Sendet eine Hive-Abfrage an einen HDInsight-Cluster und ruft Abfrageergebnisse in einem Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="0728a-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0728a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0728a-104">SYNTAX</span></span>

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0728a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0728a-105">DESCRIPTION</span></span>
<span data-ttu-id="0728a-106">Das Cmdlet **Invoke-AzureRmHDInsightHiveJob** sendet eine Hive-Abfrage an einen Azure HDInsight-Cluster und ruft Abfrageergebnisse in einem Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="0728a-106">The **Invoke-AzureRmHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="0728a-107">Verwenden Sie das Use-AzureRmHDInsightCluster-Cmdlet, bevor Sie **Invoke-AzureRmHDInsightHiveJob** aufrufen, um anzugeben, welcher Cluster für die Abfrage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0728a-107">Use the Use-AzureRmHDInsightCluster cmdlet before calling **Invoke-AzureRmHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="0728a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0728a-108">EXAMPLES</span></span>

### <span data-ttu-id="0728a-109">Beispiel 1: Übermitteln einer Hive-Abfrage an einen Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="0728a-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="0728a-110">Dieser Befehl übermittelt die Abfragetabellen an den Cluster mit dem Namen your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="0728a-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0728a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0728a-111">PARAMETERS</span></span>

### <span data-ttu-id="0728a-112">-Argumente</span><span class="sxs-lookup"><span data-stu-id="0728a-112">-Arguments</span></span>
<span data-ttu-id="0728a-113">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0728a-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="0728a-114">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="0728a-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="0728a-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="0728a-115">-DefaultContainer</span></span>
<span data-ttu-id="0728a-116">Gibt den Namen des Standardcontainers im standardmäßigen Azure Storage-Konto an, das ein HDInsight-Cluster verwendet.</span><span class="sxs-lookup"><span data-stu-id="0728a-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="0728a-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0728a-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="0728a-118">Gibt den Kontoschlüssel für das Standardspeicher Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0728a-118">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="0728a-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0728a-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="0728a-120">Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0728a-120">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="0728a-121">– Definiert</span><span class="sxs-lookup"><span data-stu-id="0728a-121">-Defines</span></span>
<span data-ttu-id="0728a-122">Gibt Hadoop-Konfigurationswerte an, die beim Ausführen eines Auftrags festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0728a-122">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="0728a-123">-Datei</span><span class="sxs-lookup"><span data-stu-id="0728a-123">-File</span></span>
<span data-ttu-id="0728a-124">Gibt den Pfad zu einer Datei im Azure-Speicher an, die die auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="0728a-124">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="0728a-125">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="0728a-125">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="0728a-126">-Dateien</span><span class="sxs-lookup"><span data-stu-id="0728a-126">-Files</span></span>
<span data-ttu-id="0728a-127">Gibt eine Sammlung von Dateien an, die für einen Hive-Auftrag erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0728a-127">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="0728a-128">-Jobname</span><span class="sxs-lookup"><span data-stu-id="0728a-128">-JobName</span></span>
<span data-ttu-id="0728a-129">Gibt den Namen eines Hive-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="0728a-129">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="0728a-130">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardwert: "Hive: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="0728a-130">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="0728a-131">-Query</span><span class="sxs-lookup"><span data-stu-id="0728a-131">-Query</span></span>
<span data-ttu-id="0728a-132">Gibt die Hive-Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="0728a-132">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="0728a-133">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="0728a-133">-RunAsFileJob</span></span>
<span data-ttu-id="0728a-134">Gibt an, dass dieses Cmdlet eine Datei im standardmäßigen Azure-Speicherkonto erstellt, in dem eine Abfrage gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0728a-134">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="0728a-135">Dieses Cmdlet übermittelt den Auftrag, der auf diese Datei verweist, als Skript, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0728a-135">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="0728a-136">Sie können diese Funktion zum Behandeln von Sonderzeichen wie Prozentzeichen (%) verwenden. Dies würde bei einer Auftragsübermittlung über Templeton fehlschlagen, da Templeton eine Abfrage mit einem Prozentzeichen als URL-Parameter interpretiert.</span><span class="sxs-lookup"><span data-stu-id="0728a-136">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="0728a-137">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="0728a-137">-StatusFolder</span></span>
<span data-ttu-id="0728a-138">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="0728a-138">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="0728a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0728a-139">-DefaultProfile</span></span>
<span data-ttu-id="0728a-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0728a-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0728a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0728a-141">CommonParameters</span></span>
<span data-ttu-id="0728a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0728a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0728a-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0728a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0728a-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0728a-144">INPUTS</span></span>

## <span data-ttu-id="0728a-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0728a-145">OUTPUTS</span></span>

### <span data-ttu-id="0728a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0728a-146">System.String</span></span>

## <span data-ttu-id="0728a-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="0728a-147">NOTES</span></span>

## <span data-ttu-id="0728a-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0728a-148">RELATED LINKS</span></span>

[<span data-ttu-id="0728a-149">Verwenden von-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0728a-149">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


