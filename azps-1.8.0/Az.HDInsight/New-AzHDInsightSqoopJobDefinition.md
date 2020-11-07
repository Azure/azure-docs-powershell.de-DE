---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: d5841a7c612bccb760a8d755fc9a1c1364cc52a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819899"
---
# <span data-ttu-id="150e5-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="150e5-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="150e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="150e5-102">SYNOPSIS</span></span>
<span data-ttu-id="150e5-103">Erstellt ein Sqoop-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="150e5-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="150e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="150e5-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="150e5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="150e5-105">DESCRIPTION</span></span>
<span data-ttu-id="150e5-106">Mit dem Cmdlet **New-AzHDInsightSqoopJobDefinition** wird ein Sqoop-Auftragsobjekt für die Verwendung mit einem Azure HDInsight-Cluster definiert.</span><span class="sxs-lookup"><span data-stu-id="150e5-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="150e5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="150e5-107">EXAMPLES</span></span>

### <span data-ttu-id="150e5-108">Beispiel 1: Erstellen einer Sqoop-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="150e5-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="150e5-109">Mit diesem Befehl wird eine Sqoop-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="150e5-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="150e5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="150e5-110">PARAMETERS</span></span>

### <span data-ttu-id="150e5-111">-Befehl</span><span class="sxs-lookup"><span data-stu-id="150e5-111">-Command</span></span>
<span data-ttu-id="150e5-112">Gibt den Sqoop-Befehl an.</span><span class="sxs-lookup"><span data-stu-id="150e5-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="150e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150e5-113">-DefaultProfile</span></span>
<span data-ttu-id="150e5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="150e5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="150e5-115">-Datei</span><span class="sxs-lookup"><span data-stu-id="150e5-115">-File</span></span>
<span data-ttu-id="150e5-116">Gibt den Pfad zu einer Datei an, die die auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="150e5-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="150e5-117">Die Datei muss auf dem dem Cluster zugeordneten Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="150e5-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="150e5-118">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="150e5-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="150e5-119">-Dateien</span><span class="sxs-lookup"><span data-stu-id="150e5-119">-Files</span></span>
<span data-ttu-id="150e5-120">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="150e5-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="150e5-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="150e5-121">-LibDir</span></span>
<span data-ttu-id="150e5-122">Gibt das Bibliotheksverzeichnis für den Sqoop-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="150e5-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="150e5-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="150e5-123">-StatusFolder</span></span>
<span data-ttu-id="150e5-124">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="150e5-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="150e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150e5-125">CommonParameters</span></span>
<span data-ttu-id="150e5-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150e5-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="150e5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150e5-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="150e5-128">INPUTS</span></span>

### <span data-ttu-id="150e5-129">Keine</span><span class="sxs-lookup"><span data-stu-id="150e5-129">None</span></span>

## <span data-ttu-id="150e5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="150e5-130">OUTPUTS</span></span>

### <span data-ttu-id="150e5-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="150e5-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="150e5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="150e5-132">NOTES</span></span>

## <span data-ttu-id="150e5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="150e5-133">RELATED LINKS</span></span>

[<span data-ttu-id="150e5-134">Anfang-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="150e5-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


