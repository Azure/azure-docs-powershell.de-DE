---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174916"
---
# <span data-ttu-id="2b63a-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="2b63a-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="2b63a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b63a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b63a-103">Entfernt die erweiterten Threat Protection-Einstellungen aus einem SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="2b63a-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="2b63a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b63a-104">SYNTAX</span></span>

### <span data-ttu-id="2b63a-105">ClearByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b63a-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b63a-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b63a-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b63a-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b63a-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b63a-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b63a-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b63a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b63a-109">DESCRIPTION</span></span>
<span data-ttu-id="2b63a-110">Das **Cmdlet "Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting"** entfernt die erweiterten Threat Protection-Einstellungen aus einem Azure Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="2b63a-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2b63a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b63a-111">EXAMPLES</span></span>

### <span data-ttu-id="2b63a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2b63a-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="2b63a-113">Mit diesem Befehl werden die erweiterten Threat Protection-Einstellungen aus SQL "ContosoSqlPool" im Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="2b63a-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2b63a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b63a-114">PARAMETERS</span></span>

### <span data-ttu-id="2b63a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b63a-115">-AsJob</span></span>
<span data-ttu-id="2b63a-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2b63a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b63a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b63a-117">-DefaultProfile</span></span>
<span data-ttu-id="2b63a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b63a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b63a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b63a-119">-InputObject</span></span>
<span data-ttu-id="2b63a-120">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2b63a-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b63a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2b63a-121">-Name</span></span>
<span data-ttu-id="2b63a-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="2b63a-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet, ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b63a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b63a-123">-PassThru</span></span>
<span data-ttu-id="2b63a-124">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2b63a-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2b63a-125">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="2b63a-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2b63a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b63a-126">-ResourceGroupName</span></span>
<span data-ttu-id="2b63a-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2b63a-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b63a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b63a-128">-ResourceId</span></span>
<span data-ttu-id="2b63a-129">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="2b63a-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b63a-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2b63a-130">-WorkspaceName</span></span>
<span data-ttu-id="2b63a-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2b63a-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b63a-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2b63a-132">-WorkspaceObject</span></span>
<span data-ttu-id="2b63a-133">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2b63a-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b63a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b63a-134">-Confirm</span></span>
<span data-ttu-id="2b63a-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b63a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b63a-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2b63a-136">-WhatIf</span></span>
<span data-ttu-id="2b63a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b63a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b63a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b63a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b63a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b63a-139">CommonParameters</span></span>
<span data-ttu-id="2b63a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b63a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b63a-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b63a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b63a-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b63a-142">INPUTS</span></span>

### <span data-ttu-id="2b63a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b63a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2b63a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2b63a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="2b63a-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b63a-145">OUTPUTS</span></span>

### <span data-ttu-id="2b63a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b63a-146">System.Boolean</span></span>

## <span data-ttu-id="2b63a-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2b63a-147">NOTES</span></span>

## <span data-ttu-id="2b63a-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2b63a-148">RELATED LINKS</span></span>
