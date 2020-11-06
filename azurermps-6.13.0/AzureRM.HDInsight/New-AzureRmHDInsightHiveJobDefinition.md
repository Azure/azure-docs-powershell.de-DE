---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: 99ed451e43062cd5411a7a8bc1577646226aa8b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502110"
---
# <span data-ttu-id="a8f67-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a8f67-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="a8f67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8f67-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f67-103">Erstellt ein Hive-Auftragsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a8f67-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8f67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8f67-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8f67-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8f67-105">DESCRIPTION</span></span>
<span data-ttu-id="a8f67-106">Das Cmdlet **New-AzureRmHDInsightHiveJobDefinition** definiert ein Hive Job-Objekt zur Verwendung mit einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a8f67-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a8f67-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8f67-107">EXAMPLES</span></span>

### <span data-ttu-id="a8f67-108">Beispiel 1: Erstellen einer Hive-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="a8f67-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="a8f67-109">Mit diesem Befehl wird eine Hive-Auftragsdefinition erstellt.</span><span class="sxs-lookup"><span data-stu-id="a8f67-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="a8f67-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8f67-110">PARAMETERS</span></span>

### <span data-ttu-id="a8f67-111">-Argumente</span><span class="sxs-lookup"><span data-stu-id="a8f67-111">-Arguments</span></span>
<span data-ttu-id="a8f67-112">Gibt ein Array von Argumenten für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="a8f67-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="a8f67-113">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="a8f67-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="a8f67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f67-114">-DefaultProfile</span></span>
<span data-ttu-id="a8f67-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a8f67-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8f67-116">– Definiert</span><span class="sxs-lookup"><span data-stu-id="a8f67-116">-Defines</span></span>
<span data-ttu-id="a8f67-117">Gibt Hadoop-Konfigurationswerte an, die für die Ausführung des Auftrags festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8f67-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f67-118">-Datei</span><span class="sxs-lookup"><span data-stu-id="a8f67-118">-File</span></span>
<span data-ttu-id="a8f67-119">Gibt den Pfad zu einer Datei an, die die auszuführende Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="a8f67-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="a8f67-120">Die Datei muss auf dem dem Cluster zugeordneten Speicherkonto verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a8f67-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="a8f67-121">Sie können diesen Parameter anstelle des *Abfrage* Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8f67-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="a8f67-122">-Dateien</span><span class="sxs-lookup"><span data-stu-id="a8f67-122">-Files</span></span>
<span data-ttu-id="a8f67-123">Gibt eine Sammlung von Dateien an, die einem Hive-Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a8f67-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="a8f67-124">-Jobname</span><span class="sxs-lookup"><span data-stu-id="a8f67-124">-JobName</span></span>
<span data-ttu-id="a8f67-125">Gibt den Namen des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="a8f67-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="a8f67-126">-Query</span><span class="sxs-lookup"><span data-stu-id="a8f67-126">-Query</span></span>
<span data-ttu-id="a8f67-127">Gibt die Hive-Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="a8f67-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="a8f67-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="a8f67-128">-RunAsFileJob</span></span>
<span data-ttu-id="a8f67-129">Gibt an, dass dieses Cmdlet eine Datei im standardmäßigen Azure-Speicherkonto erstellt, in dem eine Abfrage gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8f67-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="a8f67-130">Dieses Cmdlet übermittelt den Auftrag, der auf diese Datei verweist, als Skript, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8f67-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="a8f67-131">Sie können diese Funktion zum Behandeln von Sonderzeichen wie Prozentzeichen (%) verwenden. Dies würde bei einer Auftragsübermittlung über Templeton fehlschlagen, da Templeton eine Abfrage mit einem Prozentzeichen als URL-Parameter interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a8f67-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f67-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="a8f67-132">-StatusFolder</span></span>
<span data-ttu-id="a8f67-133">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="a8f67-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="a8f67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f67-134">CommonParameters</span></span>
<span data-ttu-id="a8f67-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8f67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f67-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8f67-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f67-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8f67-137">INPUTS</span></span>

### <span data-ttu-id="a8f67-138">Keine</span><span class="sxs-lookup"><span data-stu-id="a8f67-138">None</span></span>

## <span data-ttu-id="a8f67-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8f67-139">OUTPUTS</span></span>

### <span data-ttu-id="a8f67-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a8f67-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="a8f67-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8f67-141">NOTES</span></span>

## <span data-ttu-id="a8f67-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8f67-142">RELATED LINKS</span></span>

[<span data-ttu-id="a8f67-143">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a8f67-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


