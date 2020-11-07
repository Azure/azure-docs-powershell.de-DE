---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
ms.openlocfilehash: de297c94be69773d07efedfae42ccc029fc13414
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650664"
---
# <span data-ttu-id="bc92f-101">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bc92f-101">Remove-AzMlOpCluster</span></span>

## <span data-ttu-id="bc92f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc92f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc92f-103">Entfernt einen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="bc92f-103">Removes an operationalization cluster.</span></span>

## <span data-ttu-id="bc92f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc92f-104">SYNTAX</span></span>

### <span data-ttu-id="bc92f-105">RemoveByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc92f-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc92f-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="bc92f-106">RemoveByInputObject</span></span>
```
Remove-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc92f-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc92f-107">RemoveByResourceId</span></span>
```
Remove-AzMlOpCluster -ResourceId <String> [-IncludeAllResources] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc92f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc92f-108">DESCRIPTION</span></span>
<span data-ttu-id="bc92f-109">Entfernt einen Operations Cluster.</span><span class="sxs-lookup"><span data-stu-id="bc92f-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="bc92f-110">Einige Ressourcen, die dem Cluster zugeordnet sind, werden möglicherweise nicht alle entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc92f-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="bc92f-111">Beispielsweise wird der Azure-Containerdienst entfernt, die zugehörigen VMS jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="bc92f-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="bc92f-112">Das Speicherkonto, die Container Registrierung und die Anwendungs Einsichten werden für Diagnoseinformationen nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc92f-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="bc92f-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc92f-113">EXAMPLES</span></span>

### <span data-ttu-id="bc92f-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc92f-114">Example 1</span></span>
```
PS C:\> Remove-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="bc92f-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bc92f-115">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzMlOpCluster
```

## <span data-ttu-id="bc92f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc92f-116">PARAMETERS</span></span>

### <span data-ttu-id="bc92f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc92f-117">-DefaultProfile</span></span>
<span data-ttu-id="bc92f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc92f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc92f-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="bc92f-119">-IncludeAllResources</span></span>
<span data-ttu-id="bc92f-120">Entfernt alle Ressourcen, die mit dem Cluster erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bc92f-120">Removes all resources that were created with the cluster.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc92f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc92f-121">-InputObject</span></span>
<span data-ttu-id="bc92f-122">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="bc92f-122">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc92f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bc92f-123">-Name</span></span>
<span data-ttu-id="bc92f-124">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="bc92f-124">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc92f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc92f-125">-ResourceGroupName</span></span>
<span data-ttu-id="bc92f-126">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="bc92f-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc92f-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bc92f-127">-ResourceId</span></span>
<span data-ttu-id="bc92f-128">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="bc92f-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc92f-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc92f-129">-Confirm</span></span>
<span data-ttu-id="bc92f-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc92f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc92f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc92f-131">-WhatIf</span></span>
<span data-ttu-id="bc92f-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc92f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc92f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc92f-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc92f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc92f-134">CommonParameters</span></span>
<span data-ttu-id="bc92f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc92f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc92f-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc92f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc92f-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc92f-137">INPUTS</span></span>

### <span data-ttu-id="bc92f-138">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="bc92f-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="bc92f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bc92f-139">System.String</span></span>

## <span data-ttu-id="bc92f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc92f-140">OUTPUTS</span></span>

### <span data-ttu-id="bc92f-141">System. void</span><span class="sxs-lookup"><span data-stu-id="bc92f-141">System.Void</span></span>

## <span data-ttu-id="bc92f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc92f-142">NOTES</span></span>

## <span data-ttu-id="bc92f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc92f-143">RELATED LINKS</span></span>
