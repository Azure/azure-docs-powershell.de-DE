---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: 3f40857c0388983a12217477db96cbbdbb94e815
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651048"
---
# <span data-ttu-id="c28e7-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c28e7-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="c28e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c28e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c28e7-103">Erstellt ein Pig-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c28e7-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="c28e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c28e7-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c28e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c28e7-105">DESCRIPTION</span></span>
<span data-ttu-id="c28e7-106">Das Cmdlet **New-AzHDInsightPigJobDefinition** definiert ein Pig-Auftragsobjekt zur Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="c28e7-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c28e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c28e7-107">EXAMPLES</span></span>

### <span data-ttu-id="c28e7-108">Beispiel 1: Erstellen einer Pig-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="c28e7-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="c28e7-109">Mit diesem Befehl wird eine Pig-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="c28e7-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="c28e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c28e7-110">PARAMETERS</span></span>

### <span data-ttu-id="c28e7-111">-Argumente</span><span class="sxs-lookup"><span data-stu-id="c28e7-111">-Arguments</span></span>
<span data-ttu-id="c28e7-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="c28e7-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="c28e7-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="c28e7-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="c28e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28e7-114">-DefaultProfile</span></span>
<span data-ttu-id="c28e7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c28e7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c28e7-116">-Datei</span><span class="sxs-lookup"><span data-stu-id="c28e7-116">-File</span></span>
<span data-ttu-id="c28e7-117">Gibt den Pfad zu einer Datei an, die die auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="c28e7-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="c28e7-118">Die Datei muss auf dem dem Cluster zugeordneten Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="c28e7-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="c28e7-119">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="c28e7-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="c28e7-120">-Dateien</span><span class="sxs-lookup"><span data-stu-id="c28e7-120">-Files</span></span>
<span data-ttu-id="c28e7-121">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c28e7-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="c28e7-122">-Query</span><span class="sxs-lookup"><span data-stu-id="c28e7-122">-Query</span></span>
<span data-ttu-id="c28e7-123">Gibt die Schweine Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="c28e7-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="c28e7-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="c28e7-124">-StatusFolder</span></span>
<span data-ttu-id="c28e7-125">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="c28e7-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="c28e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28e7-126">CommonParameters</span></span>
<span data-ttu-id="c28e7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28e7-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c28e7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28e7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c28e7-129">INPUTS</span></span>

### <span data-ttu-id="c28e7-130">Keine</span><span class="sxs-lookup"><span data-stu-id="c28e7-130">None</span></span>

## <span data-ttu-id="c28e7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c28e7-131">OUTPUTS</span></span>

### <span data-ttu-id="c28e7-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c28e7-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="c28e7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c28e7-133">NOTES</span></span>

## <span data-ttu-id="c28e7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c28e7-134">RELATED LINKS</span></span>

[<span data-ttu-id="c28e7-135">Anfang-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c28e7-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


