---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300298"
---
# <span data-ttu-id="76ad4-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="76ad4-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="76ad4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="76ad4-103">Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="76ad4-103">Create cluster</span></span>

## <span data-ttu-id="76ad4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76ad4-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76ad4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76ad4-105">DESCRIPTION</span></span>

<span data-ttu-id="76ad4-106">Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="76ad4-106">Create cluster</span></span>

## <span data-ttu-id="76ad4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76ad4-107">EXAMPLES</span></span>

### <span data-ttu-id="76ad4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76ad4-108">Example 1</span></span>
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

<span data-ttu-id="76ad4-109">Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="76ad4-109">Create cluster</span></span>

## <span data-ttu-id="76ad4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="76ad4-110">PARAMETERS</span></span>

### <span data-ttu-id="76ad4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76ad4-111">-AsJob</span></span>
<span data-ttu-id="76ad4-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="76ad4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76ad4-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="76ad4-113">-ClusterName</span></span>
<span data-ttu-id="76ad4-114">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="76ad4-114">The cluster name.</span></span>

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

### <span data-ttu-id="76ad4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ad4-115">-DefaultProfile</span></span>
<span data-ttu-id="76ad4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76ad4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76ad4-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="76ad4-117">-IdentityType</span></span>
<span data-ttu-id="76ad4-118">der Identity-Typ, Value kann "SystemAssigned", "None" sein.</span><span class="sxs-lookup"><span data-stu-id="76ad4-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

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

### <span data-ttu-id="76ad4-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="76ad4-119">-Location</span></span>
<span data-ttu-id="76ad4-120">Die geografische Region, in der der Cluster bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="76ad4-120">The geographic region that the cluster will be deployed.</span></span>

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

### <span data-ttu-id="76ad4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76ad4-121">-ResourceGroupName</span></span>
<span data-ttu-id="76ad4-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76ad4-122">The resource group name.</span></span>

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

### <span data-ttu-id="76ad4-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="76ad4-123">-SkuCapacity</span></span>
<span data-ttu-id="76ad4-124">SKU-Kapazität, der Wert muss ein Vielfaches von 100 und im Bereich von 1000-2000 sein.</span><span class="sxs-lookup"><span data-stu-id="76ad4-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

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

### <span data-ttu-id="76ad4-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="76ad4-125">-SkuName</span></span>
<span data-ttu-id="76ad4-126">SKU-Name, kann jetzt nur "CapacityReservation" sein</span><span class="sxs-lookup"><span data-stu-id="76ad4-126">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="76ad4-127">-Tags</span><span class="sxs-lookup"><span data-stu-id="76ad4-127">-Tags</span></span>
<span data-ttu-id="76ad4-128">Tags des Clusters</span><span class="sxs-lookup"><span data-stu-id="76ad4-128">Tags of the cluster</span></span>

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

### <span data-ttu-id="76ad4-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76ad4-129">-Confirm</span></span>
<span data-ttu-id="76ad4-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76ad4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76ad4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76ad4-131">-WhatIf</span></span>
<span data-ttu-id="76ad4-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76ad4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76ad4-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76ad4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76ad4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ad4-134">CommonParameters</span></span>
<span data-ttu-id="76ad4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ad4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ad4-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76ad4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ad4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76ad4-137">INPUTS</span></span>

### <span data-ttu-id="76ad4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="76ad4-138">System.String</span></span>

## <span data-ttu-id="76ad4-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76ad4-139">OUTPUTS</span></span>

### <span data-ttu-id="76ad4-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="76ad4-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="76ad4-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="76ad4-141">NOTES</span></span>

## <span data-ttu-id="76ad4-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76ad4-142">RELATED LINKS</span></span>
