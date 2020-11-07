---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 769406d0eb47672fcaaea8acfb3b3fdccd6810d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664767"
---
# <span data-ttu-id="0b717-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0b717-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="0b717-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b717-102">SYNOPSIS</span></span>
<span data-ttu-id="0b717-103">Erstellt ein Sqoop-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0b717-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b717-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b717-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b717-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b717-105">DESCRIPTION</span></span>
<span data-ttu-id="0b717-106">Mit dem Cmdlet **New-AzureRmHDInsightSqoopJobDefinition** wird ein Sqoop-Auftragsobjekt für die Verwendung mit einem Azure HDInsight-Cluster definiert.</span><span class="sxs-lookup"><span data-stu-id="0b717-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0b717-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b717-107">EXAMPLES</span></span>

### <span data-ttu-id="0b717-108">Beispiel 1: Erstellen einer Sqoop-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="0b717-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="0b717-109">Mit diesem Befehl wird eine Sqoop-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="0b717-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="0b717-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b717-110">PARAMETERS</span></span>

### <span data-ttu-id="0b717-111">-Befehl</span><span class="sxs-lookup"><span data-stu-id="0b717-111">-Command</span></span>
<span data-ttu-id="0b717-112">Gibt den Sqoop-Befehl an.</span><span class="sxs-lookup"><span data-stu-id="0b717-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="0b717-113">-Datei</span><span class="sxs-lookup"><span data-stu-id="0b717-113">-File</span></span>
<span data-ttu-id="0b717-114">Gibt den Pfad zu einer Datei an, die die auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="0b717-114">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="0b717-115">Die Datei muss auf dem dem Cluster zugeordneten Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="0b717-115">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="0b717-116">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b717-116">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="0b717-117">-Dateien</span><span class="sxs-lookup"><span data-stu-id="0b717-117">-Files</span></span>
<span data-ttu-id="0b717-118">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0b717-118">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="0b717-119">-LibDir</span><span class="sxs-lookup"><span data-stu-id="0b717-119">-LibDir</span></span>
<span data-ttu-id="0b717-120">Gibt das Bibliotheksverzeichnis für den Sqoop-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0b717-120">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="0b717-121">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="0b717-121">-StatusFolder</span></span>
<span data-ttu-id="0b717-122">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="0b717-122">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="0b717-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b717-123">-DefaultProfile</span></span>
<span data-ttu-id="0b717-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b717-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b717-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b717-125">CommonParameters</span></span>
<span data-ttu-id="0b717-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b717-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b717-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b717-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b717-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b717-128">INPUTS</span></span>

## <span data-ttu-id="0b717-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b717-129">OUTPUTS</span></span>

### <span data-ttu-id="0b717-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0b717-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="0b717-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b717-131">NOTES</span></span>

## <span data-ttu-id="0b717-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b717-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b717-133">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0b717-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


