---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: abe1a0eaa03d498e151a58d5970f85be088e489e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934955"
---
# <span data-ttu-id="da663-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="da663-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="da663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da663-102">SYNOPSIS</span></span>
<span data-ttu-id="da663-103">Erstellt ein Schweinauftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="da663-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="da663-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da663-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da663-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da663-105">DESCRIPTION</span></span>
<span data-ttu-id="da663-106">Das **Cmdlet New-AzHDInsightPigJobDefinition** definiert ein Pig-Auftragsobjekt für die Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="da663-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="da663-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da663-107">EXAMPLES</span></span>

### <span data-ttu-id="da663-108">Beispiel 1: Erstellen einer Definition eines Schweinsauftrags</span><span class="sxs-lookup"><span data-stu-id="da663-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="da663-109">Mit diesem Befehl wird eine "Pig-Auftragsdefinition" erstellt.</span><span class="sxs-lookup"><span data-stu-id="da663-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="da663-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="da663-110">PARAMETERS</span></span>

### <span data-ttu-id="da663-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="da663-111">-Arguments</span></span>
<span data-ttu-id="da663-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="da663-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="da663-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="da663-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="da663-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da663-114">-DefaultProfile</span></span>
<span data-ttu-id="da663-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="da663-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da663-116">-Datei</span><span class="sxs-lookup"><span data-stu-id="da663-116">-File</span></span>
<span data-ttu-id="da663-117">Gibt den Pfad zu einer Datei an, die die abfrage enthält, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da663-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="da663-118">Die Datei muss für das dem Cluster zugeordnete Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="da663-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="da663-119">Sie können diesen Parameter anstelle des *Abfrageparameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="da663-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="da663-120">-Dateien</span><span class="sxs-lookup"><span data-stu-id="da663-120">-Files</span></span>
<span data-ttu-id="da663-121">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="da663-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="da663-122">-Query</span><span class="sxs-lookup"><span data-stu-id="da663-122">-Query</span></span>
<span data-ttu-id="da663-123">Gibt die Abfrage "Schwein" an.</span><span class="sxs-lookup"><span data-stu-id="da663-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="da663-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="da663-124">-StatusFolder</span></span>
<span data-ttu-id="da663-125">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="da663-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="da663-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da663-126">CommonParameters</span></span>
<span data-ttu-id="da663-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da663-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da663-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da663-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da663-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da663-129">INPUTS</span></span>

### <span data-ttu-id="da663-130">Keine</span><span class="sxs-lookup"><span data-stu-id="da663-130">None</span></span>

## <span data-ttu-id="da663-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da663-131">OUTPUTS</span></span>

### <span data-ttu-id="da663-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="da663-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="da663-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="da663-133">NOTES</span></span>

## <span data-ttu-id="da663-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="da663-134">RELATED LINKS</span></span>

[<span data-ttu-id="da663-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="da663-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


