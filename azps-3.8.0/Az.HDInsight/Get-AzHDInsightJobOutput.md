---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 2489da10ebf1d346b147e252d6d347635efb1aff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847579"
---
# <span data-ttu-id="70bff-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="70bff-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="70bff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70bff-102">SYNOPSIS</span></span>
<span data-ttu-id="70bff-103">Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem angegebenen Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="70bff-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="70bff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70bff-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70bff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70bff-105">DESCRIPTION</span></span>
<span data-ttu-id="70bff-106">Das Cmdlet " **Get-AzHDInsightJobOutput** " Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem Azure HDInsight-Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="70bff-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="70bff-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70bff-107">EXAMPLES</span></span>

### <span data-ttu-id="70bff-108">Beispiel 1: Abrufen der Protokollausgabe für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="70bff-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="70bff-109">Dieser Befehl ruft die Protokollausgabe des Clusters mit dem Namen "Your-Hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="70bff-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="70bff-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="70bff-110">PARAMETERS</span></span>

### <span data-ttu-id="70bff-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="70bff-111">-ClusterName</span></span>
<span data-ttu-id="70bff-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="70bff-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="70bff-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="70bff-113">-DefaultContainer</span></span>
<span data-ttu-id="70bff-114">Gibt den Standardcontainernamen an.</span><span class="sxs-lookup"><span data-stu-id="70bff-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="70bff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bff-115">-DefaultProfile</span></span>
<span data-ttu-id="70bff-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="70bff-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70bff-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="70bff-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="70bff-118">Gibt den standardmäßigen speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="70bff-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="70bff-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="70bff-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="70bff-120">Gibt den Namen des Standardspeicher Kontos an.</span><span class="sxs-lookup"><span data-stu-id="70bff-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="70bff-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="70bff-121">-DisplayOutputType</span></span>
<span data-ttu-id="70bff-122">Gibt den Auftrags Ausgabetyp an, der angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="70bff-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="70bff-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="70bff-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70bff-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="70bff-124">StandardOutput</span></span>
- <span data-ttu-id="70bff-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="70bff-125">StandardError</span></span>

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

### <span data-ttu-id="70bff-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="70bff-126">-HttpCredential</span></span>
<span data-ttu-id="70bff-127">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="70bff-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="70bff-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="70bff-128">-JobId</span></span>
<span data-ttu-id="70bff-129">Gibt die Auftrags-ID des Auftrags an, dessen Ausgabe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="70bff-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="70bff-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70bff-130">-ResourceGroupName</span></span>
<span data-ttu-id="70bff-131">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="70bff-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="70bff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bff-132">CommonParameters</span></span>
<span data-ttu-id="70bff-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70bff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bff-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bff-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bff-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70bff-135">INPUTS</span></span>

### <span data-ttu-id="70bff-136">Keine</span><span class="sxs-lookup"><span data-stu-id="70bff-136">None</span></span>

## <span data-ttu-id="70bff-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70bff-137">OUTPUTS</span></span>

### <span data-ttu-id="70bff-138">System. String</span><span class="sxs-lookup"><span data-stu-id="70bff-138">System.String</span></span>

## <span data-ttu-id="70bff-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="70bff-139">NOTES</span></span>

## <span data-ttu-id="70bff-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70bff-140">RELATED LINKS</span></span>

[<span data-ttu-id="70bff-141">Neu – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="70bff-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="70bff-142">Anfang-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="70bff-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


