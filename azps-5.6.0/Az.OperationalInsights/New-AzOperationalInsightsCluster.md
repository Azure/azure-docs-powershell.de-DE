---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: c34bb862d3928e6dbbaa55a9660c4868e38941b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948512"
---
# <span data-ttu-id="6398a-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="6398a-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="6398a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6398a-102">SYNOPSIS</span></span>
<span data-ttu-id="6398a-103">Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="6398a-103">Create cluster</span></span>

## <span data-ttu-id="6398a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6398a-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6398a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6398a-105">DESCRIPTION</span></span>

<span data-ttu-id="6398a-106">Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="6398a-106">Create cluster</span></span>

## <span data-ttu-id="6398a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6398a-107">EXAMPLES</span></span>

### <span data-ttu-id="6398a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6398a-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="6398a-109">Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="6398a-109">Create cluster</span></span>

## <span data-ttu-id="6398a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6398a-110">PARAMETERS</span></span>

### <span data-ttu-id="6398a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6398a-111">-AsJob</span></span>
<span data-ttu-id="6398a-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6398a-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6398a-113">-ClusterName</span></span>
<span data-ttu-id="6398a-114">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="6398a-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6398a-115">-DefaultProfile</span></span>
<span data-ttu-id="6398a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6398a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6398a-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6398a-117">-IdentityType</span></span>
<span data-ttu-id="6398a-118">der Identitätstyp, kann der Wert "SystemAssigned", "None" sein.</span><span class="sxs-lookup"><span data-stu-id="6398a-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="6398a-119">-Location</span></span>
<span data-ttu-id="6398a-120">Die geografische Region, in der der Cluster bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6398a-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6398a-121">-ResourceGroupName</span></span>
<span data-ttu-id="6398a-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6398a-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6398a-123">-SkuCapacity</span></span>
<span data-ttu-id="6398a-124">Sku Kapazität, Wert muss ein Vielfaches von 100 und im Bereich von 1000-2000 sein.</span><span class="sxs-lookup"><span data-stu-id="6398a-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6398a-125">-SkuName</span></span>
<span data-ttu-id="6398a-126">Sku-Name kann jetzt nur "CapacityReservation" sein</span><span class="sxs-lookup"><span data-stu-id="6398a-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-127">-Tags</span><span class="sxs-lookup"><span data-stu-id="6398a-127">-Tags</span></span>
<span data-ttu-id="6398a-128">Tags des Clusters</span><span class="sxs-lookup"><span data-stu-id="6398a-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6398a-129">-Confirm</span></span>
<span data-ttu-id="6398a-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6398a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6398a-131">-WhatIf</span></span>
<span data-ttu-id="6398a-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6398a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6398a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6398a-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6398a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6398a-134">CommonParameters</span></span>
<span data-ttu-id="6398a-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6398a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6398a-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6398a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6398a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6398a-137">INPUTS</span></span>

### <span data-ttu-id="6398a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6398a-138">System.String</span></span>

## <span data-ttu-id="6398a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6398a-139">OUTPUTS</span></span>

### <span data-ttu-id="6398a-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="6398a-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="6398a-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6398a-141">NOTES</span></span>

## <span data-ttu-id="6398a-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6398a-142">RELATED LINKS</span></span>
