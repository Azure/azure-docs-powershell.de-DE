---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 400153558dffc619e8e567b292ad402a42ce9359
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458543"
---
# <span data-ttu-id="f6a62-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="f6a62-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="f6a62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6a62-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a62-103">Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem angegebenen Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f6a62-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="f6a62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6a62-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6a62-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a62-106">Das **Cmdlet "Get-AzHDInsightJobOutput"** ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem Azure -HDInsight-Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f6a62-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f6a62-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6a62-107">EXAMPLES</span></span>

### <span data-ttu-id="f6a62-108">Beispiel 1: Erhalten der Protokollausgabe für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f6a62-108">Example 1: Get the log output for a job</span></span>
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

<span data-ttu-id="f6a62-109">Dieser Befehl ruft die Protokollausgabe aus dem Cluster mit dem Namen "your-hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="f6a62-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f6a62-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6a62-110">PARAMETERS</span></span>

### <span data-ttu-id="f6a62-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f6a62-111">-ClusterName</span></span>
<span data-ttu-id="f6a62-112">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f6a62-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f6a62-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="f6a62-113">-DefaultContainer</span></span>
<span data-ttu-id="f6a62-114">Gibt den Standardcontainernamen an.</span><span class="sxs-lookup"><span data-stu-id="f6a62-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="f6a62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a62-115">-DefaultProfile</span></span>
<span data-ttu-id="f6a62-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f6a62-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6a62-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f6a62-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="f6a62-118">Gibt den Standardspeicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="f6a62-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="f6a62-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f6a62-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="f6a62-120">Gibt den Standardnamen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f6a62-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="f6a62-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="f6a62-121">-DisplayOutputType</span></span>
<span data-ttu-id="f6a62-122">Gibt den angeforderten Auftragsausgabetyp an.</span><span class="sxs-lookup"><span data-stu-id="f6a62-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="f6a62-123">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="f6a62-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6a62-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="f6a62-124">StandardOutput</span></span>
- <span data-ttu-id="f6a62-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="f6a62-125">StandardError</span></span>

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

### <span data-ttu-id="f6a62-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f6a62-126">-HttpCredential</span></span>
<span data-ttu-id="f6a62-127">Gibt die Anmeldeinformationen für den Cluster (Cluster Login, HTTP) für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f6a62-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="f6a62-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="f6a62-128">-JobId</span></span>
<span data-ttu-id="f6a62-129">Gibt die Auftrags-ID des Auftrags an, dessen Ausgabe abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f6a62-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="f6a62-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a62-130">-ResourceGroupName</span></span>
<span data-ttu-id="f6a62-131">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f6a62-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f6a62-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a62-132">CommonParameters</span></span>
<span data-ttu-id="f6a62-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a62-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a62-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6a62-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a62-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6a62-135">INPUTS</span></span>

### <span data-ttu-id="f6a62-136">Keine</span><span class="sxs-lookup"><span data-stu-id="f6a62-136">None</span></span>

## <span data-ttu-id="f6a62-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6a62-137">OUTPUTS</span></span>

### <span data-ttu-id="f6a62-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f6a62-138">System.String</span></span>

## <span data-ttu-id="f6a62-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f6a62-139">NOTES</span></span>

## <span data-ttu-id="f6a62-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f6a62-140">RELATED LINKS</span></span>

[<span data-ttu-id="f6a62-141">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f6a62-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f6a62-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f6a62-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


