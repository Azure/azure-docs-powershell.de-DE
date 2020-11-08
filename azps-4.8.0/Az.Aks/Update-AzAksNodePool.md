---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165382"
---
# <span data-ttu-id="3cf61-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="3cf61-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="3cf61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cf61-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf61-103">Aktualisieren des Knoten Pools in einem verwalteten Cluster</span><span class="sxs-lookup"><span data-stu-id="3cf61-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="3cf61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cf61-104">SYNTAX</span></span>

### <span data-ttu-id="3cf61-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cf61-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf61-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf61-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf61-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf61-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf61-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf61-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cf61-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cf61-109">DESCRIPTION</span></span>
<span data-ttu-id="3cf61-110">Aktualisieren des Knoten Pools in einem verwalteten Cluster</span><span class="sxs-lookup"><span data-stu-id="3cf61-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="3cf61-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cf61-111">EXAMPLES</span></span>

### <span data-ttu-id="3cf61-112">Ändern der Mindestanzahl für den angegebenen Knoten Pool in 5</span><span class="sxs-lookup"><span data-stu-id="3cf61-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="3cf61-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cf61-113">PARAMETERS</span></span>

### <span data-ttu-id="3cf61-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cf61-114">-AsJob</span></span>
<span data-ttu-id="3cf61-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3cf61-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cf61-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="3cf61-116">-ClusterName</span></span>
<span data-ttu-id="3cf61-117">Der Name der verwalteten Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="3cf61-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="3cf61-118">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="3cf61-118">-ClusterObject</span></span>
<span data-ttu-id="3cf61-119">Das Clusterobjekt</span><span class="sxs-lookup"><span data-stu-id="3cf61-119">The cluster object</span></span>

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

### <span data-ttu-id="3cf61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf61-120">-DefaultProfile</span></span>
<span data-ttu-id="3cf61-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cf61-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf61-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="3cf61-122">-EnableAutoScaling</span></span>
<span data-ttu-id="3cf61-123">Ob die automatische Skalierung aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="3cf61-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="3cf61-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3cf61-124">-Force</span></span>
<span data-ttu-id="3cf61-125">Aktualisieren des Knoten Pools ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="3cf61-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="3cf61-126">-ID</span><span class="sxs-lookup"><span data-stu-id="3cf61-126">-Id</span></span>
<span data-ttu-id="3cf61-127">ID eines Knoten Pools in verwaltetem Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="3cf61-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="3cf61-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3cf61-128">-InputObject</span></span>
<span data-ttu-id="3cf61-129">Ein PSAgentPool-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3cf61-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="3cf61-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="3cf61-130">-KubernetesVersion</span></span>
<span data-ttu-id="3cf61-131">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cf61-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="3cf61-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3cf61-132">-MaxCount</span></span>
<span data-ttu-id="3cf61-133">Maximale Anzahl von Knoten für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="3cf61-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="3cf61-134">-"Mincount</span><span class="sxs-lookup"><span data-stu-id="3cf61-134">-MinCount</span></span>
<span data-ttu-id="3cf61-135">Minimale Anzahl von Knoten für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="3cf61-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="3cf61-136">-Name</span><span class="sxs-lookup"><span data-stu-id="3cf61-136">-Name</span></span>
<span data-ttu-id="3cf61-137">Der Name des Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="3cf61-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="3cf61-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf61-138">-ResourceGroupName</span></span>
<span data-ttu-id="3cf61-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3cf61-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="3cf61-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cf61-140">-Confirm</span></span>
<span data-ttu-id="3cf61-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cf61-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf61-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf61-142">-WhatIf</span></span>
<span data-ttu-id="3cf61-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cf61-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf61-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cf61-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf61-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf61-145">CommonParameters</span></span>
<span data-ttu-id="3cf61-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf61-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf61-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cf61-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf61-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cf61-148">INPUTS</span></span>

### <span data-ttu-id="3cf61-149">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="3cf61-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="3cf61-150">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf61-150">System.String</span></span>

## <span data-ttu-id="3cf61-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cf61-151">OUTPUTS</span></span>

### <span data-ttu-id="3cf61-152">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="3cf61-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="3cf61-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cf61-153">NOTES</span></span>

## <span data-ttu-id="3cf61-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cf61-154">RELATED LINKS</span></span>
