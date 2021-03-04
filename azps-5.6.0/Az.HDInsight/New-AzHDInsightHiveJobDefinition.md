---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: be8878d338206e1355dc36082d4f9941cf141838
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947115"
---
# <span data-ttu-id="f50a2-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f50a2-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="f50a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f50a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f50a2-103">Erstellt ein Hive-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f50a2-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="f50a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f50a2-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f50a2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f50a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f50a2-106">Das **Cmdlet New-AzHDInsightHiveJobDefinition** definiert ein Hive-Auftragsobjekt für die Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f50a2-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f50a2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f50a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f50a2-108">Beispiel 1: Erstellen einer Hive-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="f50a2-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f50a2-109">Mit diesem Befehl wird eine Hive-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="f50a2-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="f50a2-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f50a2-110">PARAMETERS</span></span>

### <span data-ttu-id="f50a2-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="f50a2-111">-Arguments</span></span>
<span data-ttu-id="f50a2-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="f50a2-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="f50a2-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="f50a2-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="f50a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f50a2-114">-DefaultProfile</span></span>
<span data-ttu-id="f50a2-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f50a2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f50a2-116">-Defines</span><span class="sxs-lookup"><span data-stu-id="f50a2-116">-Defines</span></span>
<span data-ttu-id="f50a2-117">Gibt Hadoop-Konfigurationswerte an, die festgelegt werden müssen, wenn der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f50a2-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="f50a2-118">-Datei</span><span class="sxs-lookup"><span data-stu-id="f50a2-118">-File</span></span>
<span data-ttu-id="f50a2-119">Gibt den Pfad zu einer Datei an, die die abfrage enthält, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f50a2-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="f50a2-120">Die Datei muss für das dem Cluster zugeordnete Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f50a2-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="f50a2-121">Sie können diesen Parameter anstelle des *Abfrageparameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="f50a2-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="f50a2-122">-Dateien</span><span class="sxs-lookup"><span data-stu-id="f50a2-122">-Files</span></span>
<span data-ttu-id="f50a2-123">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f50a2-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="f50a2-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="f50a2-124">-JobName</span></span>
<span data-ttu-id="f50a2-125">Gibt den Namen des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="f50a2-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="f50a2-126">-Query</span><span class="sxs-lookup"><span data-stu-id="f50a2-126">-Query</span></span>
<span data-ttu-id="f50a2-127">Gibt die Hive-Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="f50a2-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="f50a2-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="f50a2-128">-RunAsFileJob</span></span>
<span data-ttu-id="f50a2-129">Gibt an, dass mit diesem Cmdlet eine Datei im Azure-Standardspeicherkonto erstellt wird, in dem eine Abfrage gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f50a2-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="f50a2-130">Dieses Cmdlet übermittelt den Auftrag, der auf diese Datei als Skript verweist, um ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="f50a2-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="f50a2-131">Sie können diese Funktion verwenden, um Sonderzeichen wie Prozentzeichen (%) zu behandeln. Dies würde bei einer Auftragsübermittlung über Templeton fehlschlagen, da Templeton eine Abfrage mit einem Prozentzeichen als URL-Parameter interpretiert.</span><span class="sxs-lookup"><span data-stu-id="f50a2-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="f50a2-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f50a2-132">-StatusFolder</span></span>
<span data-ttu-id="f50a2-133">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="f50a2-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="f50a2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f50a2-134">CommonParameters</span></span>
<span data-ttu-id="f50a2-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f50a2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f50a2-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f50a2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f50a2-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f50a2-137">INPUTS</span></span>

### <span data-ttu-id="f50a2-138">Keine</span><span class="sxs-lookup"><span data-stu-id="f50a2-138">None</span></span>

## <span data-ttu-id="f50a2-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f50a2-139">OUTPUTS</span></span>

### <span data-ttu-id="f50a2-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f50a2-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="f50a2-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f50a2-141">NOTES</span></span>

## <span data-ttu-id="f50a2-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f50a2-142">RELATED LINKS</span></span>

[<span data-ttu-id="f50a2-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f50a2-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


