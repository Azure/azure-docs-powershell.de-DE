---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 5b58e535acae8d6d0845b6be8c838f8372af9c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948672"
---
# <span data-ttu-id="64a64-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="64a64-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="64a64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64a64-102">SYNOPSIS</span></span>
<span data-ttu-id="64a64-103">Listet die Hosts des HDInsight-Clusters auf.</span><span class="sxs-lookup"><span data-stu-id="64a64-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="64a64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64a64-104">SYNTAX</span></span>

### <span data-ttu-id="64a64-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="64a64-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64a64-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64a64-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64a64-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64a64-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64a64-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64a64-108">DESCRIPTION</span></span>
<span data-ttu-id="64a64-109">Das **Get-AzHDInsightHost-Cmdlet** listet die Hosts des HDInsight-Clusters auf.</span><span class="sxs-lookup"><span data-stu-id="64a64-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="64a64-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64a64-110">EXAMPLES</span></span>

### <span data-ttu-id="64a64-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64a64-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="64a64-112">Dieser Befehl listet die Hosts des Clusters mit dem Clusternamen auf.</span><span class="sxs-lookup"><span data-stu-id="64a64-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="64a64-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="64a64-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="64a64-114">Dieser Befehl listet die Hosts des Clusters mit Pipeline auf.</span><span class="sxs-lookup"><span data-stu-id="64a64-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="64a64-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="64a64-115">PARAMETERS</span></span>

### <span data-ttu-id="64a64-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64a64-116">-ClusterName</span></span>
<span data-ttu-id="64a64-117">Ruft den Namen des Clusters ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="64a64-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a64-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a64-118">-DefaultProfile</span></span>
<span data-ttu-id="64a64-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64a64-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a64-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64a64-120">-InputObject</span></span>
<span data-ttu-id="64a64-121">Ruft das Eingabeobjekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="64a64-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64a64-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a64-122">-ResourceGroupName</span></span>
<span data-ttu-id="64a64-123">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="64a64-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a64-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64a64-124">-ResourceId</span></span>
<span data-ttu-id="64a64-125">Ruft die Ressourcen-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="64a64-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64a64-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a64-126">CommonParameters</span></span>
<span data-ttu-id="64a64-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a64-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a64-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64a64-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a64-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64a64-129">INPUTS</span></span>

### <span data-ttu-id="64a64-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="64a64-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="64a64-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64a64-131">OUTPUTS</span></span>

### <span data-ttu-id="64a64-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="64a64-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="64a64-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="64a64-133">NOTES</span></span>

## <span data-ttu-id="64a64-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="64a64-134">RELATED LINKS</span></span>
