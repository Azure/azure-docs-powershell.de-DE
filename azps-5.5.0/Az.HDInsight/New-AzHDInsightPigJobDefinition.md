---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: 4a21a8fdacdb53df7e513744cae31da4a7a61ca7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173252"
---
# <span data-ttu-id="0fbf5-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0fbf5-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="0fbf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fbf5-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbf5-103">Erstellt ein Objekt für einen Schweinauftrag.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="0fbf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fbf5-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fbf5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fbf5-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbf5-106">Das **Cmdlet "New-AzHDInsightPigJobDefinition"** definiert ein Jobobjekt für ein Schwein zur Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0fbf5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0fbf5-107">EXAMPLES</span></span>

### <span data-ttu-id="0fbf5-108">Beispiel 1: Erstellen einer Jobdefinition für ein Schwein</span><span class="sxs-lookup"><span data-stu-id="0fbf5-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="0fbf5-109">Mit diesem Befehl wird eine Jobdefinition für ein Schwein erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="0fbf5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fbf5-110">PARAMETERS</span></span>

### <span data-ttu-id="0fbf5-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="0fbf5-111">-Arguments</span></span>
<span data-ttu-id="0fbf5-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="0fbf5-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="0fbf5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbf5-114">-DefaultProfile</span></span>
<span data-ttu-id="0fbf5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0fbf5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fbf5-116">-File</span><span class="sxs-lookup"><span data-stu-id="0fbf5-116">-File</span></span>
<span data-ttu-id="0fbf5-117">Gibt den Pfad zu einer Datei an, die die zu ausführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="0fbf5-118">Die Datei muss für das Speicherkonto verfügbar sein, das dem Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="0fbf5-119">Sie können diesen Parameter anstelle des *Abfrageparameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="0fbf5-120">-Files</span><span class="sxs-lookup"><span data-stu-id="0fbf5-120">-Files</span></span>
<span data-ttu-id="0fbf5-121">Gibt eine Sammlung von Dateien an, die einem Strukturauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="0fbf5-122">-Query</span><span class="sxs-lookup"><span data-stu-id="0fbf5-122">-Query</span></span>
<span data-ttu-id="0fbf5-123">Gibt die Abfrage "Schwein" an.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="0fbf5-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="0fbf5-124">-StatusFolder</span></span>
<span data-ttu-id="0fbf5-125">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="0fbf5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbf5-126">CommonParameters</span></span>
<span data-ttu-id="0fbf5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbf5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbf5-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fbf5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbf5-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0fbf5-129">INPUTS</span></span>

### <span data-ttu-id="0fbf5-130">Keine</span><span class="sxs-lookup"><span data-stu-id="0fbf5-130">None</span></span>

## <span data-ttu-id="0fbf5-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0fbf5-131">OUTPUTS</span></span>

### <span data-ttu-id="0fbf5-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0fbf5-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="0fbf5-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0fbf5-133">NOTES</span></span>

## <span data-ttu-id="0fbf5-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0fbf5-134">RELATED LINKS</span></span>

[<span data-ttu-id="0fbf5-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0fbf5-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


