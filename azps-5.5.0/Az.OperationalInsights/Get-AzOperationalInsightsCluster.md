---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158716"
---
# <span data-ttu-id="01dc8-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="01dc8-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="01dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="01dc8-103">Cluster erhalten oder auflisten</span><span class="sxs-lookup"><span data-stu-id="01dc8-103">Get or list clusters</span></span>

## <span data-ttu-id="01dc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01dc8-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01dc8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="01dc8-106">Cluster erhalten oder auflisten, Cluster unter Ressourcengruppe, wenn "-ClusterName" nicht bereitgestellt wurde, Listenclusters unter Abonnement, wenn "-ClusterName" und "ResourceGroupName" nicht bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="01dc8-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="01dc8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01dc8-107">EXAMPLES</span></span>

### <span data-ttu-id="01dc8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01dc8-108">Example 1</span></span>
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

<span data-ttu-id="01dc8-109">Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="01dc8-109">Get cluster</span></span>

## <span data-ttu-id="01dc8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01dc8-110">PARAMETERS</span></span>

### <span data-ttu-id="01dc8-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="01dc8-111">-ClusterName</span></span>
<span data-ttu-id="01dc8-112">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="01dc8-112">The cluster name.</span></span>

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

### <span data-ttu-id="01dc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01dc8-113">-DefaultProfile</span></span>
<span data-ttu-id="01dc8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01dc8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01dc8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01dc8-115">-ResourceGroupName</span></span>
<span data-ttu-id="01dc8-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01dc8-116">The resource group name.</span></span>

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

### <span data-ttu-id="01dc8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01dc8-117">CommonParameters</span></span>
<span data-ttu-id="01dc8-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01dc8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01dc8-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01dc8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01dc8-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01dc8-120">INPUTS</span></span>

### <span data-ttu-id="01dc8-121">System.String</span><span class="sxs-lookup"><span data-stu-id="01dc8-121">System.String</span></span>

## <span data-ttu-id="01dc8-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01dc8-122">OUTPUTS</span></span>

### <span data-ttu-id="01dc8-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="01dc8-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="01dc8-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01dc8-124">NOTES</span></span>

## <span data-ttu-id="01dc8-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01dc8-125">RELATED LINKS</span></span>
