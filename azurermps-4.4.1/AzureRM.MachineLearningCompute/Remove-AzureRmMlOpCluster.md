---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663313"
---
# <span data-ttu-id="9dcbe-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="9dcbe-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="9dcbe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9dcbe-102">SYNOPSIS</span></span>
<span data-ttu-id="9dcbe-103">Entfernt einen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dcbe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dcbe-104">SYNTAX</span></span>

### <span data-ttu-id="9dcbe-105">Entfernen eines Vorgangs Clusters aus Cmdlet-Eingabeparametern</span><span class="sxs-lookup"><span data-stu-id="9dcbe-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9dcbe-106">Entfernen eines Vorgangs Clusters aus einer OperationalizationCluster-Instanzen Definition</span><span class="sxs-lookup"><span data-stu-id="9dcbe-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9dcbe-107">Entfernen eines Vorgangs Clusters aus einer Azure Resouce-ID</span><span class="sxs-lookup"><span data-stu-id="9dcbe-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9dcbe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9dcbe-108">DESCRIPTION</span></span>
<span data-ttu-id="9dcbe-109">Entfernt einen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="9dcbe-110">Einige Ressourcen, die dem Cluster zugeordnet sind, werden möglicherweise nicht alle entfernt.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="9dcbe-111">Beispielsweise wird der Azure-Containerdienst entfernt, die zugehörigen VMS jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="9dcbe-112">Das Speicherkonto, die Container Registrierung und die Anwendungs Einsichten werden für Diagnoseinformationen nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="9dcbe-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9dcbe-113">EXAMPLES</span></span>

### <span data-ttu-id="9dcbe-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9dcbe-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="9dcbe-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9dcbe-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="9dcbe-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dcbe-116">PARAMETERS</span></span>

### <span data-ttu-id="9dcbe-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9dcbe-117">-InputObject</span></span>
<span data-ttu-id="9dcbe-118">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="9dcbe-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dcbe-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9dcbe-119">-Confirm</span></span>
<span data-ttu-id="9dcbe-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dcbe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9dcbe-121">-Name</span></span>
<span data-ttu-id="9dcbe-122">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dcbe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dcbe-123">-ResourceGroupName</span></span>
<span data-ttu-id="9dcbe-124">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dcbe-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9dcbe-125">-ResourceId</span></span>
<span data-ttu-id="9dcbe-126">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dcbe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dcbe-127">-WhatIf</span></span>
<span data-ttu-id="9dcbe-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dcbe-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9dcbe-129">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="9dcbe-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9dcbe-130">INPUTS</span></span>

### <span data-ttu-id="9dcbe-131">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="9dcbe-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="9dcbe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9dcbe-132">System.String</span></span>


## <span data-ttu-id="9dcbe-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9dcbe-133">OUTPUTS</span></span>

### <span data-ttu-id="9dcbe-134">System. void</span><span class="sxs-lookup"><span data-stu-id="9dcbe-134">System.Void</span></span>


## <span data-ttu-id="9dcbe-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9dcbe-135">NOTES</span></span>

## <span data-ttu-id="9dcbe-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9dcbe-136">RELATED LINKS</span></span>

