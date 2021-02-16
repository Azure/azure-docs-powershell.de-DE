---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150697"
---
# <span data-ttu-id="7cbdf-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="7cbdf-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="7cbdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cbdf-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbdf-103">Entfernen Sie den Knotentyp oder bestimmte Knoten innerhalb des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="7cbdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cbdf-104">SYNTAX</span></span>

### <span data-ttu-id="7cbdf-105">DeleteNodeTypeByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="7cbdf-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cbdf-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="7cbdf-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cbdf-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="7cbdf-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cbdf-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="7cbdf-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cbdf-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="7cbdf-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cbdf-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="7cbdf-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cbdf-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cbdf-111">DESCRIPTION</span></span>
<span data-ttu-id="7cbdf-112">Entfernen Sie den Knotentyp oder bestimmte Knoten innerhalb des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="7cbdf-113">Wenn der Paremter "-NodeName" verwendet wird, werden nur angegebene Knoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="7cbdf-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7cbdf-114">EXAMPLES</span></span>

### <span data-ttu-id="7cbdf-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7cbdf-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="7cbdf-116">Knotentyp entfernen.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-116">Remove node type.</span></span>

### <span data-ttu-id="7cbdf-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7cbdf-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="7cbdf-118">Entfernen des Knotentyps mit Piping.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="7cbdf-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7cbdf-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="7cbdf-120">Entfernen Sie zwei Knoten aus dem Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="7cbdf-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="7cbdf-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="7cbdf-122">Entfernen Sie zwei Knoten aus dem Knotentyp mit Piping.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="7cbdf-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cbdf-123">PARAMETERS</span></span>

### <span data-ttu-id="7cbdf-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cbdf-124">-AsJob</span></span>
<span data-ttu-id="7cbdf-125">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7cbdf-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7cbdf-126">-ClusterName</span></span>
<span data-ttu-id="7cbdf-127">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbdf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbdf-128">-DefaultProfile</span></span>
<span data-ttu-id="7cbdf-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cbdf-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="7cbdf-130">-ForceRemoveNode</span></span>
<span data-ttu-id="7cbdf-131">Wenn Sie dieses Flag verwenden, wird das Entfernen auch dann erzwingen, wenn das Service Fabric die Knoten nicht deaktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="7cbdf-132">Seien Sie vorsichtig, da dies zu Datenverlust führen kann, wenn zustandsbehaftete Workloads für die Knoten ausgeführt werden, oder den Cluster nach dem Opeario nicht genügend Startknoten enthalten.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbdf-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cbdf-133">-InputObject</span></span>
<span data-ttu-id="7cbdf-134">Knotentypressource</span><span class="sxs-lookup"><span data-stu-id="7cbdf-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbdf-135">-Name</span><span class="sxs-lookup"><span data-stu-id="7cbdf-135">-Name</span></span>
<span data-ttu-id="7cbdf-136">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbdf-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="7cbdf-137">-NodeName</span></span>
<span data-ttu-id="7cbdf-138">Liste der Knotennamen für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbdf-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cbdf-139">-PassThru</span></span>
<span data-ttu-id="7cbdf-140">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="7cbdf-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7cbdf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbdf-141">-ResourceGroupName</span></span>
<span data-ttu-id="7cbdf-142">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbdf-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cbdf-143">-ResourceId</span></span>
<span data-ttu-id="7cbdf-144">Ressourcen-ID des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="7cbdf-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbdf-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cbdf-145">-Confirm</span></span>
<span data-ttu-id="7cbdf-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cbdf-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7cbdf-147">-WhatIf</span></span>
<span data-ttu-id="7cbdf-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cbdf-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cbdf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbdf-150">CommonParameters</span></span>
<span data-ttu-id="7cbdf-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cbdf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbdf-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cbdf-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbdf-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7cbdf-153">INPUTS</span></span>

### <span data-ttu-id="7cbdf-154">System.String</span><span class="sxs-lookup"><span data-stu-id="7cbdf-154">System.String</span></span>

## <span data-ttu-id="7cbdf-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7cbdf-155">OUTPUTS</span></span>

### <span data-ttu-id="7cbdf-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7cbdf-156">System.Boolean</span></span>

## <span data-ttu-id="7cbdf-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7cbdf-157">NOTES</span></span>

## <span data-ttu-id="7cbdf-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7cbdf-158">RELATED LINKS</span></span>
