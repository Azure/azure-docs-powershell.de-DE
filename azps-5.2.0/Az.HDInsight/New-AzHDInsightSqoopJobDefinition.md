---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 2cc5acb2017a9db2bf5ed1f80ccfd1069bc1a465
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289697"
---
# <span data-ttu-id="6ac06-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6ac06-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="6ac06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ac06-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac06-103">Erstellt ein Sqoop-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="6ac06-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="6ac06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ac06-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ac06-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ac06-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac06-106">Das **Cmdlet "New-AzHDInsightSqoopJobDefinition"** definiert ein Sqoop-Auftragsobjekt für die Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="6ac06-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6ac06-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ac06-107">EXAMPLES</span></span>

### <span data-ttu-id="6ac06-108">Beispiel 1: Erstellen einer Definition eines Sqoop-Auftrags</span><span class="sxs-lookup"><span data-stu-id="6ac06-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="6ac06-109">Dieser Befehl erstellt eine Sqoop-Auftragsdefinition.</span><span class="sxs-lookup"><span data-stu-id="6ac06-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="6ac06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ac06-110">PARAMETERS</span></span>

### <span data-ttu-id="6ac06-111">-Command</span><span class="sxs-lookup"><span data-stu-id="6ac06-111">-Command</span></span>
<span data-ttu-id="6ac06-112">Gibt den Befehl "Sqoop" an.</span><span class="sxs-lookup"><span data-stu-id="6ac06-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="6ac06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac06-113">-DefaultProfile</span></span>
<span data-ttu-id="6ac06-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6ac06-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ac06-115">-File</span><span class="sxs-lookup"><span data-stu-id="6ac06-115">-File</span></span>
<span data-ttu-id="6ac06-116">Gibt den Pfad zu einer Datei an, die die zu ausführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="6ac06-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="6ac06-117">Die Datei muss für das Speicherkonto verfügbar sein, das dem Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6ac06-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="6ac06-118">Sie können diesen Parameter anstelle des *Abfrageparameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ac06-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="6ac06-119">-Files</span><span class="sxs-lookup"><span data-stu-id="6ac06-119">-Files</span></span>
<span data-ttu-id="6ac06-120">Gibt eine Sammlung von Dateien an, die einem Strukturauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6ac06-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="6ac06-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="6ac06-121">-LibDir</span></span>
<span data-ttu-id="6ac06-122">Gibt das Bibliotheksverzeichnis für den Sqoop-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="6ac06-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="6ac06-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="6ac06-123">-StatusFolder</span></span>
<span data-ttu-id="6ac06-124">Gibt den Speicherort des Ordners an, der Standardausgabe- und Fehlerausgabe für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="6ac06-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="6ac06-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac06-125">CommonParameters</span></span>
<span data-ttu-id="6ac06-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ac06-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac06-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac06-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac06-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ac06-128">INPUTS</span></span>

### <span data-ttu-id="6ac06-129">Keine</span><span class="sxs-lookup"><span data-stu-id="6ac06-129">None</span></span>

## <span data-ttu-id="6ac06-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ac06-130">OUTPUTS</span></span>

### <span data-ttu-id="6ac06-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6ac06-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="6ac06-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6ac06-132">NOTES</span></span>

## <span data-ttu-id="6ac06-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6ac06-133">RELATED LINKS</span></span>

[<span data-ttu-id="6ac06-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6ac06-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


