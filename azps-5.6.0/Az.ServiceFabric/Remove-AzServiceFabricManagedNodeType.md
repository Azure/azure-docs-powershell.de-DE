---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5cb0e5bf8dce38a8552514835d2e16d19c3cc833
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945640"
---
# <span data-ttu-id="735ef-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="735ef-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="735ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="735ef-102">SYNOPSIS</span></span>
<span data-ttu-id="735ef-103">Entfernen Sie den Knotentyp oder bestimmte Knoten innerhalb des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="735ef-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="735ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="735ef-104">SYNTAX</span></span>

### <span data-ttu-id="735ef-105">DeleteNodeTypeByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="735ef-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="735ef-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="735ef-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="735ef-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="735ef-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="735ef-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="735ef-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="735ef-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="735ef-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="735ef-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="735ef-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="735ef-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="735ef-111">DESCRIPTION</span></span>
<span data-ttu-id="735ef-112">Entfernen Sie den Knotentyp oder bestimmte Knoten innerhalb des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="735ef-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="735ef-113">Wenn der Paremter -NodeName verwendet wird, werden nur die angegebenen Knoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="735ef-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="735ef-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="735ef-114">EXAMPLES</span></span>

### <span data-ttu-id="735ef-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="735ef-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="735ef-116">Knotentyp entfernen.</span><span class="sxs-lookup"><span data-stu-id="735ef-116">Remove node type.</span></span>

### <span data-ttu-id="735ef-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="735ef-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="735ef-118">Entfernen Sie den Knotentyp mit Piping.</span><span class="sxs-lookup"><span data-stu-id="735ef-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="735ef-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="735ef-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="735ef-120">Entfernen Sie zwei Knoten aus dem Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="735ef-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="735ef-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="735ef-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="735ef-122">Entfernen Sie 2 Knoten vom Knotentyp mit Piping.</span><span class="sxs-lookup"><span data-stu-id="735ef-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="735ef-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="735ef-123">PARAMETERS</span></span>

### <span data-ttu-id="735ef-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="735ef-124">-AsJob</span></span>
<span data-ttu-id="735ef-125">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="735ef-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="735ef-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="735ef-126">-ClusterName</span></span>
<span data-ttu-id="735ef-127">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="735ef-127">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="735ef-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735ef-128">-DefaultProfile</span></span>
<span data-ttu-id="735ef-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="735ef-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="735ef-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="735ef-130">-ForceRemoveNode</span></span>
<span data-ttu-id="735ef-131">Wenn Sie dieses Kennzeichen verwenden, wird das Entfernen auch dann erzwingen, wenn service fabric die Knoten nicht deaktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="735ef-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="735ef-132">Verwenden Sie mit Bedacht, da dies zu Datenverlusten führen kann, wenn zustandsbehaftete Arbeitsauslastungen auf den Knoten ausgeführt werden, oder den Cluster verringern, wenn nach dem Opearion nicht genügend Startknoten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="735ef-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

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

### <span data-ttu-id="735ef-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="735ef-133">-InputObject</span></span>
<span data-ttu-id="735ef-134">Knotentypressource</span><span class="sxs-lookup"><span data-stu-id="735ef-134">Node type resource</span></span>

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

### <span data-ttu-id="735ef-135">-Name</span><span class="sxs-lookup"><span data-stu-id="735ef-135">-Name</span></span>
<span data-ttu-id="735ef-136">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="735ef-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="735ef-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="735ef-137">-NodeName</span></span>
<span data-ttu-id="735ef-138">Liste der Knotennamen für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="735ef-138">List of node names for the operation.</span></span>

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

### <span data-ttu-id="735ef-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="735ef-139">-PassThru</span></span>
<span data-ttu-id="735ef-140">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="735ef-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="735ef-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="735ef-141">-ResourceGroupName</span></span>
<span data-ttu-id="735ef-142">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="735ef-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="735ef-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="735ef-143">-ResourceId</span></span>
<span data-ttu-id="735ef-144">Ressourcen-ID des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="735ef-144">Node type resource id</span></span>

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

### <span data-ttu-id="735ef-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="735ef-145">-Confirm</span></span>
<span data-ttu-id="735ef-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="735ef-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="735ef-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="735ef-147">-WhatIf</span></span>
<span data-ttu-id="735ef-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="735ef-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="735ef-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="735ef-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="735ef-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735ef-150">CommonParameters</span></span>
<span data-ttu-id="735ef-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735ef-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735ef-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="735ef-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735ef-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="735ef-153">INPUTS</span></span>

### <span data-ttu-id="735ef-154">System.String</span><span class="sxs-lookup"><span data-stu-id="735ef-154">System.String</span></span>

## <span data-ttu-id="735ef-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="735ef-155">OUTPUTS</span></span>

### <span data-ttu-id="735ef-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="735ef-156">System.Boolean</span></span>

## <span data-ttu-id="735ef-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="735ef-157">NOTES</span></span>

## <span data-ttu-id="735ef-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="735ef-158">RELATED LINKS</span></span>
