---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 6f7045773dc1bf5582e2c480fd9e4aed283bf8ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496577"
---
# <span data-ttu-id="51fa8-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="51fa8-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="51fa8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="51fa8-103">Erstellt ein Sqoop-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="51fa8-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51fa8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51fa8-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51fa8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51fa8-105">DESCRIPTION</span></span>
<span data-ttu-id="51fa8-106">Mit dem Cmdlet **New-AzureRmHDInsightSqoopJobDefinition** wird ein Sqoop-Auftragsobjekt für die Verwendung mit einem Azure HDInsight-Cluster definiert.</span><span class="sxs-lookup"><span data-stu-id="51fa8-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="51fa8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51fa8-107">EXAMPLES</span></span>

### <span data-ttu-id="51fa8-108">Beispiel 1: Erstellen einer Sqoop-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="51fa8-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="51fa8-109">Mit diesem Befehl wird eine Sqoop-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="51fa8-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="51fa8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="51fa8-110">PARAMETERS</span></span>

### <span data-ttu-id="51fa8-111">-Befehl</span><span class="sxs-lookup"><span data-stu-id="51fa8-111">-Command</span></span>
<span data-ttu-id="51fa8-112">Gibt den Sqoop-Befehl an.</span><span class="sxs-lookup"><span data-stu-id="51fa8-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="51fa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fa8-113">-DefaultProfile</span></span>
<span data-ttu-id="51fa8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="51fa8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51fa8-115">-Datei</span><span class="sxs-lookup"><span data-stu-id="51fa8-115">-File</span></span>
<span data-ttu-id="51fa8-116">Gibt den Pfad zu einer Datei an, die die auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="51fa8-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="51fa8-117">Die Datei muss auf dem dem Cluster zugeordneten Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="51fa8-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="51fa8-118">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="51fa8-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="51fa8-119">-Dateien</span><span class="sxs-lookup"><span data-stu-id="51fa8-119">-Files</span></span>
<span data-ttu-id="51fa8-120">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="51fa8-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="51fa8-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="51fa8-121">-LibDir</span></span>
<span data-ttu-id="51fa8-122">Gibt das Bibliotheksverzeichnis für den Sqoop-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="51fa8-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="51fa8-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="51fa8-123">-StatusFolder</span></span>
<span data-ttu-id="51fa8-124">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="51fa8-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="51fa8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fa8-125">CommonParameters</span></span>
<span data-ttu-id="51fa8-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51fa8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fa8-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51fa8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fa8-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51fa8-128">INPUTS</span></span>

### <span data-ttu-id="51fa8-129">Keine</span><span class="sxs-lookup"><span data-stu-id="51fa8-129">None</span></span>
<span data-ttu-id="51fa8-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="51fa8-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51fa8-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51fa8-131">OUTPUTS</span></span>

### <span data-ttu-id="51fa8-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="51fa8-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="51fa8-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="51fa8-133">NOTES</span></span>

## <span data-ttu-id="51fa8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51fa8-134">RELATED LINKS</span></span>

[<span data-ttu-id="51fa8-135">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="51fa8-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


