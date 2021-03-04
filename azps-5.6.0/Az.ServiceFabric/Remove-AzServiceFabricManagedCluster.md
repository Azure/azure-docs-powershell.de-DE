---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: a9e3f5f8305733329f7ff9e34eadde151d873c6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945647"
---
# <span data-ttu-id="c9442-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="c9442-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="c9442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9442-102">SYNOPSIS</span></span>
<span data-ttu-id="c9442-103">Entfernen Sie die Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="c9442-103">Remove cluster resource.</span></span>

## <span data-ttu-id="c9442-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9442-104">SYNTAX</span></span>

### <span data-ttu-id="c9442-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9442-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9442-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c9442-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9442-107">ById</span><span class="sxs-lookup"><span data-stu-id="c9442-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9442-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9442-108">DESCRIPTION</span></span>
<span data-ttu-id="c9442-109">Cluster entfernen Dadurch werden auch die Knotentypen unter dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="c9442-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="c9442-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c9442-110">EXAMPLES</span></span>

### <span data-ttu-id="c9442-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c9442-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="c9442-112">Entfernen Sie den Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9442-112">Remove cluster.</span></span>

### <span data-ttu-id="c9442-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c9442-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="c9442-114">Entfernen Sie den Cluster mit Piping.</span><span class="sxs-lookup"><span data-stu-id="c9442-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="c9442-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c9442-115">PARAMETERS</span></span>

### <span data-ttu-id="c9442-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9442-116">-AsJob</span></span>
<span data-ttu-id="c9442-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="c9442-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c9442-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9442-118">-DefaultProfile</span></span>
<span data-ttu-id="c9442-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9442-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9442-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9442-120">-InputObject</span></span>
<span data-ttu-id="c9442-121">Verwaltete Clusterressource</span><span class="sxs-lookup"><span data-stu-id="c9442-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9442-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c9442-122">-Name</span></span>
<span data-ttu-id="c9442-123">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="c9442-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9442-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9442-124">-PassThru</span></span>
<span data-ttu-id="c9442-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="c9442-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c9442-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9442-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9442-127">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c9442-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9442-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9442-128">-ResourceId</span></span>
<span data-ttu-id="c9442-129">Ressourcen-ID für verwaltete Cluster</span><span class="sxs-lookup"><span data-stu-id="c9442-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9442-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9442-130">-Confirm</span></span>
<span data-ttu-id="c9442-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9442-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9442-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9442-132">-WhatIf</span></span>
<span data-ttu-id="c9442-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9442-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9442-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9442-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9442-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9442-135">CommonParameters</span></span>
<span data-ttu-id="c9442-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9442-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9442-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9442-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9442-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c9442-138">INPUTS</span></span>

### <span data-ttu-id="c9442-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c9442-139">System.String</span></span>

## <span data-ttu-id="c9442-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c9442-140">OUTPUTS</span></span>

### <span data-ttu-id="c9442-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c9442-141">System.Boolean</span></span>

## <span data-ttu-id="c9442-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c9442-142">NOTES</span></span>

## <span data-ttu-id="c9442-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c9442-143">RELATED LINKS</span></span>
