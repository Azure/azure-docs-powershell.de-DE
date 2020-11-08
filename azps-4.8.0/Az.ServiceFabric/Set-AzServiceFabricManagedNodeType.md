---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173510"
---
# <span data-ttu-id="e94a5-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e94a5-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="e94a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e94a5-102">SYNOPSIS</span></span>
<span data-ttu-id="e94a5-103">Legt Knotentyp-Ressourceneigenschaften fest oder führt reimage-Aktionen für bestimmte NDES des Knotentyps mit dem Parameter-reimage aus.</span><span class="sxs-lookup"><span data-stu-id="e94a5-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="e94a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e94a5-104">SYNTAX</span></span>

### <span data-ttu-id="e94a5-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="e94a5-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94a5-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="e94a5-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e94a5-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="e94a5-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94a5-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="e94a5-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94a5-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="e94a5-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94a5-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="e94a5-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e94a5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e94a5-111">DESCRIPTION</span></span>
<span data-ttu-id="e94a5-112">Legt Knotentyp-Ressourceneigenschaften fest oder führt reimage-Aktionen für bestimmte NDES des Knotentyps mit dem Parameter-reimage aus.</span><span class="sxs-lookup"><span data-stu-id="e94a5-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="e94a5-113">Bei einem reimgae-Vorgang werden die Service Fabric-Knoten deaktiviert, bevor Sie die VMs erneut abbilden und Sie wieder aktivieren, sobald Sie wieder verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e94a5-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="e94a5-114">Wenn dies für primäre Knotentypen erfolgt, kann es eine Weile dauern, da es möglicherweise nicht alle Knoten zur gleichen Zeit umbildet.</span><span class="sxs-lookup"><span data-stu-id="e94a5-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="e94a5-115">Use-ForceReimage erzwingen Sie den Vorgang selbst dann, wenn Service Fabric die Knoten nicht deaktivieren, aber mit Vorsicht verwenden kann, da dies zu Datenverlusten führen kann, wenn statusbehaftete Arbeitslasten auf dem Knoten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e94a5-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="e94a5-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e94a5-116">EXAMPLES</span></span>

### <span data-ttu-id="e94a5-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e94a5-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="e94a5-118">Aktualisieren Sie die Anzahl der Instanzen des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="e94a5-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="e94a5-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e94a5-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="e94a5-120">Aktualisieren der Platzierungs-properites des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="e94a5-120">Update placement properites of the node type.</span></span> <span data-ttu-id="e94a5-121">Dadurch werden ältere Placement-properites, falls vorhanden, überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e94a5-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="e94a5-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e94a5-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="e94a5-123">Umbilden von Knoten 0 und 3 auf dem Knotentyp</span><span class="sxs-lookup"><span data-stu-id="e94a5-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="e94a5-124">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e94a5-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="e94a5-125">Aktualisieren Sie die Anzahl der Instanzen des Knotentyps mit Piping.</span><span class="sxs-lookup"><span data-stu-id="e94a5-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="e94a5-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="e94a5-126">PARAMETERS</span></span>

### <span data-ttu-id="e94a5-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="e94a5-127">-ApplicationEndPort</span></span>
<span data-ttu-id="e94a5-128">Anwendungsendpunkt eines Portbereichs</span><span class="sxs-lookup"><span data-stu-id="e94a5-128">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="e94a5-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="e94a5-129">-ApplicationStartPort</span></span>
<span data-ttu-id="e94a5-130">Anwendungsstart Port eines Bereichs von Ports.</span><span class="sxs-lookup"><span data-stu-id="e94a5-130">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="e94a5-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e94a5-131">-AsJob</span></span>
<span data-ttu-id="e94a5-132">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="e94a5-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e94a5-133">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="e94a5-133">-Capacity</span></span>
<span data-ttu-id="e94a5-134">Kapazitätskategorien, die auf die Knoten im Knotentyp als Schlüssel-Wert-Paare angewendet wurden, verwendet der Clusterressourcen-Manager diese Tags, um zu verstehen, wie viel Ressourcen ein Knoten besitzt.</span><span class="sxs-lookup"><span data-stu-id="e94a5-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="e94a5-135">Beim Aktualisieren werden die aktuellen Werte außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="e94a5-135">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="e94a5-136">-Clustername</span><span class="sxs-lookup"><span data-stu-id="e94a5-136">-ClusterName</span></span>
<span data-ttu-id="e94a5-137">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e94a5-137">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e94a5-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94a5-138">-DefaultProfile</span></span>
<span data-ttu-id="e94a5-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e94a5-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e94a5-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="e94a5-140">-EphemeralEndPort</span></span>
<span data-ttu-id="e94a5-141">Ephemerer Endpunkt Port eines Bereichs von Ports.</span><span class="sxs-lookup"><span data-stu-id="e94a5-141">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="e94a5-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="e94a5-142">-EphemeralStartPort</span></span>
<span data-ttu-id="e94a5-143">Ephemerer Start-Port eines Bereichs von Ports.</span><span class="sxs-lookup"><span data-stu-id="e94a5-143">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="e94a5-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="e94a5-144">-ForceReimage</span></span>
<span data-ttu-id="e94a5-145">Wenn Sie dieses Flag verwenden, wird die Entfernung erzwungen, auch wenn Service Fabric die Knoten nicht deaktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="e94a5-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="e94a5-146">Verwenden Sie mit bedacht, da dies zu Datenverlusten führen kann, wenn auf dem Knotenstatus behaftete Arbeitslasten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e94a5-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

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

### <span data-ttu-id="e94a5-147">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e94a5-147">-InputObject</span></span>
<span data-ttu-id="e94a5-148">Knotentyp Ressource</span><span class="sxs-lookup"><span data-stu-id="e94a5-148">Node type resource</span></span>

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

### <span data-ttu-id="e94a5-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="e94a5-149">-InstanceCount</span></span>
<span data-ttu-id="e94a5-150">Die Anzahl der Knoten im Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="e94a5-150">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="e94a5-151">-Name</span><span class="sxs-lookup"><span data-stu-id="e94a5-151">-Name</span></span>
<span data-ttu-id="e94a5-152">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="e94a5-152">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="e94a5-153">-Nodename</span><span class="sxs-lookup"><span data-stu-id="e94a5-153">-NodeName</span></span>
<span data-ttu-id="e94a5-154">Liste der Knotennamen für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e94a5-154">List of node names for the operation.</span></span>

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

### <span data-ttu-id="e94a5-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e94a5-155">-PassThru</span></span>
<span data-ttu-id="e94a5-156">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="e94a5-156">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e94a5-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="e94a5-157">-PlacementProperty</span></span>
<span data-ttu-id="e94a5-158">Platzierungs Tags, die auf Knoten im Knotentyp als Schlüssel-Wert-Paare angewendet werden, können verwendet werden, um anzugeben, wo bestimmte Dienste (Arbeitsauslastung) ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e94a5-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="e94a5-159">Beim Aktualisieren werden die aktuellen Werte außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="e94a5-159">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="e94a5-160">-Reimage</span><span class="sxs-lookup"><span data-stu-id="e94a5-160">-Reimage</span></span>
<span data-ttu-id="e94a5-161">Geben Sie an, dass Knoten auf dem Knotentyp erneut abbilden sollen.</span><span class="sxs-lookup"><span data-stu-id="e94a5-161">Specify to reimage nodes on the node type.</span></span>

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

### <span data-ttu-id="e94a5-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94a5-162">-ResourceGroupName</span></span>
<span data-ttu-id="e94a5-163">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e94a5-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e94a5-164">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e94a5-164">-ResourceId</span></span>
<span data-ttu-id="e94a5-165">Ressourcen-ID des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="e94a5-165">Node type resource id</span></span>

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

### <span data-ttu-id="e94a5-166">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e94a5-166">-Confirm</span></span>
<span data-ttu-id="e94a5-167">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e94a5-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e94a5-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94a5-168">-WhatIf</span></span>
<span data-ttu-id="e94a5-169">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e94a5-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94a5-170">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e94a5-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e94a5-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94a5-171">CommonParameters</span></span>
<span data-ttu-id="e94a5-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e94a5-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94a5-173">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e94a5-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94a5-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e94a5-174">INPUTS</span></span>

### <span data-ttu-id="e94a5-175">System. String</span><span class="sxs-lookup"><span data-stu-id="e94a5-175">System.String</span></span>

## <span data-ttu-id="e94a5-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e94a5-176">OUTPUTS</span></span>

### <span data-ttu-id="e94a5-177">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e94a5-177">System.Boolean</span></span>

## <span data-ttu-id="e94a5-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="e94a5-178">NOTES</span></span>

## <span data-ttu-id="e94a5-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e94a5-179">RELATED LINKS</span></span>
