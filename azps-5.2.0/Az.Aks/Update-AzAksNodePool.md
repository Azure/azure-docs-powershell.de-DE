---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303691"
---
# <span data-ttu-id="21af5-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="21af5-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="21af5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21af5-102">SYNOPSIS</span></span>
<span data-ttu-id="21af5-103">Aktualisieren des Knotenpools in einem verwalteten Cluster</span><span class="sxs-lookup"><span data-stu-id="21af5-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="21af5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21af5-104">SYNTAX</span></span>

### <span data-ttu-id="21af5-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="21af5-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21af5-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21af5-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21af5-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21af5-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21af5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21af5-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21af5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21af5-109">DESCRIPTION</span></span>
<span data-ttu-id="21af5-110">Aktualisieren des Knotenpools in einem verwalteten Cluster</span><span class="sxs-lookup"><span data-stu-id="21af5-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="21af5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21af5-111">EXAMPLES</span></span>

### <span data-ttu-id="21af5-112">Ändern der minimun count für den angegebenen Knotenpool in 5</span><span class="sxs-lookup"><span data-stu-id="21af5-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="21af5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21af5-113">PARAMETERS</span></span>

### <span data-ttu-id="21af5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21af5-114">-AsJob</span></span>
<span data-ttu-id="21af5-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="21af5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21af5-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="21af5-116">-ClusterName</span></span>
<span data-ttu-id="21af5-117">Der Name der verwalteten Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="21af5-117">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21af5-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="21af5-118">-ClusterObject</span></span>
<span data-ttu-id="21af5-119">Das Clusterobjekt</span><span class="sxs-lookup"><span data-stu-id="21af5-119">The cluster object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21af5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21af5-120">-DefaultProfile</span></span>
<span data-ttu-id="21af5-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21af5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21af5-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="21af5-122">-EnableAutoScaling</span></span>
<span data-ttu-id="21af5-123">Aktivieren der automatischen Skalierung</span><span class="sxs-lookup"><span data-stu-id="21af5-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="21af5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="21af5-124">-Force</span></span>
<span data-ttu-id="21af5-125">Aktualisieren des Knotenpools ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="21af5-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="21af5-126">-ID</span><span class="sxs-lookup"><span data-stu-id="21af5-126">-Id</span></span>
<span data-ttu-id="21af5-127">ID eines Knotenpools im verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="21af5-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21af5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21af5-128">-InputObject</span></span>
<span data-ttu-id="21af5-129">Ein PSAgentPool-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="21af5-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21af5-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="21af5-130">-KubernetesVersion</span></span>
<span data-ttu-id="21af5-131">Die Version von Kubernetes, die zum Erstellen des Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21af5-131">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21af5-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="21af5-132">-MaxCount</span></span>
<span data-ttu-id="21af5-133">Maximale Anzahl von Knoten für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="21af5-133">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21af5-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="21af5-134">-MinCount</span></span>
<span data-ttu-id="21af5-135">Mindestanzahl von Knoten für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="21af5-135">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21af5-136">-Name</span><span class="sxs-lookup"><span data-stu-id="21af5-136">-Name</span></span>
<span data-ttu-id="21af5-137">Der Name des Knotenpools.</span><span class="sxs-lookup"><span data-stu-id="21af5-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21af5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21af5-138">-ResourceGroupName</span></span>
<span data-ttu-id="21af5-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21af5-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21af5-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21af5-140">-Confirm</span></span>
<span data-ttu-id="21af5-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21af5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21af5-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="21af5-142">-WhatIf</span></span>
<span data-ttu-id="21af5-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21af5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21af5-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21af5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21af5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21af5-145">CommonParameters</span></span>
<span data-ttu-id="21af5-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21af5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21af5-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21af5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21af5-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21af5-148">INPUTS</span></span>

### <span data-ttu-id="21af5-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="21af5-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="21af5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="21af5-150">System.String</span></span>

## <span data-ttu-id="21af5-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21af5-151">OUTPUTS</span></span>

### <span data-ttu-id="21af5-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="21af5-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="21af5-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="21af5-153">NOTES</span></span>

## <span data-ttu-id="21af5-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="21af5-154">RELATED LINKS</span></span>
