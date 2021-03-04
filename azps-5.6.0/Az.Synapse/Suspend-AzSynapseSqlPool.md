---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: d0249098c8414a38adecc4112449174496656b78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948251"
---
# <span data-ttu-id="29cb9-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="29cb9-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="29cb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="29cb9-103">Ein Synapse Analytics-SQL angehalten.</span><span class="sxs-lookup"><span data-stu-id="29cb9-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="29cb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29cb9-104">SYNTAX</span></span>

### <span data-ttu-id="29cb9-105">SuspendByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="29cb9-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29cb9-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29cb9-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29cb9-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29cb9-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29cb9-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29cb9-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29cb9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29cb9-109">DESCRIPTION</span></span>
<span data-ttu-id="29cb9-110">Das **Cmdlet Suspend-AzSynapseSqlPool** setzt einen Azure Synapse Analytics SQL aus.</span><span class="sxs-lookup"><span data-stu-id="29cb9-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="29cb9-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29cb9-111">EXAMPLES</span></span>

### <span data-ttu-id="29cb9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29cb9-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="29cb9-113">Mit diesem Befehl wird ein aktiver Azure Synapse Analytics-SQL angehalten.</span><span class="sxs-lookup"><span data-stu-id="29cb9-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="29cb9-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="29cb9-114">PARAMETERS</span></span>

### <span data-ttu-id="29cb9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29cb9-115">-AsJob</span></span>
<span data-ttu-id="29cb9-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29cb9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29cb9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29cb9-117">-DefaultProfile</span></span>
<span data-ttu-id="29cb9-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29cb9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29cb9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29cb9-119">-InputObject</span></span>
<span data-ttu-id="29cb9-120">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="29cb9-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="29cb9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="29cb9-121">-Name</span></span>
<span data-ttu-id="29cb9-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="29cb9-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29cb9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29cb9-123">-PassThru</span></span>
<span data-ttu-id="29cb9-124">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="29cb9-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="29cb9-125">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="29cb9-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="29cb9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29cb9-126">-ResourceGroupName</span></span>
<span data-ttu-id="29cb9-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29cb9-127">Resource group name.</span></span>

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

### <span data-ttu-id="29cb9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29cb9-128">-ResourceId</span></span>
<span data-ttu-id="29cb9-129">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="29cb9-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="29cb9-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="29cb9-130">-WorkspaceName</span></span>
<span data-ttu-id="29cb9-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="29cb9-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="29cb9-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="29cb9-132">-WorkspaceObject</span></span>
<span data-ttu-id="29cb9-133">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="29cb9-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="29cb9-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29cb9-134">-Confirm</span></span>
<span data-ttu-id="29cb9-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29cb9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29cb9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29cb9-136">-WhatIf</span></span>
<span data-ttu-id="29cb9-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29cb9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29cb9-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29cb9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29cb9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29cb9-139">CommonParameters</span></span>
<span data-ttu-id="29cb9-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29cb9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29cb9-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29cb9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29cb9-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29cb9-142">INPUTS</span></span>

### <span data-ttu-id="29cb9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="29cb9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="29cb9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="29cb9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="29cb9-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29cb9-145">OUTPUTS</span></span>

### <span data-ttu-id="29cb9-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="29cb9-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="29cb9-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="29cb9-147">NOTES</span></span>

## <span data-ttu-id="29cb9-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="29cb9-148">RELATED LINKS</span></span>
