---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 430c2aa7f38e6246c13ef6045f52346b580d20fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458547"
---
# <span data-ttu-id="53bcc-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="53bcc-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="53bcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="53bcc-103">Listet die Hosts des Cluster "HDInsight" auf.</span><span class="sxs-lookup"><span data-stu-id="53bcc-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="53bcc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53bcc-104">SYNTAX</span></span>

### <span data-ttu-id="53bcc-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="53bcc-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53bcc-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53bcc-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53bcc-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53bcc-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53bcc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53bcc-108">DESCRIPTION</span></span>
<span data-ttu-id="53bcc-109">Das **Cmdlet "Get-AzHDInsightHost"** listet die Hosts des Cluster "HDInsight" auf.</span><span class="sxs-lookup"><span data-stu-id="53bcc-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="53bcc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53bcc-110">EXAMPLES</span></span>

### <span data-ttu-id="53bcc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53bcc-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="53bcc-112">Diese Befehlsliste der Clusterhosts mit Clusternamen.</span><span class="sxs-lookup"><span data-stu-id="53bcc-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="53bcc-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="53bcc-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="53bcc-114">Diese Befehlsliste der Clusterhosts mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="53bcc-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="53bcc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53bcc-115">PARAMETERS</span></span>

### <span data-ttu-id="53bcc-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="53bcc-116">-ClusterName</span></span>
<span data-ttu-id="53bcc-117">Ruft den Namen des Cluster ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="53bcc-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="53bcc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bcc-118">-DefaultProfile</span></span>
<span data-ttu-id="53bcc-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53bcc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53bcc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53bcc-120">-InputObject</span></span>
<span data-ttu-id="53bcc-121">Ruft das Eingabeobjekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="53bcc-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="53bcc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53bcc-122">-ResourceGroupName</span></span>
<span data-ttu-id="53bcc-123">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="53bcc-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="53bcc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53bcc-124">-ResourceId</span></span>
<span data-ttu-id="53bcc-125">Ruft die Ressourcen-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="53bcc-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="53bcc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bcc-126">CommonParameters</span></span>
<span data-ttu-id="53bcc-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bcc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bcc-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53bcc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bcc-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53bcc-129">INPUTS</span></span>

### <span data-ttu-id="53bcc-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="53bcc-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="53bcc-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53bcc-131">OUTPUTS</span></span>

### <span data-ttu-id="53bcc-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="53bcc-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="53bcc-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53bcc-133">NOTES</span></span>

## <span data-ttu-id="53bcc-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53bcc-134">RELATED LINKS</span></span>
