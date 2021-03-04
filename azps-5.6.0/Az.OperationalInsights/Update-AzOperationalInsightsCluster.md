---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: f76ca0db3f4203bf1906c29c32c1973ea098789c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937803"
---
# <span data-ttu-id="6af74-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="6af74-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="6af74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6af74-102">SYNOPSIS</span></span>
<span data-ttu-id="6af74-103">Updatecluster</span><span class="sxs-lookup"><span data-stu-id="6af74-103">update cluster</span></span>

## <span data-ttu-id="6af74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6af74-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6af74-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6af74-105">DESCRIPTION</span></span>
<span data-ttu-id="6af74-106">Updatecluster</span><span class="sxs-lookup"><span data-stu-id="6af74-106">update cluster</span></span>

## <span data-ttu-id="6af74-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6af74-107">EXAMPLES</span></span>

### <span data-ttu-id="6af74-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6af74-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="6af74-109">Updatecluster mit Schlüsseltresoreigenschaften und Sku</span><span class="sxs-lookup"><span data-stu-id="6af74-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="6af74-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6af74-110">PARAMETERS</span></span>

### <span data-ttu-id="6af74-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6af74-111">-AsJob</span></span>
<span data-ttu-id="6af74-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6af74-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6af74-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6af74-113">-ClusterName</span></span>
<span data-ttu-id="6af74-114">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="6af74-114">The cluster name.</span></span>

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

### <span data-ttu-id="6af74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af74-115">-DefaultProfile</span></span>
<span data-ttu-id="6af74-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6af74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6af74-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6af74-117">-KeyName</span></span>
<span data-ttu-id="6af74-118">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="6af74-118">Key Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af74-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="6af74-119">-KeyVaultUri</span></span>
<span data-ttu-id="6af74-120">Key Vault Uri, "Purge Protection" und "Soft Delete" müssen für diesen Keyvault aktiviert werden</span><span class="sxs-lookup"><span data-stu-id="6af74-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af74-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="6af74-121">-KeyVersion</span></span>
<span data-ttu-id="6af74-122">Schlüsselversion</span><span class="sxs-lookup"><span data-stu-id="6af74-122">Key Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af74-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6af74-123">-ResourceGroupName</span></span>
<span data-ttu-id="6af74-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6af74-124">The resource group name.</span></span>

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

### <span data-ttu-id="6af74-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6af74-125">-SkuCapacity</span></span>
<span data-ttu-id="6af74-126">Sku-Kapazität</span><span class="sxs-lookup"><span data-stu-id="6af74-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af74-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6af74-127">-SkuName</span></span>
<span data-ttu-id="6af74-128">Sku-Name kann jetzt nur "CapacityReservation" sein</span><span class="sxs-lookup"><span data-stu-id="6af74-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="6af74-129">-Tags</span><span class="sxs-lookup"><span data-stu-id="6af74-129">-Tags</span></span>
<span data-ttu-id="6af74-130">Tags des Clusters</span><span class="sxs-lookup"><span data-stu-id="6af74-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="6af74-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6af74-131">-Confirm</span></span>
<span data-ttu-id="6af74-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6af74-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6af74-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6af74-133">-WhatIf</span></span>
<span data-ttu-id="6af74-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6af74-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6af74-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6af74-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6af74-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af74-136">CommonParameters</span></span>
<span data-ttu-id="6af74-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af74-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af74-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6af74-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af74-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6af74-139">INPUTS</span></span>

### <span data-ttu-id="6af74-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6af74-140">System.String</span></span>

## <span data-ttu-id="6af74-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6af74-141">OUTPUTS</span></span>

### <span data-ttu-id="6af74-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="6af74-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="6af74-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6af74-143">NOTES</span></span>

## <span data-ttu-id="6af74-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6af74-144">RELATED LINKS</span></span>
