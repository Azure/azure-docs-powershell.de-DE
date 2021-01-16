---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289715"
---
# <span data-ttu-id="bd99d-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="bd99d-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="bd99d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd99d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd99d-103">Erstellt ein Objekt für einen Strukturauftrag.</span><span class="sxs-lookup"><span data-stu-id="bd99d-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="bd99d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd99d-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd99d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd99d-105">DESCRIPTION</span></span>
<span data-ttu-id="bd99d-106">Das **Cmdlet "New-AzHDInsightHiveJobDefinition"** definiert ein Jobobjekt "Strukture" zur Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="bd99d-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="bd99d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd99d-107">EXAMPLES</span></span>

### <span data-ttu-id="bd99d-108">Beispiel 1: Erstellen einer Struktur</span><span class="sxs-lookup"><span data-stu-id="bd99d-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="bd99d-109">Mit diesem Befehl wird eine Strukturauftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="bd99d-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="bd99d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd99d-110">PARAMETERS</span></span>

### <span data-ttu-id="bd99d-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="bd99d-111">-Arguments</span></span>
<span data-ttu-id="bd99d-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="bd99d-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="bd99d-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="bd99d-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="bd99d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd99d-114">-DefaultProfile</span></span>
<span data-ttu-id="bd99d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bd99d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd99d-116">-Defines</span><span class="sxs-lookup"><span data-stu-id="bd99d-116">-Defines</span></span>
<span data-ttu-id="bd99d-117">Gibt die Werte der Hadoop-Konfiguration an, die festgelegt werden müssen, wenn der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd99d-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="bd99d-118">-File</span><span class="sxs-lookup"><span data-stu-id="bd99d-118">-File</span></span>
<span data-ttu-id="bd99d-119">Gibt den Pfad zu einer Datei an, die die zu ausführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="bd99d-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="bd99d-120">Die Datei muss für das Speicherkonto verfügbar sein, das dem Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bd99d-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="bd99d-121">Sie können diesen Parameter anstelle des *Abfrageparameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd99d-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="bd99d-122">-Files</span><span class="sxs-lookup"><span data-stu-id="bd99d-122">-Files</span></span>
<span data-ttu-id="bd99d-123">Gibt eine Sammlung von Dateien an, die einem Strukturauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bd99d-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="bd99d-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="bd99d-124">-JobName</span></span>
<span data-ttu-id="bd99d-125">Gibt den Namen des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="bd99d-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="bd99d-126">-Query</span><span class="sxs-lookup"><span data-stu-id="bd99d-126">-Query</span></span>
<span data-ttu-id="bd99d-127">Gibt die Strukturabfrage an.</span><span class="sxs-lookup"><span data-stu-id="bd99d-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="bd99d-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="bd99d-128">-RunAsFileJob</span></span>
<span data-ttu-id="bd99d-129">Gibt an, dass dieses Cmdlet eine Datei im Azure -Standardspeicherkonto erstellt, in dem eine Abfrage gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd99d-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="bd99d-130">Dieses Cmdlet übermittelt den Auftrag, der auf diese Datei verweist, als auszuführende Skript.</span><span class="sxs-lookup"><span data-stu-id="bd99d-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="bd99d-131">Sie können diese Funktion verwenden, um Sonderzeichen wie Prozentzeichen (%) zu behandeln. die bei einer Auftragsübermittlung über Templeton fehlschlagen würden, da Templeton eine Abfrage mit einem Prozentzeichen als einen URL-Parameter interpretiert.</span><span class="sxs-lookup"><span data-stu-id="bd99d-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="bd99d-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="bd99d-132">-StatusFolder</span></span>
<span data-ttu-id="bd99d-133">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="bd99d-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="bd99d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd99d-134">CommonParameters</span></span>
<span data-ttu-id="bd99d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd99d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd99d-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd99d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd99d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd99d-137">INPUTS</span></span>

### <span data-ttu-id="bd99d-138">Keine</span><span class="sxs-lookup"><span data-stu-id="bd99d-138">None</span></span>

## <span data-ttu-id="bd99d-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd99d-139">OUTPUTS</span></span>

### <span data-ttu-id="bd99d-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="bd99d-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="bd99d-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bd99d-141">NOTES</span></span>

## <span data-ttu-id="bd99d-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bd99d-142">RELATED LINKS</span></span>

[<span data-ttu-id="bd99d-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bd99d-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


