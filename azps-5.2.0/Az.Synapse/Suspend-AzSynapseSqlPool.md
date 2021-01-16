---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366175"
---
# <span data-ttu-id="667ea-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="667ea-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="667ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667ea-102">SYNOPSIS</span></span>
<span data-ttu-id="667ea-103">Setzt einen Synapse Analytics SQL aus.</span><span class="sxs-lookup"><span data-stu-id="667ea-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="667ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="667ea-104">SYNTAX</span></span>

### <span data-ttu-id="667ea-105">SuspendByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="667ea-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667ea-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="667ea-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667ea-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="667ea-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667ea-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="667ea-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="667ea-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="667ea-109">DESCRIPTION</span></span>
<span data-ttu-id="667ea-110">Das **Cmdlet "Suspend-AzSynapseSqlPool"** setzt einen Azure Synapse Analytics SQL aus.</span><span class="sxs-lookup"><span data-stu-id="667ea-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="667ea-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="667ea-111">EXAMPLES</span></span>

### <span data-ttu-id="667ea-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="667ea-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="667ea-113">Mit diesem Befehl wird ein aktiver Azure Synapse Analytics SQL angehalten.</span><span class="sxs-lookup"><span data-stu-id="667ea-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="667ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="667ea-114">PARAMETERS</span></span>

### <span data-ttu-id="667ea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="667ea-115">-AsJob</span></span>
<span data-ttu-id="667ea-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="667ea-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="667ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667ea-117">-DefaultProfile</span></span>
<span data-ttu-id="667ea-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="667ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="667ea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="667ea-119">-InputObject</span></span>
<span data-ttu-id="667ea-120">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="667ea-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="667ea-121">-Name</span><span class="sxs-lookup"><span data-stu-id="667ea-121">-Name</span></span>
<span data-ttu-id="667ea-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="667ea-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667ea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="667ea-123">-PassThru</span></span>
<span data-ttu-id="667ea-124">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="667ea-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="667ea-125">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="667ea-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="667ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="667ea-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="667ea-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667ea-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="667ea-128">-ResourceId</span></span>
<span data-ttu-id="667ea-129">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="667ea-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667ea-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="667ea-130">-WorkspaceName</span></span>
<span data-ttu-id="667ea-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="667ea-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667ea-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="667ea-132">-WorkspaceObject</span></span>
<span data-ttu-id="667ea-133">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="667ea-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="667ea-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="667ea-134">-Confirm</span></span>
<span data-ttu-id="667ea-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="667ea-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667ea-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="667ea-136">-WhatIf</span></span>
<span data-ttu-id="667ea-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="667ea-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667ea-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="667ea-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="667ea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667ea-139">CommonParameters</span></span>
<span data-ttu-id="667ea-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667ea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667ea-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="667ea-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667ea-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="667ea-142">INPUTS</span></span>

### <span data-ttu-id="667ea-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="667ea-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="667ea-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="667ea-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="667ea-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="667ea-145">OUTPUTS</span></span>

### <span data-ttu-id="667ea-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="667ea-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="667ea-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="667ea-147">NOTES</span></span>

## <span data-ttu-id="667ea-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="667ea-148">RELATED LINKS</span></span>
