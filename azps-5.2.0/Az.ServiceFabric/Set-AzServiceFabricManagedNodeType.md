---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356543"
---
# <span data-ttu-id="49c5c-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="49c5c-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="49c5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="49c5c-103">Legt Ressourceneigenschaften des Knotentyps fest, oder führen Sie Reimageaktionen für bestimmte Typen des Knotentyps mit dem Parameter "-Reimage" aus.</span><span class="sxs-lookup"><span data-stu-id="49c5c-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="49c5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49c5c-104">SYNTAX</span></span>

### <span data-ttu-id="49c5c-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="49c5c-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49c5c-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="49c5c-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49c5c-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="49c5c-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49c5c-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="49c5c-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49c5c-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="49c5c-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49c5c-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="49c5c-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49c5c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49c5c-111">DESCRIPTION</span></span>
<span data-ttu-id="49c5c-112">Legt Ressourceneigenschaften des Knotentyps fest, oder führen Sie Reimageaktionen für bestimmte Typen des Knotentyps mit dem Parameter "-Reimage" aus.</span><span class="sxs-lookup"><span data-stu-id="49c5c-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="49c5c-113">Bei einem reimgae-Vorgang werden die Dienststrukturknoten deaktiviert, bevor sie die vms neu erstellen, und sie wieder aktiviert, sobald sie wieder da sind.</span><span class="sxs-lookup"><span data-stu-id="49c5c-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="49c5c-114">Wenn dies für primäre Knotentypen erfolgt, kann dies eine Weile dauern, da möglicherweise nicht alle Knoten gleichzeitig neu abbilden werden.</span><span class="sxs-lookup"><span data-stu-id="49c5c-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="49c5c-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span><span class="sxs-lookup"><span data-stu-id="49c5c-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="49c5c-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49c5c-116">EXAMPLES</span></span>

### <span data-ttu-id="49c5c-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49c5c-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="49c5c-118">Aktualisieren Sie die Instanzenanzahl des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="49c5c-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="49c5c-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="49c5c-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="49c5c-120">Aktualisieren sie die Platzierung der Richtigen des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="49c5c-120">Update placement properites of the node type.</span></span> <span data-ttu-id="49c5c-121">Dadurch werden ältere Platzierungs-Properites (sofern vorhanden) überschrieben.</span><span class="sxs-lookup"><span data-stu-id="49c5c-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="49c5c-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="49c5c-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="49c5c-123">Knoten 0 und 3 für den Knotentyp neu abbilden</span><span class="sxs-lookup"><span data-stu-id="49c5c-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="49c5c-124">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="49c5c-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="49c5c-125">Aktualisieren Sie die Instanzenanzahl des Knotentyps mit Piping.</span><span class="sxs-lookup"><span data-stu-id="49c5c-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="49c5c-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49c5c-126">PARAMETERS</span></span>

### <span data-ttu-id="49c5c-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="49c5c-127">-ApplicationEndPort</span></span>
<span data-ttu-id="49c5c-128">Anwendungsendport einer Reihe von Ports.</span><span class="sxs-lookup"><span data-stu-id="49c5c-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="49c5c-129">-ApplicationStartPort</span></span>
<span data-ttu-id="49c5c-130">Anwendungsstartport einer Reihe von Ports</span><span class="sxs-lookup"><span data-stu-id="49c5c-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49c5c-131">-AsJob</span></span>
<span data-ttu-id="49c5c-132">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="49c5c-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="49c5c-133">-Capacity</span><span class="sxs-lookup"><span data-stu-id="49c5c-133">-Capacity</span></span>
<span data-ttu-id="49c5c-134">Auf die Knoten im Knotentyp als Schlüssel/Wert-Paare angewendete Kapazitätstags verwendet der Clusterressourcen-Manager diese Tags, um zu verstehen, wie viel Ressourcen ein Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="49c5c-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="49c5c-135">Durch das Aktualisieren dieser Einstellung werden die aktuellen Werte überschrieben.</span><span class="sxs-lookup"><span data-stu-id="49c5c-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="49c5c-136">-ClusterName</span></span>
<span data-ttu-id="49c5c-137">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="49c5c-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c5c-138">-DefaultProfile</span></span>
<span data-ttu-id="49c5c-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49c5c-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49c5c-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="49c5c-140">-EphemeralEndPort</span></span>
<span data-ttu-id="49c5c-141">Kurzlebiger Endport eines Portsbereichs.</span><span class="sxs-lookup"><span data-stu-id="49c5c-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="49c5c-142">-EphemeralStartPort</span></span>
<span data-ttu-id="49c5c-143">Kurzlebiger Startport eines Portsbereichs.</span><span class="sxs-lookup"><span data-stu-id="49c5c-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="49c5c-144">-ForceReimage</span></span>
<span data-ttu-id="49c5c-145">Wenn Sie dieses Flag verwenden, wird das Entfernen auch dann erzwingen, wenn das Service Fabric die Knoten nicht deaktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="49c5c-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="49c5c-146">Seien Sie vorsichtig, da dies zu Datenverlust führen kann, wenn auf dem Knoten zustandsreiche Workloads ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="49c5c-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49c5c-147">-InputObject</span></span>
<span data-ttu-id="49c5c-148">Knotentypressource</span><span class="sxs-lookup"><span data-stu-id="49c5c-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="49c5c-149">-InstanceCount</span></span>
<span data-ttu-id="49c5c-150">Die Anzahl der Knoten im Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="49c5c-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-151">-Name</span><span class="sxs-lookup"><span data-stu-id="49c5c-151">-Name</span></span>
<span data-ttu-id="49c5c-152">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="49c5c-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="49c5c-153">-NodeName</span></span>
<span data-ttu-id="49c5c-154">Liste der Knotennamen für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="49c5c-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49c5c-155">-PassThru</span></span>
<span data-ttu-id="49c5c-156">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="49c5c-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="49c5c-157">-PlacementProperty</span></span>
<span data-ttu-id="49c5c-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span><span class="sxs-lookup"><span data-stu-id="49c5c-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="49c5c-159">Durch das Aktualisieren dieser Einstellung werden die aktuellen Werte überschrieben.</span><span class="sxs-lookup"><span data-stu-id="49c5c-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-160">-Reimage</span><span class="sxs-lookup"><span data-stu-id="49c5c-160">-Reimage</span></span>
<span data-ttu-id="49c5c-161">Geben Sie an, dass Knoten für den Knotentyp neu geimaget werden.</span><span class="sxs-lookup"><span data-stu-id="49c5c-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c5c-162">-ResourceGroupName</span></span>
<span data-ttu-id="49c5c-163">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="49c5c-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49c5c-164">-ResourceId</span></span>
<span data-ttu-id="49c5c-165">Ressourcen-ID des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="49c5c-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49c5c-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49c5c-166">-Confirm</span></span>
<span data-ttu-id="49c5c-167">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49c5c-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49c5c-168">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="49c5c-168">-WhatIf</span></span>
<span data-ttu-id="49c5c-169">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49c5c-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49c5c-170">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49c5c-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49c5c-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c5c-171">CommonParameters</span></span>
<span data-ttu-id="49c5c-172">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c5c-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c5c-173">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49c5c-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c5c-174">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49c5c-174">INPUTS</span></span>

### <span data-ttu-id="49c5c-175">System.String</span><span class="sxs-lookup"><span data-stu-id="49c5c-175">System.String</span></span>

## <span data-ttu-id="49c5c-176">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49c5c-176">OUTPUTS</span></span>

### <span data-ttu-id="49c5c-177">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49c5c-177">System.Boolean</span></span>

## <span data-ttu-id="49c5c-178">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="49c5c-178">NOTES</span></span>

## <span data-ttu-id="49c5c-179">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="49c5c-179">RELATED LINKS</span></span>
