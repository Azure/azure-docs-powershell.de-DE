---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304667"
---
# <span data-ttu-id="285d8-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="285d8-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="285d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="285d8-102">SYNOPSIS</span></span>
<span data-ttu-id="285d8-103">Löschen Sie den Knotenpool aus dem verwalteten Cluster.</span><span class="sxs-lookup"><span data-stu-id="285d8-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="285d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="285d8-104">SYNTAX</span></span>

### <span data-ttu-id="285d8-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="285d8-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="285d8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="285d8-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="285d8-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="285d8-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="285d8-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="285d8-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="285d8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285d8-109">DESCRIPTION</span></span>
<span data-ttu-id="285d8-110">Löschen Sie den Knotenpool aus dem verwalteten Cluster.</span><span class="sxs-lookup"><span data-stu-id="285d8-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="285d8-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="285d8-111">EXAMPLES</span></span>

### <span data-ttu-id="285d8-112">Löschen eines angegebenen Knotenpools</span><span class="sxs-lookup"><span data-stu-id="285d8-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="285d8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="285d8-113">PARAMETERS</span></span>

### <span data-ttu-id="285d8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="285d8-114">-AsJob</span></span>
<span data-ttu-id="285d8-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="285d8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="285d8-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="285d8-116">-ClusterName</span></span>
<span data-ttu-id="285d8-117">Name des verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="285d8-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285d8-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="285d8-118">-ClusterObject</span></span>
<span data-ttu-id="285d8-119">Das Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="285d8-119">The cluster object.</span></span>

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

### <span data-ttu-id="285d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285d8-120">-DefaultProfile</span></span>
<span data-ttu-id="285d8-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="285d8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="285d8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="285d8-122">-Force</span></span>
<span data-ttu-id="285d8-123">Entfernen des Knotenpools ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="285d8-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="285d8-124">-ID</span><span class="sxs-lookup"><span data-stu-id="285d8-124">-Id</span></span>
<span data-ttu-id="285d8-125">ID eines Knotenpools im verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="285d8-125">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285d8-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="285d8-126">-InputObject</span></span>
<span data-ttu-id="285d8-127">Ein PSAgentPool-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="285d8-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="285d8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="285d8-128">-Name</span></span>
<span data-ttu-id="285d8-129">Name des Knotenpools</span><span class="sxs-lookup"><span data-stu-id="285d8-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285d8-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="285d8-130">-PassThru</span></span>
<span data-ttu-id="285d8-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="285d8-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="285d8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="285d8-132">-ResourceGroupName</span></span>
<span data-ttu-id="285d8-133">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="285d8-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285d8-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="285d8-134">-Confirm</span></span>
<span data-ttu-id="285d8-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="285d8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="285d8-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="285d8-136">-WhatIf</span></span>
<span data-ttu-id="285d8-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="285d8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="285d8-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="285d8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="285d8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285d8-139">CommonParameters</span></span>
<span data-ttu-id="285d8-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285d8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285d8-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="285d8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285d8-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="285d8-142">INPUTS</span></span>

### <span data-ttu-id="285d8-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="285d8-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="285d8-144">System.String</span><span class="sxs-lookup"><span data-stu-id="285d8-144">System.String</span></span>

## <span data-ttu-id="285d8-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="285d8-145">OUTPUTS</span></span>

### <span data-ttu-id="285d8-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="285d8-146">System.Boolean</span></span>

## <span data-ttu-id="285d8-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="285d8-147">NOTES</span></span>

## <span data-ttu-id="285d8-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="285d8-148">RELATED LINKS</span></span>
