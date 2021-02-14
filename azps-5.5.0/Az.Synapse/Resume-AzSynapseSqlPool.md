---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ff2a68d7e0ae0ad94f685bbe1cfb795f7cd6a706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149908"
---
# <span data-ttu-id="434fc-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="434fc-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="434fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="434fc-102">SYNOPSIS</span></span>
<span data-ttu-id="434fc-103">Setzt einen Synapse Analytics SQL fort.</span><span class="sxs-lookup"><span data-stu-id="434fc-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="434fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="434fc-104">SYNTAX</span></span>

### <span data-ttu-id="434fc-105">ResumeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="434fc-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="434fc-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="434fc-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="434fc-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="434fc-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="434fc-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="434fc-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="434fc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="434fc-109">DESCRIPTION</span></span>
<span data-ttu-id="434fc-110">Das **Cmdlet "Resume-AzSynapseSqlPool"** setzt einen Azure Synapse Analytics SQL fort.</span><span class="sxs-lookup"><span data-stu-id="434fc-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="434fc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="434fc-111">EXAMPLES</span></span>

### <span data-ttu-id="434fc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="434fc-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="434fc-113">Dieser Befehl setzt einen angehaltenen Azure Synapse Analytics SQL fort.</span><span class="sxs-lookup"><span data-stu-id="434fc-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="434fc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="434fc-114">PARAMETERS</span></span>

### <span data-ttu-id="434fc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="434fc-115">-AsJob</span></span>
<span data-ttu-id="434fc-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="434fc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="434fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434fc-117">-DefaultProfile</span></span>
<span data-ttu-id="434fc-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="434fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434fc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="434fc-119">-InputObject</span></span>
<span data-ttu-id="434fc-120">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="434fc-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="434fc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="434fc-121">-Name</span></span>
<span data-ttu-id="434fc-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="434fc-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="434fc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="434fc-123">-PassThru</span></span>
<span data-ttu-id="434fc-124">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="434fc-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="434fc-125">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="434fc-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="434fc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434fc-126">-ResourceGroupName</span></span>
<span data-ttu-id="434fc-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="434fc-127">Resource group name.</span></span>

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

### <span data-ttu-id="434fc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="434fc-128">-ResourceId</span></span>
<span data-ttu-id="434fc-129">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="434fc-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="434fc-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="434fc-130">-WorkspaceName</span></span>
<span data-ttu-id="434fc-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="434fc-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="434fc-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="434fc-132">-WorkspaceObject</span></span>
<span data-ttu-id="434fc-133">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="434fc-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="434fc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="434fc-134">-Confirm</span></span>
<span data-ttu-id="434fc-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="434fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="434fc-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="434fc-136">-WhatIf</span></span>
<span data-ttu-id="434fc-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="434fc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="434fc-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="434fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="434fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434fc-139">CommonParameters</span></span>
<span data-ttu-id="434fc-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="434fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434fc-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="434fc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434fc-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="434fc-142">INPUTS</span></span>

### <span data-ttu-id="434fc-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="434fc-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="434fc-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="434fc-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="434fc-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="434fc-145">OUTPUTS</span></span>

### <span data-ttu-id="434fc-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="434fc-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="434fc-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="434fc-147">NOTES</span></span>

## <span data-ttu-id="434fc-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="434fc-148">RELATED LINKS</span></span>
