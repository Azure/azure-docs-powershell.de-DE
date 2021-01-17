---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292318"
---
# <span data-ttu-id="f72c1-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="f72c1-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="f72c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f72c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f72c1-103">Entfernt die Überwachungseinstellungen eines Azure Synapse Analytics SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="f72c1-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f72c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f72c1-104">SYNTAX</span></span>

### <span data-ttu-id="f72c1-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f72c1-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f72c1-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f72c1-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f72c1-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f72c1-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f72c1-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f72c1-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f72c1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f72c1-109">DESCRIPTION</span></span>
<span data-ttu-id="f72c1-110">Das **Cmdlet "Reset-AzSynapseSqlPoolAuditSetting"** entfernt die Überwachungseinstellungen eines Azure Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="f72c1-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f72c1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f72c1-111">EXAMPLES</span></span>

### <span data-ttu-id="f72c1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f72c1-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f72c1-113">Mit diesem Befehl werden die Überwachungseinstellungen eines SQL "ContosoSqlPool" im Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f72c1-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f72c1-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f72c1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="f72c1-115">Mit diesem Befehl werden die Überwachungseinstellungen eines SQL "ContosoSqlPool" im Arbeitsbereich "ContosoWorkspace" über die Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="f72c1-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f72c1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f72c1-116">PARAMETERS</span></span>

### <span data-ttu-id="f72c1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f72c1-117">-AsJob</span></span>
<span data-ttu-id="f72c1-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f72c1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f72c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72c1-119">-DefaultProfile</span></span>
<span data-ttu-id="f72c1-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f72c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f72c1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f72c1-121">-InputObject</span></span>
<span data-ttu-id="f72c1-122">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f72c1-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f72c1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f72c1-123">-Name</span></span>
<span data-ttu-id="f72c1-124">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="f72c1-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72c1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f72c1-125">-PassThru</span></span>
<span data-ttu-id="f72c1-126">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f72c1-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f72c1-127">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="f72c1-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f72c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f72c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="f72c1-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f72c1-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72c1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f72c1-130">-ResourceId</span></span>
<span data-ttu-id="f72c1-131">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="f72c1-131">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72c1-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f72c1-132">-WorkspaceName</span></span>
<span data-ttu-id="f72c1-133">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f72c1-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72c1-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f72c1-134">-WorkspaceObject</span></span>
<span data-ttu-id="f72c1-135">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f72c1-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f72c1-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f72c1-136">-Confirm</span></span>
<span data-ttu-id="f72c1-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f72c1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f72c1-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f72c1-138">-WhatIf</span></span>
<span data-ttu-id="f72c1-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f72c1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f72c1-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f72c1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f72c1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72c1-141">CommonParameters</span></span>
<span data-ttu-id="f72c1-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72c1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72c1-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f72c1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72c1-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f72c1-144">INPUTS</span></span>

### <span data-ttu-id="f72c1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f72c1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f72c1-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f72c1-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f72c1-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f72c1-147">OUTPUTS</span></span>

### <span data-ttu-id="f72c1-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f72c1-148">System.Boolean</span></span>

## <span data-ttu-id="f72c1-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f72c1-149">NOTES</span></span>

## <span data-ttu-id="f72c1-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f72c1-150">RELATED LINKS</span></span>
