---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177777"
---
# <span data-ttu-id="c8cc4-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="c8cc4-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="c8cc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="c8cc4-103">Cluster aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c8cc4-103">update cluster</span></span>

## <span data-ttu-id="c8cc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8cc4-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8cc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="c8cc4-106">Cluster aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c8cc4-106">update cluster</span></span>

## <span data-ttu-id="c8cc4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8cc4-107">EXAMPLES</span></span>

### <span data-ttu-id="c8cc4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c8cc4-108">Example 1</span></span>
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

<span data-ttu-id="c8cc4-109">Aktualisieren des Clusters mit wichtigen Vault-Eigenschaften und SKU</span><span class="sxs-lookup"><span data-stu-id="c8cc4-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="c8cc4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8cc4-110">PARAMETERS</span></span>

### <span data-ttu-id="c8cc4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8cc4-111">-AsJob</span></span>
<span data-ttu-id="c8cc4-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c8cc4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8cc4-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c8cc4-113">-ClusterName</span></span>
<span data-ttu-id="c8cc4-114">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="c8cc4-114">The cluster name.</span></span>

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

### <span data-ttu-id="c8cc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8cc4-115">-DefaultProfile</span></span>
<span data-ttu-id="c8cc4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8cc4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8cc4-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c8cc4-117">-KeyName</span></span>
<span data-ttu-id="c8cc4-118">Schlüssel Name</span><span class="sxs-lookup"><span data-stu-id="c8cc4-118">Key Name</span></span>

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

### <span data-ttu-id="c8cc4-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c8cc4-119">-KeyVaultUri</span></span>
<span data-ttu-id="c8cc4-120">Schlüsseltresor-URI, "Säuberungs Schutz" und "Soft Delete" müssen für diesen keyvault aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="c8cc4-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="c8cc4-121">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="c8cc4-121">-KeyVersion</span></span>
<span data-ttu-id="c8cc4-122">Schlüssel Version</span><span class="sxs-lookup"><span data-stu-id="c8cc4-122">Key Version</span></span>

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

### <span data-ttu-id="c8cc4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8cc4-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8cc4-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c8cc4-124">The resource group name.</span></span>

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

### <span data-ttu-id="c8cc4-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c8cc4-125">-SkuCapacity</span></span>
<span data-ttu-id="c8cc4-126">SKU-Kapazität</span><span class="sxs-lookup"><span data-stu-id="c8cc4-126">Sku Capacity</span></span>

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

### <span data-ttu-id="c8cc4-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c8cc4-127">-SkuName</span></span>
<span data-ttu-id="c8cc4-128">SKU-Name, kann jetzt nur "CapacityReservation" sein</span><span class="sxs-lookup"><span data-stu-id="c8cc4-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="c8cc4-129">-Tags</span><span class="sxs-lookup"><span data-stu-id="c8cc4-129">-Tags</span></span>
<span data-ttu-id="c8cc4-130">Tags des Clusters</span><span class="sxs-lookup"><span data-stu-id="c8cc4-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="c8cc4-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8cc4-131">-Confirm</span></span>
<span data-ttu-id="c8cc4-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8cc4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8cc4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8cc4-133">-WhatIf</span></span>
<span data-ttu-id="c8cc4-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8cc4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8cc4-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8cc4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8cc4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8cc4-136">CommonParameters</span></span>
<span data-ttu-id="c8cc4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8cc4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8cc4-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8cc4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8cc4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8cc4-139">INPUTS</span></span>

### <span data-ttu-id="c8cc4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c8cc4-140">System.String</span></span>

## <span data-ttu-id="c8cc4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8cc4-141">OUTPUTS</span></span>

### <span data-ttu-id="c8cc4-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="c8cc4-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="c8cc4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8cc4-143">NOTES</span></span>

## <span data-ttu-id="c8cc4-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8cc4-144">RELATED LINKS</span></span>
