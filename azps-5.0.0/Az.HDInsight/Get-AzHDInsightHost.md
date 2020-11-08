---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 2e9e8858e79521c32cdf08b980584fd2b77dd955
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175579"
---
# <span data-ttu-id="7a801-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="7a801-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="7a801-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a801-102">SYNOPSIS</span></span>
<span data-ttu-id="7a801-103">Listet die Hosts des HDInsight-Clusters auf.</span><span class="sxs-lookup"><span data-stu-id="7a801-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="7a801-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a801-104">SYNTAX</span></span>

### <span data-ttu-id="7a801-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a801-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a801-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a801-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a801-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a801-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [[-DefaultProfile] <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a801-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a801-108">DESCRIPTION</span></span>
<span data-ttu-id="7a801-109">Das Cmdlet " **Get-AzHDInsightHost** " listet die Hosts des HDInsight-Clusters auf.</span><span class="sxs-lookup"><span data-stu-id="7a801-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="7a801-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a801-110">EXAMPLES</span></span>

### <span data-ttu-id="7a801-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a801-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="7a801-112">Dieser Befehl listet die Clusterhosts mit dem Clusternamen auf.</span><span class="sxs-lookup"><span data-stu-id="7a801-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="7a801-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7a801-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="7a801-114">Dieser Befehl listet die Clusterhosts mit Pipeline auf.</span><span class="sxs-lookup"><span data-stu-id="7a801-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="7a801-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a801-115">PARAMETERS</span></span>

### <span data-ttu-id="7a801-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="7a801-116">-ClusterName</span></span>
<span data-ttu-id="7a801-117">Ruft den Namen des Clusters ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="7a801-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="7a801-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a801-118">-DefaultProfile</span></span>
<span data-ttu-id="7a801-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a801-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a801-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7a801-120">-InputObject</span></span>
<span data-ttu-id="7a801-121">Ruft das Eingabeobjekt ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="7a801-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="7a801-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a801-122">-ResourceGroupName</span></span>
<span data-ttu-id="7a801-123">Ruft den Namen der Ressourcengruppe ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="7a801-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="7a801-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7a801-124">-ResourceId</span></span>
<span data-ttu-id="7a801-125">Ruft die Ressourcen-ID ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7a801-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="7a801-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a801-126">CommonParameters</span></span>
<span data-ttu-id="7a801-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a801-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a801-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a801-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a801-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a801-129">INPUTS</span></span>

### <span data-ttu-id="7a801-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="7a801-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="7a801-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a801-131">OUTPUTS</span></span>

### <span data-ttu-id="7a801-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="7a801-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="7a801-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a801-133">NOTES</span></span>

## <span data-ttu-id="7a801-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a801-134">RELATED LINKS</span></span>
