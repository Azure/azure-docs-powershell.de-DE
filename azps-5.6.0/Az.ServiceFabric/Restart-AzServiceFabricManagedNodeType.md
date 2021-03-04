---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 8b68175be91b3669c42a67259f5095b567e7905e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945599"
---
# <span data-ttu-id="d57f8-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d57f8-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="d57f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d57f8-102">SYNOPSIS</span></span>
<span data-ttu-id="d57f8-103">Starten Sie bestimmte Knoten vom Knotentyp neu.</span><span class="sxs-lookup"><span data-stu-id="d57f8-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="d57f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d57f8-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d57f8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d57f8-105">DESCRIPTION</span></span>
<span data-ttu-id="d57f8-106">Starten Sie bestimmte Knoten vom Knotentyp neu.</span><span class="sxs-lookup"><span data-stu-id="d57f8-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="d57f8-107">Es deaktiviert die Dienst-Fabric-Knoten, bevor die vms neu gestartet werden, und aktiviert sie wieder, sobald sie wiederkommen.</span><span class="sxs-lookup"><span data-stu-id="d57f8-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="d57f8-108">Wenn dies für primäre Knotentypen erfolgt, kann es eine Weile dauern, da möglicherweise nicht alle Knoten gleichzeitig neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d57f8-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="d57f8-109">Verwenden Sie -ForceRestart erzwingen den Vorgang, auch wenn service fabric die Knoten nicht deaktivieren kann, aber mit Vorsicht vorgehen kann, da dies zu Datenverlust führen kann, wenn auf dem Knoten zustandsreiche Arbeitsauslastungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d57f8-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="d57f8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d57f8-110">EXAMPLES</span></span>

### <span data-ttu-id="d57f8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d57f8-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="d57f8-112">Starten Sie knoten 0 und 3 für den Knotentyp neu.</span><span class="sxs-lookup"><span data-stu-id="d57f8-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="d57f8-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d57f8-113">PARAMETERS</span></span>

### <span data-ttu-id="d57f8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d57f8-114">-AsJob</span></span>
<span data-ttu-id="d57f8-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="d57f8-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d57f8-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d57f8-116">-ClusterName</span></span>
<span data-ttu-id="d57f8-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="d57f8-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d57f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57f8-118">-DefaultProfile</span></span>
<span data-ttu-id="d57f8-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d57f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d57f8-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="d57f8-120">-ForceRestart</span></span>
<span data-ttu-id="d57f8-121">Wenn Sie dieses Kennzeichen verwenden, wird der Knoten zum Neustart zwingen, auch wenn service fabric die Knoten nicht deaktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="d57f8-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="d57f8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d57f8-122">-Name</span></span>
<span data-ttu-id="d57f8-123">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="d57f8-123">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="d57f8-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="d57f8-124">-NodeName</span></span>
<span data-ttu-id="d57f8-125">Liste der Knotennamen für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d57f8-125">List of node names for the operation.</span></span>

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

### <span data-ttu-id="d57f8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d57f8-126">-PassThru</span></span>
<span data-ttu-id="d57f8-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d57f8-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d57f8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57f8-128">-ResourceGroupName</span></span>
<span data-ttu-id="d57f8-129">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d57f8-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d57f8-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d57f8-130">-Confirm</span></span>
<span data-ttu-id="d57f8-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d57f8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d57f8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57f8-132">-WhatIf</span></span>
<span data-ttu-id="d57f8-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d57f8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d57f8-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d57f8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d57f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57f8-135">CommonParameters</span></span>
<span data-ttu-id="d57f8-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d57f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57f8-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d57f8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57f8-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d57f8-138">INPUTS</span></span>

### <span data-ttu-id="d57f8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d57f8-139">System.String</span></span>

## <span data-ttu-id="d57f8-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d57f8-140">OUTPUTS</span></span>

### <span data-ttu-id="d57f8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d57f8-141">System.Boolean</span></span>

## <span data-ttu-id="d57f8-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d57f8-142">NOTES</span></span>

## <span data-ttu-id="d57f8-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d57f8-143">RELATED LINKS</span></span>
