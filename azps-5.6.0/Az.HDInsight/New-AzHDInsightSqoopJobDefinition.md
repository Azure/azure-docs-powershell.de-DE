---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 3217673c01e4d77fe2643765df55ff58747b3133
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928600"
---
# <span data-ttu-id="79f48-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="79f48-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="79f48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79f48-102">SYNOPSIS</span></span>
<span data-ttu-id="79f48-103">Erstellt ein Sqoop-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="79f48-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="79f48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79f48-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79f48-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79f48-105">DESCRIPTION</span></span>
<span data-ttu-id="79f48-106">Das **Cmdlet New-AzHDInsightSqoopJobDefinition** definiert ein Sqoop-Auftragsobjekt für die Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="79f48-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="79f48-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79f48-107">EXAMPLES</span></span>

### <span data-ttu-id="79f48-108">Beispiel 1: Erstellen einer Sqoop-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="79f48-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="79f48-109">Mit diesem Befehl wird eine Sqoop-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="79f48-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="79f48-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79f48-110">PARAMETERS</span></span>

### <span data-ttu-id="79f48-111">-Befehl</span><span class="sxs-lookup"><span data-stu-id="79f48-111">-Command</span></span>
<span data-ttu-id="79f48-112">Gibt den Befehl Sqoop an.</span><span class="sxs-lookup"><span data-stu-id="79f48-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="79f48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f48-113">-DefaultProfile</span></span>
<span data-ttu-id="79f48-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="79f48-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79f48-115">-Datei</span><span class="sxs-lookup"><span data-stu-id="79f48-115">-File</span></span>
<span data-ttu-id="79f48-116">Gibt den Pfad zu einer Datei an, die die abfrage enthält, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="79f48-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="79f48-117">Die Datei muss für das dem Cluster zugeordnete Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="79f48-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="79f48-118">Sie können diesen Parameter anstelle des *Abfrageparameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="79f48-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="79f48-119">-Dateien</span><span class="sxs-lookup"><span data-stu-id="79f48-119">-Files</span></span>
<span data-ttu-id="79f48-120">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="79f48-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="79f48-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="79f48-121">-LibDir</span></span>
<span data-ttu-id="79f48-122">Gibt das Bibliotheksverzeichnis für den Sqoop-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="79f48-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="79f48-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="79f48-123">-StatusFolder</span></span>
<span data-ttu-id="79f48-124">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="79f48-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="79f48-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f48-125">CommonParameters</span></span>
<span data-ttu-id="79f48-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f48-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f48-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79f48-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f48-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79f48-128">INPUTS</span></span>

### <span data-ttu-id="79f48-129">Keine</span><span class="sxs-lookup"><span data-stu-id="79f48-129">None</span></span>

## <span data-ttu-id="79f48-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79f48-130">OUTPUTS</span></span>

### <span data-ttu-id="79f48-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="79f48-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="79f48-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79f48-132">NOTES</span></span>

## <span data-ttu-id="79f48-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79f48-133">RELATED LINKS</span></span>

[<span data-ttu-id="79f48-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="79f48-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


