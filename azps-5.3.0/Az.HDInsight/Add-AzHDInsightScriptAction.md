---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: 2759059da9bc37f942eaa733319539bc1fa53b5b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458555"
---
# <span data-ttu-id="58c9c-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="58c9c-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="58c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="58c9c-103">Fügt einem Clusterkonfigurationsobjekt eine Skriptaktion hinzu.</span><span class="sxs-lookup"><span data-stu-id="58c9c-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="58c9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58c9c-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58c9c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="58c9c-106">Das **Cmdlet "Add-AzHDInsightScriptAction"** fügt dem hdInsight-Konfigurationsobjekt, das vom cmdlet für New-AzHDInsightClusterConfig erstellt wurde, Skriptaktionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="58c9c-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="58c9c-107">Skriptaktionen stellen Funktionen bereit, die verwendet werden, um zusätzliche Software zu installieren oder die Konfiguration von Anwendungen zu ändern, die mit Windows PowerShell- oder Bash-Skripts (für Windows- bzw. Linux-Cluster) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="58c9c-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="58c9c-108">Eine Skriptaktion wird für die Clusterknoten ausgeführt, wenn die HDInsight-Cluster bereitgestellt werden, und sie werden nach Knoten im Cluster ausgeführt, die die Konfiguration "HDInsight" abschließen.</span><span class="sxs-lookup"><span data-stu-id="58c9c-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="58c9c-109">Die Skriptaktion wird unter den Berechtigungen des Systemadministratorkontos ausgeführt und bietet Vollzugriff auf die Clusterknoten.</span><span class="sxs-lookup"><span data-stu-id="58c9c-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="58c9c-110">Sie können jedem Cluster eine Liste von Skriptaktionen bereitstellen, die in einer bestimmten Reihenfolge ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="58c9c-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="58c9c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58c9c-111">EXAMPLES</span></span>

### <span data-ttu-id="58c9c-112">Beispiel 1: Hinzufügen einer Skriptaktion zum Clusterkonfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="58c9c-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="58c9c-113">Dieser Befehl fügt eine Skriptaktion für die Head- und Workerknoten des Ihr-Hadoop-001-Cluster hinzu, die am Ende der Clustererstellung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58c9c-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="58c9c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58c9c-114">PARAMETERS</span></span>

### <span data-ttu-id="58c9c-115">-Config</span><span class="sxs-lookup"><span data-stu-id="58c9c-115">-Config</span></span>
<span data-ttu-id="58c9c-116">Gibt das Konfigurationsobjekt für den HDInsight-Cluster an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="58c9c-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="58c9c-117">Dieses Objekt wird vom Cmdlet **"New-AzHDInsightClusterConfig"** erstellt.</span><span class="sxs-lookup"><span data-stu-id="58c9c-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58c9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c9c-118">-DefaultProfile</span></span>
<span data-ttu-id="58c9c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="58c9c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58c9c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="58c9c-120">-Name</span></span>
<span data-ttu-id="58c9c-121">Gibt den Namen der Skriptaktion an.</span><span class="sxs-lookup"><span data-stu-id="58c9c-121">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c9c-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="58c9c-122">-NodeType</span></span>
<span data-ttu-id="58c9c-123">Gibt den Knotentyp an, für den die Skriptaktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58c9c-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="58c9c-124">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="58c9c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58c9c-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="58c9c-125">HeadNode</span></span>
- <span data-ttu-id="58c9c-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="58c9c-126">WorkerNode</span></span>
- <span data-ttu-id="58c9c-127">HüttnerNode</span><span class="sxs-lookup"><span data-stu-id="58c9c-127">ZookeeperNode</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c9c-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="58c9c-128">-Parameters</span></span>
<span data-ttu-id="58c9c-129">Gibt die Parameter für die Skriptaktion an.</span><span class="sxs-lookup"><span data-stu-id="58c9c-129">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="58c9c-130">-URI</span><span class="sxs-lookup"><span data-stu-id="58c9c-130">-Uri</span></span>
<span data-ttu-id="58c9c-131">Gibt den öffentlichen URI für die Skriptaktion an (ein PowerShell- oder Bash-Skript).</span><span class="sxs-lookup"><span data-stu-id="58c9c-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c9c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c9c-132">CommonParameters</span></span>
<span data-ttu-id="58c9c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c9c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c9c-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58c9c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c9c-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58c9c-135">INPUTS</span></span>

### <span data-ttu-id="58c9c-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="58c9c-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="58c9c-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58c9c-137">OUTPUTS</span></span>

### <span data-ttu-id="58c9c-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="58c9c-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="58c9c-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58c9c-139">NOTES</span></span>

## <span data-ttu-id="58c9c-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58c9c-140">RELATED LINKS</span></span>

[<span data-ttu-id="58c9c-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="58c9c-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


