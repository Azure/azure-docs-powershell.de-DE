---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
ms.openlocfilehash: 8606cc96cde6271fd3d986eb0047475cbe709aee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497602"
---
# <span data-ttu-id="59852-101">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="59852-101">New-AzureRmHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="59852-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59852-102">SYNOPSIS</span></span>
<span data-ttu-id="59852-103">Erstellt ein Pig-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="59852-103">Creates a Pig job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59852-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59852-104">SYNTAX</span></span>

```
New-AzureRmHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59852-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59852-105">DESCRIPTION</span></span>
<span data-ttu-id="59852-106">Das Cmdlet **New-AzureRmHDInsightPigJobDefinition** definiert ein Pig-Auftragsobjekt zur Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="59852-106">The **New-AzureRmHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="59852-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59852-107">EXAMPLES</span></span>

### <span data-ttu-id="59852-108">Beispiel 1: Erstellen einer Pig-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="59852-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="59852-109">Mit diesem Befehl wird eine Pig-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="59852-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="59852-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59852-110">PARAMETERS</span></span>

### <span data-ttu-id="59852-111">-Argumente</span><span class="sxs-lookup"><span data-stu-id="59852-111">-Arguments</span></span>
<span data-ttu-id="59852-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="59852-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="59852-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="59852-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59852-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59852-114">-DefaultProfile</span></span>
<span data-ttu-id="59852-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="59852-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59852-116">-Datei</span><span class="sxs-lookup"><span data-stu-id="59852-116">-File</span></span>
<span data-ttu-id="59852-117">Gibt den Pfad zu einer Datei an, die die auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="59852-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="59852-118">Die Datei muss auf dem dem Cluster zugeordneten Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="59852-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="59852-119">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="59852-119">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59852-120">-Dateien</span><span class="sxs-lookup"><span data-stu-id="59852-120">-Files</span></span>
<span data-ttu-id="59852-121">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="59852-121">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59852-122">-Query</span><span class="sxs-lookup"><span data-stu-id="59852-122">-Query</span></span>
<span data-ttu-id="59852-123">Gibt die Schweine Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="59852-123">Specifies the Pig query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59852-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="59852-124">-StatusFolder</span></span>
<span data-ttu-id="59852-125">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="59852-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59852-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59852-126">CommonParameters</span></span>
<span data-ttu-id="59852-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59852-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59852-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59852-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59852-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59852-129">INPUTS</span></span>

### <span data-ttu-id="59852-130">Keine</span><span class="sxs-lookup"><span data-stu-id="59852-130">None</span></span>
<span data-ttu-id="59852-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="59852-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59852-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59852-132">OUTPUTS</span></span>

### <span data-ttu-id="59852-133">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="59852-133">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="59852-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="59852-134">NOTES</span></span>

## <span data-ttu-id="59852-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59852-135">RELATED LINKS</span></span>

[<span data-ttu-id="59852-136">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="59852-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


