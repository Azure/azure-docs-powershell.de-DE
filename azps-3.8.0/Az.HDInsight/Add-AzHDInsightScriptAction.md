---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: d103a2bc3d23ff37857592ed9496e625302ed144
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847608"
---
# <span data-ttu-id="94b6d-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="94b6d-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="94b6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="94b6d-103">Fügt einem Cluster Konfigurationsobjekt eine Skript Aktion hinzu.</span><span class="sxs-lookup"><span data-stu-id="94b6d-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="94b6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94b6d-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94b6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94b6d-105">DESCRIPTION</span></span>
<span data-ttu-id="94b6d-106">Das **Add-AzHDInsightScriptAction-** Cmdlet fügt dem vom New-AzHDInsightClusterConfig-Cmdlet erstellten HDInsight-Konfigurationsobjekt Skriptaktionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="94b6d-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="94b6d-107">Skriptaktionen stellen Funktionen bereit, die zum Installieren zusätzlicher Software oder zum Ändern der Konfiguration von Anwendungen, die auf einem Hadoop-Cluster ausgeführt werden, mithilfe von Windows PowerShell-oder Bash-Skripts (für Windows-oder Linux-Cluster) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94b6d-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="94b6d-108">Eine Skript Aktion wird auf den Clusterknoten ausgeführt, wenn HDInsight-Cluster bereitgestellt werden, und Sie werden ausgeführt, nachdem die Knoten im Cluster die HDInsight-Konfiguration abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="94b6d-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="94b6d-109">Die Skript Aktion wird unter Systemadministratorkonto Privilegien ausgeführt und bietet vollständige Zugriffsrechte für die Clusterknoten.</span><span class="sxs-lookup"><span data-stu-id="94b6d-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="94b6d-110">Sie können jedem Cluster eine Liste von Skriptaktionen zur Verfügung stellen, die in einer bestimmten Reihenfolge ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94b6d-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="94b6d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94b6d-111">EXAMPLES</span></span>

### <span data-ttu-id="94b6d-112">Beispiel 1: Hinzufügen einer Skript Aktion zum Cluster-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="94b6d-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="94b6d-113">Dieser Befehl fügt eine Skript Aktion für die Head-und worker-Knoten des Clusters your-Hadoop-001 hinzu, die am Ende der Clustererstellung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="94b6d-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="94b6d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="94b6d-114">PARAMETERS</span></span>

### <span data-ttu-id="94b6d-115">-Config</span><span class="sxs-lookup"><span data-stu-id="94b6d-115">-Config</span></span>
<span data-ttu-id="94b6d-116">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="94b6d-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="94b6d-117">Dieses Objekt wird vom Cmdlet **New-AzHDInsightClusterConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="94b6d-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="94b6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b6d-118">-DefaultProfile</span></span>
<span data-ttu-id="94b6d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="94b6d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94b6d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="94b6d-120">-Name</span></span>
<span data-ttu-id="94b6d-121">Gibt den Namen der Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="94b6d-121">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="94b6d-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="94b6d-122">-NodeType</span></span>
<span data-ttu-id="94b6d-123">Gibt den Knotentyp an, für den die Skript Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="94b6d-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="94b6d-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="94b6d-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94b6d-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="94b6d-125">HeadNode</span></span>
- <span data-ttu-id="94b6d-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="94b6d-126">WorkerNode</span></span>
- <span data-ttu-id="94b6d-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="94b6d-127">ZookeeperNode</span></span>

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

### <span data-ttu-id="94b6d-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="94b6d-128">-Parameters</span></span>
<span data-ttu-id="94b6d-129">Gibt die Parameter für die Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="94b6d-129">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="94b6d-130">-URI</span><span class="sxs-lookup"><span data-stu-id="94b6d-130">-Uri</span></span>
<span data-ttu-id="94b6d-131">Gibt den öffentlichen URI für die Skript Aktion an (ein PowerShell-oder bash-Skript).</span><span class="sxs-lookup"><span data-stu-id="94b6d-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="94b6d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b6d-132">CommonParameters</span></span>
<span data-ttu-id="94b6d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b6d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b6d-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b6d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b6d-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94b6d-135">INPUTS</span></span>

### <span data-ttu-id="94b6d-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="94b6d-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="94b6d-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94b6d-137">OUTPUTS</span></span>

### <span data-ttu-id="94b6d-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="94b6d-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="94b6d-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="94b6d-139">NOTES</span></span>

## <span data-ttu-id="94b6d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94b6d-140">RELATED LINKS</span></span>

[<span data-ttu-id="94b6d-141">Neu – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="94b6d-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


