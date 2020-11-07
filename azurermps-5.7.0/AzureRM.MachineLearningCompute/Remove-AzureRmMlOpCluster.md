---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 9836856ffd663939de8ca0e28635d81785c9c898
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93665414"
---
# <span data-ttu-id="300e2-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="300e2-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="300e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="300e2-102">SYNOPSIS</span></span>
<span data-ttu-id="300e2-103">Entfernt einen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="300e2-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="300e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="300e2-104">SYNTAX</span></span>

### <span data-ttu-id="300e2-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="300e2-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="300e2-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="300e2-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="300e2-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="300e2-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeAllResources] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="300e2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="300e2-108">DESCRIPTION</span></span>
<span data-ttu-id="300e2-109">Entfernt einen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="300e2-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="300e2-110">Einige Ressourcen, die dem Cluster zugeordnet sind, werden möglicherweise nicht alle entfernt.</span><span class="sxs-lookup"><span data-stu-id="300e2-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="300e2-111">Beispielsweise wird der Azure-Containerdienst entfernt, die zugehörigen VMS jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="300e2-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="300e2-112">Das Speicherkonto, die Container Registrierung und die Anwendungs Einsichten werden für Diagnoseinformationen nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="300e2-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="300e2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="300e2-113">EXAMPLES</span></span>

### <span data-ttu-id="300e2-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="300e2-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="300e2-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="300e2-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="300e2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="300e2-116">PARAMETERS</span></span>

### <span data-ttu-id="300e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="300e2-117">-DefaultProfile</span></span>
<span data-ttu-id="300e2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="300e2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e2-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="300e2-119">-IncludeAllResources</span></span>
<span data-ttu-id="300e2-120">Entfernt alle Ressourcen, die mit dem Cluster erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="300e2-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="300e2-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="300e2-121">-InputObject</span></span>
<span data-ttu-id="300e2-122">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="300e2-122">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="300e2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="300e2-123">-Name</span></span>
<span data-ttu-id="300e2-124">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="300e2-124">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="300e2-125">-ResourceGroupName</span></span>
<span data-ttu-id="300e2-126">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="300e2-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e2-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="300e2-127">-ResourceId</span></span>
<span data-ttu-id="300e2-128">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="300e2-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="300e2-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="300e2-129">-Confirm</span></span>
<span data-ttu-id="300e2-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="300e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="300e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="300e2-131">-WhatIf</span></span>
<span data-ttu-id="300e2-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="300e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="300e2-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="300e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="300e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="300e2-134">CommonParameters</span></span>
<span data-ttu-id="300e2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="300e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="300e2-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="300e2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="300e2-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="300e2-137">INPUTS</span></span>

### <span data-ttu-id="300e2-138">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="300e2-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="300e2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="300e2-139">System.String</span></span>

## <span data-ttu-id="300e2-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="300e2-140">OUTPUTS</span></span>

### <span data-ttu-id="300e2-141">System. void</span><span class="sxs-lookup"><span data-stu-id="300e2-141">System.Void</span></span>

## <span data-ttu-id="300e2-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="300e2-142">NOTES</span></span>

## <span data-ttu-id="300e2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="300e2-143">RELATED LINKS</span></span>

