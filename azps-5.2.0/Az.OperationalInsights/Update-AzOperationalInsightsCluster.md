---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364760"
---
# <span data-ttu-id="1821b-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="1821b-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="1821b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1821b-102">SYNOPSIS</span></span>
<span data-ttu-id="1821b-103">Updatecluster</span><span class="sxs-lookup"><span data-stu-id="1821b-103">update cluster</span></span>

## <span data-ttu-id="1821b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1821b-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1821b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1821b-105">DESCRIPTION</span></span>
<span data-ttu-id="1821b-106">Updatecluster</span><span class="sxs-lookup"><span data-stu-id="1821b-106">update cluster</span></span>

## <span data-ttu-id="1821b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1821b-107">EXAMPLES</span></span>

### <span data-ttu-id="1821b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1821b-108">Example 1</span></span>
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

<span data-ttu-id="1821b-109">Updatecluster mit Schlüsseltresoreigenschaften und SKU</span><span class="sxs-lookup"><span data-stu-id="1821b-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="1821b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1821b-110">PARAMETERS</span></span>

### <span data-ttu-id="1821b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1821b-111">-AsJob</span></span>
<span data-ttu-id="1821b-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1821b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1821b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1821b-113">-ClusterName</span></span>
<span data-ttu-id="1821b-114">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="1821b-114">The cluster name.</span></span>

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

### <span data-ttu-id="1821b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1821b-115">-DefaultProfile</span></span>
<span data-ttu-id="1821b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1821b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1821b-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1821b-117">-KeyName</span></span>
<span data-ttu-id="1821b-118">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="1821b-118">Key Name</span></span>

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

### <span data-ttu-id="1821b-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="1821b-119">-KeyVaultUri</span></span>
<span data-ttu-id="1821b-120">Schlüsseltresor-URI, "Löschschutz" und "Weiches Löschen" müssen für diesen Keyvault aktiviert sein</span><span class="sxs-lookup"><span data-stu-id="1821b-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="1821b-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="1821b-121">-KeyVersion</span></span>
<span data-ttu-id="1821b-122">Schlüsselversion</span><span class="sxs-lookup"><span data-stu-id="1821b-122">Key Version</span></span>

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

### <span data-ttu-id="1821b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1821b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1821b-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1821b-124">The resource group name.</span></span>

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

### <span data-ttu-id="1821b-125">-Sku1</span><span class="sxs-lookup"><span data-stu-id="1821b-125">-SkuCapacity</span></span>
<span data-ttu-id="1821b-126">SKU-Kapazität</span><span class="sxs-lookup"><span data-stu-id="1821b-126">Sku Capacity</span></span>

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

### <span data-ttu-id="1821b-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1821b-127">-SkuName</span></span>
<span data-ttu-id="1821b-128">"SKU-Name" darf jetzt nur noch "CapacityReservation" sein.</span><span class="sxs-lookup"><span data-stu-id="1821b-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="1821b-129">-Tags</span><span class="sxs-lookup"><span data-stu-id="1821b-129">-Tags</span></span>
<span data-ttu-id="1821b-130">Tags des Cluster</span><span class="sxs-lookup"><span data-stu-id="1821b-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="1821b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1821b-131">-Confirm</span></span>
<span data-ttu-id="1821b-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1821b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1821b-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1821b-133">-WhatIf</span></span>
<span data-ttu-id="1821b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1821b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1821b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1821b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1821b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1821b-136">CommonParameters</span></span>
<span data-ttu-id="1821b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1821b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1821b-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1821b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1821b-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1821b-139">INPUTS</span></span>

### <span data-ttu-id="1821b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1821b-140">System.String</span></span>

## <span data-ttu-id="1821b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1821b-141">OUTPUTS</span></span>

### <span data-ttu-id="1821b-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="1821b-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="1821b-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1821b-143">NOTES</span></span>

## <span data-ttu-id="1821b-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1821b-144">RELATED LINKS</span></span>
