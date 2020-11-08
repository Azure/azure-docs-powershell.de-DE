---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176066"
---
# <span data-ttu-id="261bb-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="261bb-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="261bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="261bb-102">SYNOPSIS</span></span>
<span data-ttu-id="261bb-103">Entfernen des Knotentyps oder bestimmter Knoten innerhalb des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="261bb-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="261bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="261bb-104">SYNTAX</span></span>

### <span data-ttu-id="261bb-105">DeleteNodeTypeByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="261bb-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261bb-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="261bb-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261bb-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="261bb-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261bb-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="261bb-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="261bb-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="261bb-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261bb-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="261bb-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="261bb-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="261bb-111">DESCRIPTION</span></span>
<span data-ttu-id="261bb-112">Entfernen des Knotentyps oder bestimmter Knoten innerhalb des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="261bb-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="261bb-113">Wenn der paremter-nodename verwendet wird, werden nur die angegebenen Knoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="261bb-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="261bb-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="261bb-114">EXAMPLES</span></span>

### <span data-ttu-id="261bb-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="261bb-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="261bb-116">Entfernen des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="261bb-116">Remove node type.</span></span>

### <span data-ttu-id="261bb-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="261bb-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="261bb-118">Entfernen des Knotentyps mit Piping</span><span class="sxs-lookup"><span data-stu-id="261bb-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="261bb-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="261bb-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="261bb-120">Entfernen Sie 2 Knoten aus dem Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="261bb-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="261bb-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="261bb-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="261bb-122">Entfernen Sie 2 Knoten aus dem Knotentyp mit Piping.</span><span class="sxs-lookup"><span data-stu-id="261bb-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="261bb-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="261bb-123">PARAMETERS</span></span>

### <span data-ttu-id="261bb-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="261bb-124">-AsJob</span></span>
<span data-ttu-id="261bb-125">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="261bb-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="261bb-126">-Clustername</span><span class="sxs-lookup"><span data-stu-id="261bb-126">-ClusterName</span></span>
<span data-ttu-id="261bb-127">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="261bb-127">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="261bb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261bb-128">-DefaultProfile</span></span>
<span data-ttu-id="261bb-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="261bb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="261bb-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="261bb-130">-ForceRemoveNode</span></span>
<span data-ttu-id="261bb-131">Wenn Sie dieses Flag verwenden, wird die Entfernung erzwungen, auch wenn Service Fabric die Knoten nicht deaktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="261bb-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="261bb-132">Verwenden Sie mit bedacht, da dies zu Datenverlusten führen kann, wenn statusbehaftete Arbeitsauslastungen auf den Knoten ausgeführt werden, oder den Cluster nach unten bringen, wenn nicht genügend Seed-Knoten nach dem opearion vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="261bb-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

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

### <span data-ttu-id="261bb-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="261bb-133">-InputObject</span></span>
<span data-ttu-id="261bb-134">Knotentyp Ressource</span><span class="sxs-lookup"><span data-stu-id="261bb-134">Node type resource</span></span>

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

### <span data-ttu-id="261bb-135">-Name</span><span class="sxs-lookup"><span data-stu-id="261bb-135">-Name</span></span>
<span data-ttu-id="261bb-136">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="261bb-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="261bb-137">-Nodename</span><span class="sxs-lookup"><span data-stu-id="261bb-137">-NodeName</span></span>
<span data-ttu-id="261bb-138">Liste der Knotennamen für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="261bb-138">List of node names for the operation.</span></span>

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

### <span data-ttu-id="261bb-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="261bb-139">-PassThru</span></span>
<span data-ttu-id="261bb-140">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="261bb-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="261bb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="261bb-141">-ResourceGroupName</span></span>
<span data-ttu-id="261bb-142">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="261bb-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="261bb-143">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="261bb-143">-ResourceId</span></span>
<span data-ttu-id="261bb-144">Ressourcen-ID des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="261bb-144">Node type resource id</span></span>

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

### <span data-ttu-id="261bb-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="261bb-145">-Confirm</span></span>
<span data-ttu-id="261bb-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="261bb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="261bb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="261bb-147">-WhatIf</span></span>
<span data-ttu-id="261bb-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="261bb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="261bb-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="261bb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="261bb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261bb-150">CommonParameters</span></span>
<span data-ttu-id="261bb-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="261bb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261bb-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="261bb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261bb-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="261bb-153">INPUTS</span></span>

### <span data-ttu-id="261bb-154">System. String</span><span class="sxs-lookup"><span data-stu-id="261bb-154">System.String</span></span>

## <span data-ttu-id="261bb-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="261bb-155">OUTPUTS</span></span>

### <span data-ttu-id="261bb-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="261bb-156">System.Boolean</span></span>

## <span data-ttu-id="261bb-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="261bb-157">NOTES</span></span>

## <span data-ttu-id="261bb-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="261bb-158">RELATED LINKS</span></span>
