---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: bc78b7d791d0988ee692c12537aed3207066ba26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942320"
---
# <span data-ttu-id="97085-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="97085-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="97085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97085-102">SYNOPSIS</span></span>
<span data-ttu-id="97085-103">Cluster erhalten oder auflisten</span><span class="sxs-lookup"><span data-stu-id="97085-103">Get or list clusters</span></span>

## <span data-ttu-id="97085-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97085-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97085-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97085-105">DESCRIPTION</span></span>
<span data-ttu-id="97085-106">Erhalten oder Listencluster, Listencluster unter Ressourcengruppe, wenn "-ClusterName" nicht bereitgestellt wurde, Listencluster unter Abonnement, wenn "-ClusterName" und "ResourceGroupName" nicht bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="97085-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="97085-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97085-107">EXAMPLES</span></span>

### <span data-ttu-id="97085-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97085-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="97085-109">Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="97085-109">Get cluster</span></span>

## <span data-ttu-id="97085-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="97085-110">PARAMETERS</span></span>

### <span data-ttu-id="97085-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="97085-111">-ClusterName</span></span>
<span data-ttu-id="97085-112">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="97085-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97085-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97085-113">-DefaultProfile</span></span>
<span data-ttu-id="97085-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97085-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97085-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97085-115">-ResourceGroupName</span></span>
<span data-ttu-id="97085-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97085-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97085-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97085-117">CommonParameters</span></span>
<span data-ttu-id="97085-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97085-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97085-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97085-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97085-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97085-120">INPUTS</span></span>

### <span data-ttu-id="97085-121">System.String</span><span class="sxs-lookup"><span data-stu-id="97085-121">System.String</span></span>

## <span data-ttu-id="97085-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97085-122">OUTPUTS</span></span>

### <span data-ttu-id="97085-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="97085-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="97085-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="97085-124">NOTES</span></span>

## <span data-ttu-id="97085-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="97085-125">RELATED LINKS</span></span>
