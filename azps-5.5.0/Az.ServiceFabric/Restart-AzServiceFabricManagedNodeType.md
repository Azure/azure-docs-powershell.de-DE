---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150657"
---
# <span data-ttu-id="dd1f4-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="dd1f4-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="dd1f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd1f4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1f4-103">Starten Sie bestimmte Knoten vom Knotentyp neu.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="dd1f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd1f4-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd1f4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd1f4-105">DESCRIPTION</span></span>
<span data-ttu-id="dd1f4-106">Starten Sie bestimmte Knoten vom Knotentyp neu.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="dd1f4-107">Es deaktiviert die Dienststrukturknoten vor dem Neustart der vms und aktiviert sie wieder, sobald sie wieder da sind.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="dd1f4-108">Wenn dies für primäre Knotentypen erfolgt, kann dies eine Weile dauern, da möglicherweise nicht alle Knoten gleichzeitig neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="dd1f4-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="dd1f4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd1f4-110">EXAMPLES</span></span>

### <span data-ttu-id="dd1f4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd1f4-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="dd1f4-112">Starten Sie Knoten 0 und 3 für den Knotentyp neu.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="dd1f4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd1f4-113">PARAMETERS</span></span>

### <span data-ttu-id="dd1f4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd1f4-114">-AsJob</span></span>
<span data-ttu-id="dd1f4-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dd1f4-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dd1f4-116">-ClusterName</span></span>
<span data-ttu-id="dd1f4-117">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1f4-118">-DefaultProfile</span></span>
<span data-ttu-id="dd1f4-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd1f4-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="dd1f4-120">-ForceRestart</span></span>
<span data-ttu-id="dd1f4-121">Wenn Sie dieses Flag verwenden, wird der Neustart des Knotens auch dann erzwingen, wenn das Service Fabric die Knoten nicht deaktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="dd1f4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dd1f4-122">-Name</span></span>
<span data-ttu-id="dd1f4-123">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1f4-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="dd1f4-124">-NodeName</span></span>
<span data-ttu-id="dd1f4-125">Liste der Knotennamen für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1f4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd1f4-126">-PassThru</span></span>
<span data-ttu-id="dd1f4-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="dd1f4-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="dd1f4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd1f4-128">-ResourceGroupName</span></span>
<span data-ttu-id="dd1f4-129">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1f4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd1f4-130">-Confirm</span></span>
<span data-ttu-id="dd1f4-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd1f4-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dd1f4-132">-WhatIf</span></span>
<span data-ttu-id="dd1f4-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd1f4-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd1f4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1f4-135">CommonParameters</span></span>
<span data-ttu-id="dd1f4-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd1f4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1f4-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd1f4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1f4-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd1f4-138">INPUTS</span></span>

### <span data-ttu-id="dd1f4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dd1f4-139">System.String</span></span>

## <span data-ttu-id="dd1f4-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd1f4-140">OUTPUTS</span></span>

### <span data-ttu-id="dd1f4-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd1f4-141">System.Boolean</span></span>

## <span data-ttu-id="dd1f4-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dd1f4-142">NOTES</span></span>

## <span data-ttu-id="dd1f4-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dd1f4-143">RELATED LINKS</span></span>
