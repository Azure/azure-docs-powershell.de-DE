---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: cfcfb283887e221db02c894f7a7712203e516996
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926192"
---
# <span data-ttu-id="9b2fe-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9b2fe-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="9b2fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b2fe-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2fe-103">Setzt einen Synapse Analytics-SQL fort.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9b2fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b2fe-104">SYNTAX</span></span>

### <span data-ttu-id="9b2fe-105">ResumeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b2fe-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b2fe-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b2fe-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b2fe-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b2fe-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b2fe-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b2fe-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b2fe-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b2fe-109">DESCRIPTION</span></span>
<span data-ttu-id="9b2fe-110">Das **Cmdlet Resume-AzSynapseSqlPool** setzt einen Azure Synapse Analytics SQL fort.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9b2fe-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b2fe-111">EXAMPLES</span></span>

### <span data-ttu-id="9b2fe-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9b2fe-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="9b2fe-113">Mit diesem Befehl wird ein angehaltener Azure Synapse Analytics SQL fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9b2fe-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9b2fe-114">PARAMETERS</span></span>

### <span data-ttu-id="9b2fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b2fe-115">-AsJob</span></span>
<span data-ttu-id="9b2fe-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9b2fe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b2fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2fe-117">-DefaultProfile</span></span>
<span data-ttu-id="9b2fe-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b2fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b2fe-119">-InputObject</span></span>
<span data-ttu-id="9b2fe-120">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2fe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9b2fe-121">-Name</span></span>
<span data-ttu-id="9b2fe-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2fe-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b2fe-123">-PassThru</span></span>
<span data-ttu-id="9b2fe-124">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9b2fe-125">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9b2fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b2fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b2fe-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2fe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b2fe-128">-ResourceId</span></span>
<span data-ttu-id="9b2fe-129">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2fe-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b2fe-130">-WorkspaceName</span></span>
<span data-ttu-id="9b2fe-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2fe-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9b2fe-132">-WorkspaceObject</span></span>
<span data-ttu-id="9b2fe-133">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2fe-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b2fe-134">-Confirm</span></span>
<span data-ttu-id="9b2fe-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b2fe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b2fe-136">-WhatIf</span></span>
<span data-ttu-id="9b2fe-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b2fe-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b2fe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2fe-139">CommonParameters</span></span>
<span data-ttu-id="9b2fe-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2fe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2fe-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b2fe-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2fe-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b2fe-142">INPUTS</span></span>

### <span data-ttu-id="9b2fe-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9b2fe-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9b2fe-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9b2fe-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9b2fe-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b2fe-145">OUTPUTS</span></span>

### <span data-ttu-id="9b2fe-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9b2fe-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9b2fe-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9b2fe-147">NOTES</span></span>

## <span data-ttu-id="9b2fe-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9b2fe-148">RELATED LINKS</span></span>
