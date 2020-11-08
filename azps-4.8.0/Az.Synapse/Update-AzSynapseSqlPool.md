---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173663"
---
# <span data-ttu-id="9f5f2-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9f5f2-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="9f5f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f5f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5f2-103">Aktualisiert einen Synapse Analytics SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9f5f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f5f2-104">SYNTAX</span></span>

### <span data-ttu-id="9f5f2-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f5f2-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-112">PauseByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-114">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5f2-116">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5f2-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f5f2-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f5f2-117">DESCRIPTION</span></span>
<span data-ttu-id="9f5f2-118">Das Cmdlet **Update-AzSynapseSqlPool** aktualisiert einen Azure Synapse Analytics SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9f5f2-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f5f2-119">EXAMPLES</span></span>

### <span data-ttu-id="9f5f2-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f5f2-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="9f5f2-121">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="9f5f2-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9f5f2-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="9f5f2-123">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool durch Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="9f5f2-124">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9f5f2-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="9f5f2-125">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool durch Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="9f5f2-126">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="9f5f2-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="9f5f2-127">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool mit Ressourcen-ID aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="9f5f2-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f5f2-128">PARAMETERS</span></span>

### <span data-ttu-id="9f5f2-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f5f2-129">-AsJob</span></span>
<span data-ttu-id="9f5f2-130">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9f5f2-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f5f2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5f2-131">-DefaultProfile</span></span>
<span data-ttu-id="9f5f2-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f5f2-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9f5f2-133">-InputObject</span></span>
<span data-ttu-id="9f5f2-134">SQL-Pool Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-135">-Name</span><span class="sxs-lookup"><span data-stu-id="9f5f2-135">-Name</span></span>
<span data-ttu-id="9f5f2-136">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f5f2-137">-PassThru</span></span>
<span data-ttu-id="9f5f2-138">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9f5f2-139">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9f5f2-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="9f5f2-140">-PerformanceLevel</span></span>
<span data-ttu-id="9f5f2-141">Die SQL-Dienstebene und die Leistungsstufe, die dem SQL-Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="9f5f2-142">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5f2-143">-ResourceGroupName</span></span>
<span data-ttu-id="9f5f2-144">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-145">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9f5f2-145">-ResourceId</span></span>
<span data-ttu-id="9f5f2-146">Ressourcen-ID des Synapse-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-147">-Resume</span><span class="sxs-lookup"><span data-stu-id="9f5f2-147">-Resume</span></span>
<span data-ttu-id="9f5f2-148">Gibt an, dass der SQL-Pool fortgesetzt wird</span><span class="sxs-lookup"><span data-stu-id="9f5f2-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-149">-Suspend</span><span class="sxs-lookup"><span data-stu-id="9f5f2-149">-Suspend</span></span>
<span data-ttu-id="9f5f2-150">Gibt an, dass der SQL-Pool angehalten wird</span><span class="sxs-lookup"><span data-stu-id="9f5f2-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f5f2-151">-Tag</span></span>
<span data-ttu-id="9f5f2-152">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-153">-Version</span><span class="sxs-lookup"><span data-stu-id="9f5f2-153">-Version</span></span>
<span data-ttu-id="9f5f2-154">Version des Synapse SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="9f5f2-155">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-155">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-156">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9f5f2-156">-WorkspaceName</span></span>
<span data-ttu-id="9f5f2-157">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="9f5f2-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-158">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="9f5f2-158">-WorkspaceObject</span></span>
<span data-ttu-id="9f5f2-159">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f2-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f5f2-160">-Confirm</span></span>
<span data-ttu-id="9f5f2-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f5f2-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f5f2-162">-WhatIf</span></span>
<span data-ttu-id="9f5f2-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f5f2-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f5f2-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5f2-165">CommonParameters</span></span>
<span data-ttu-id="9f5f2-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f5f2-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5f2-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f5f2-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5f2-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f5f2-168">INPUTS</span></span>

### <span data-ttu-id="9f5f2-169">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9f5f2-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9f5f2-170">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9f5f2-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9f5f2-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f5f2-171">OUTPUTS</span></span>

### <span data-ttu-id="9f5f2-172">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9f5f2-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9f5f2-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f5f2-173">NOTES</span></span>

## <span data-ttu-id="9f5f2-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f5f2-174">RELATED LINKS</span></span>
