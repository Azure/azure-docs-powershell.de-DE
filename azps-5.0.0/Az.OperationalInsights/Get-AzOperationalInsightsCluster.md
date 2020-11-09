---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303460"
---
# <span data-ttu-id="689a4-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="689a4-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="689a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="689a4-102">SYNOPSIS</span></span>
<span data-ttu-id="689a4-103">Abrufen oder Auflisten von Clustern</span><span class="sxs-lookup"><span data-stu-id="689a4-103">Get or list clusters</span></span>

## <span data-ttu-id="689a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="689a4-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="689a4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="689a4-105">DESCRIPTION</span></span>
<span data-ttu-id="689a4-106">Abrufen oder Auflisten von Clustern, Auflisten von Clustern unter Ressourcengruppe, wenn "-Clustername" nicht angegeben wurde, Listen Cluster unter "Abonnement", wenn "-Clustername" und "ResourceGroupName" nicht bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="689a4-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="689a4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="689a4-107">EXAMPLES</span></span>

### <span data-ttu-id="689a4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="689a4-108">Example 1</span></span>
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

<span data-ttu-id="689a4-109">Cluster abrufen</span><span class="sxs-lookup"><span data-stu-id="689a4-109">Get cluster</span></span>

## <span data-ttu-id="689a4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="689a4-110">PARAMETERS</span></span>

### <span data-ttu-id="689a4-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="689a4-111">-ClusterName</span></span>
<span data-ttu-id="689a4-112">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="689a4-112">The cluster name.</span></span>

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

### <span data-ttu-id="689a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689a4-113">-DefaultProfile</span></span>
<span data-ttu-id="689a4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="689a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="689a4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="689a4-115">-ResourceGroupName</span></span>
<span data-ttu-id="689a4-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="689a4-116">The resource group name.</span></span>

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

### <span data-ttu-id="689a4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689a4-117">CommonParameters</span></span>
<span data-ttu-id="689a4-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="689a4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689a4-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="689a4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689a4-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="689a4-120">INPUTS</span></span>

### <span data-ttu-id="689a4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="689a4-121">System.String</span></span>

## <span data-ttu-id="689a4-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="689a4-122">OUTPUTS</span></span>

### <span data-ttu-id="689a4-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="689a4-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="689a4-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="689a4-124">NOTES</span></span>

## <span data-ttu-id="689a4-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="689a4-125">RELATED LINKS</span></span>
