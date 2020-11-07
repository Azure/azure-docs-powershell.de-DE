---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
ms.openlocfilehash: 7045131d7f94aab65ec1947f9fe65d25347c9f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665047"
---
# <span data-ttu-id="45b53-101">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="45b53-101">New-AzureRmHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="45b53-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45b53-102">SYNOPSIS</span></span>
<span data-ttu-id="45b53-103">Erstellt ein Pig-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="45b53-103">Creates a Pig job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b53-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45b53-104">SYNTAX</span></span>

```
New-AzureRmHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b53-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b53-105">DESCRIPTION</span></span>
<span data-ttu-id="45b53-106">Das Cmdlet **New-AzureRmHDInsightPigJobDefinition** definiert ein Pig-Auftragsobjekt zur Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="45b53-106">The **New-AzureRmHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="45b53-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45b53-107">EXAMPLES</span></span>

### <span data-ttu-id="45b53-108">Beispiel 1: Erstellen einer Pig-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="45b53-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="45b53-109">Mit diesem Befehl wird eine Pig-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="45b53-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="45b53-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b53-110">PARAMETERS</span></span>

### <span data-ttu-id="45b53-111">-Argumente</span><span class="sxs-lookup"><span data-stu-id="45b53-111">-Arguments</span></span>
<span data-ttu-id="45b53-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="45b53-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="45b53-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="45b53-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="45b53-114">-Datei</span><span class="sxs-lookup"><span data-stu-id="45b53-114">-File</span></span>
<span data-ttu-id="45b53-115">Gibt den Pfad zu einer Datei an, die die auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="45b53-115">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="45b53-116">Die Datei muss auf dem dem Cluster zugeordneten Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="45b53-116">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="45b53-117">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="45b53-117">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="45b53-118">-Dateien</span><span class="sxs-lookup"><span data-stu-id="45b53-118">-Files</span></span>
<span data-ttu-id="45b53-119">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="45b53-119">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="45b53-120">-Query</span><span class="sxs-lookup"><span data-stu-id="45b53-120">-Query</span></span>
<span data-ttu-id="45b53-121">Gibt die Schweine Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="45b53-121">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="45b53-122">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="45b53-122">-StatusFolder</span></span>
<span data-ttu-id="45b53-123">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="45b53-123">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="45b53-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b53-124">-DefaultProfile</span></span>
<span data-ttu-id="45b53-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45b53-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b53-126">CommonParameters</span></span>
<span data-ttu-id="45b53-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b53-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b53-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b53-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45b53-129">INPUTS</span></span>

## <span data-ttu-id="45b53-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45b53-130">OUTPUTS</span></span>

### <span data-ttu-id="45b53-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="45b53-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="45b53-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="45b53-132">NOTES</span></span>

## <span data-ttu-id="45b53-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45b53-133">RELATED LINKS</span></span>

[<span data-ttu-id="45b53-134">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="45b53-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


