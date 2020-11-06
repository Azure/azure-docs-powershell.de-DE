---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: eebbe6fb233b0d6117411973e841cf39f2ae377d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500021"
---
# <span data-ttu-id="e0068-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="e0068-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="e0068-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0068-102">SYNOPSIS</span></span>
<span data-ttu-id="e0068-103">Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem angegebenen Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0068-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0068-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0068-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0068-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0068-105">DESCRIPTION</span></span>
<span data-ttu-id="e0068-106">Das Cmdlet " **Get-AzureRmHDInsightJobOutput** " Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem Azure HDInsight-Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0068-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e0068-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0068-107">EXAMPLES</span></span>

### <span data-ttu-id="e0068-108">Beispiel 1: Abrufen der Protokollausgabe für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="e0068-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="e0068-109">Dieser Befehl ruft die Protokollausgabe des Clusters mit dem Namen "Your-Hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="e0068-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e0068-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0068-110">PARAMETERS</span></span>

### <span data-ttu-id="e0068-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="e0068-111">-ClusterName</span></span>
<span data-ttu-id="e0068-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e0068-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0068-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="e0068-113">-DefaultContainer</span></span>
<span data-ttu-id="e0068-114">Gibt den Standardcontainernamen an.</span><span class="sxs-lookup"><span data-stu-id="e0068-114">Specifies the default container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0068-115">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e0068-115">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="e0068-116">Gibt den standardmäßigen speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="e0068-116">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0068-117">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e0068-117">-DefaultStorageAccountName</span></span>
<span data-ttu-id="e0068-118">Gibt den Namen des Standardspeicher Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e0068-118">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0068-119">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="e0068-119">-DisplayOutputType</span></span>
<span data-ttu-id="e0068-120">Gibt den Auftrags Ausgabetyp an, der angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="e0068-120">Specifies the job output type being requested.</span></span>
<span data-ttu-id="e0068-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e0068-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e0068-122">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="e0068-122">StandardOutput</span></span>
- <span data-ttu-id="e0068-123">StandardError</span><span class="sxs-lookup"><span data-stu-id="e0068-123">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases: 
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0068-124">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e0068-124">-HttpCredential</span></span>
<span data-ttu-id="e0068-125">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e0068-125">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0068-126">-JobId</span><span class="sxs-lookup"><span data-stu-id="e0068-126">-JobId</span></span>
<span data-ttu-id="e0068-127">Gibt die Auftrags-ID des Auftrags an, dessen Ausgabe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0068-127">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0068-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0068-128">-ResourceGroupName</span></span>
<span data-ttu-id="e0068-129">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e0068-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e0068-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0068-130">-DefaultProfile</span></span>
<span data-ttu-id="e0068-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0068-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0068-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0068-132">CommonParameters</span></span>
<span data-ttu-id="e0068-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0068-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0068-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0068-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0068-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0068-135">INPUTS</span></span>

## <span data-ttu-id="e0068-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0068-136">OUTPUTS</span></span>

### <span data-ttu-id="e0068-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e0068-137">System.String</span></span>

## <span data-ttu-id="e0068-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0068-138">NOTES</span></span>

## <span data-ttu-id="e0068-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0068-139">RELATED LINKS</span></span>

[<span data-ttu-id="e0068-140">Neu – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e0068-140">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="e0068-141">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e0068-141">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


