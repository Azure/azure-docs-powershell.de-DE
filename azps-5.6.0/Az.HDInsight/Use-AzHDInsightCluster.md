---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: c9b95a1f16c90eb3c6e057707dbf63d431b9a1ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949392"
---
# <span data-ttu-id="64f39-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="64f39-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="64f39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f39-102">SYNOPSIS</span></span>
<span data-ttu-id="64f39-103">Wählt einen Cluster aus, der mit dem cmdlet Invoke-RmAzureHDInsightHiveJob werden soll.</span><span class="sxs-lookup"><span data-stu-id="64f39-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="64f39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64f39-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64f39-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64f39-105">DESCRIPTION</span></span>
<span data-ttu-id="64f39-106">Das **Use-AzHDInsightCluster-Cmdlet** wählt den Azure HDInsight-Cluster für das Invoke-AzHDInsightHiveJob-Cmdlet aus, das zum Übermitteln von Hive-Aufträgen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64f39-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="64f39-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64f39-107">EXAMPLES</span></span>

### <span data-ttu-id="64f39-108">Beispiel 1: Auswählen eines Clusters für die Übermittlung von Hive-Abfragen</span><span class="sxs-lookup"><span data-stu-id="64f39-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="64f39-109">Mit diesem Befehl wird ein Cluster für eine Hive-Abfrageübermittlung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="64f39-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="64f39-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="64f39-110">PARAMETERS</span></span>

### <span data-ttu-id="64f39-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64f39-111">-ClusterName</span></span>
<span data-ttu-id="64f39-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="64f39-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="64f39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f39-113">-DefaultProfile</span></span>
<span data-ttu-id="64f39-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="64f39-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64f39-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="64f39-115">-HttpCredential</span></span>
<span data-ttu-id="64f39-116">Gibt die Anmeldeinformationen für den Cluster (Cluster Login, HTTP) für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="64f39-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f39-117">-ResourceGroupName</span></span>
<span data-ttu-id="64f39-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="64f39-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="64f39-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f39-119">CommonParameters</span></span>
<span data-ttu-id="64f39-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f39-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f39-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64f39-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f39-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64f39-122">INPUTS</span></span>

### <span data-ttu-id="64f39-123">Keine</span><span class="sxs-lookup"><span data-stu-id="64f39-123">None</span></span>

## <span data-ttu-id="64f39-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64f39-124">OUTPUTS</span></span>

### <span data-ttu-id="64f39-125">System.String</span><span class="sxs-lookup"><span data-stu-id="64f39-125">System.String</span></span>

## <span data-ttu-id="64f39-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="64f39-126">NOTES</span></span>

## <span data-ttu-id="64f39-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="64f39-127">RELATED LINKS</span></span>

[<span data-ttu-id="64f39-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="64f39-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="64f39-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="64f39-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


