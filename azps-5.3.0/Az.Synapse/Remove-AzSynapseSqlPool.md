---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 37ece1d86c4b41dbf8a185c0d4ed5d7117db8b2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383367"
---
# <span data-ttu-id="ee52f-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ee52f-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="ee52f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee52f-102">SYNOPSIS</span></span>
<span data-ttu-id="ee52f-103">Löscht einen Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="ee52f-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ee52f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee52f-104">SYNTAX</span></span>

### <span data-ttu-id="ee52f-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee52f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee52f-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee52f-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee52f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee52f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee52f-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee52f-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee52f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee52f-109">DESCRIPTION</span></span>
<span data-ttu-id="ee52f-110">Mit **dem Cmdlet "Remove-AzSynapseSqlPool"** wird ein Azure Synapse Analytics SQL gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee52f-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ee52f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ee52f-111">EXAMPLES</span></span>

### <span data-ttu-id="ee52f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ee52f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="ee52f-113">Mit diesem Befehl wird ein Azure Synapse Analytics SQL gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee52f-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="ee52f-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ee52f-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="ee52f-115">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee52f-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="ee52f-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ee52f-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="ee52f-117">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee52f-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="ee52f-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ee52f-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="ee52f-119">Mit diesem Befehl wird ein Azure Synapse Analytics SQL mit der angegebenen Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee52f-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="ee52f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee52f-120">PARAMETERS</span></span>

### <span data-ttu-id="ee52f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee52f-121">-AsJob</span></span>
<span data-ttu-id="ee52f-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ee52f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee52f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee52f-123">-DefaultProfile</span></span>
<span data-ttu-id="ee52f-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee52f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee52f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ee52f-125">-Force</span></span>
<span data-ttu-id="ee52f-126">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="ee52f-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ee52f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee52f-127">-InputObject</span></span>
<span data-ttu-id="ee52f-128">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee52f-128">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee52f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ee52f-129">-Name</span></span>
<span data-ttu-id="ee52f-130">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="ee52f-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee52f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee52f-131">-PassThru</span></span>
<span data-ttu-id="ee52f-132">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ee52f-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ee52f-133">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="ee52f-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ee52f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee52f-134">-ResourceGroupName</span></span>
<span data-ttu-id="ee52f-135">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ee52f-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee52f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee52f-136">-ResourceId</span></span>
<span data-ttu-id="ee52f-137">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="ee52f-137">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee52f-138">-Version</span><span class="sxs-lookup"><span data-stu-id="ee52f-138">-Version</span></span>
<span data-ttu-id="ee52f-139">Version des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="ee52f-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="ee52f-140">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="ee52f-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="ee52f-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ee52f-141">-WorkspaceName</span></span>
<span data-ttu-id="ee52f-142">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ee52f-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee52f-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ee52f-143">-WorkspaceObject</span></span>
<span data-ttu-id="ee52f-144">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee52f-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee52f-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee52f-145">-Confirm</span></span>
<span data-ttu-id="ee52f-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee52f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee52f-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ee52f-147">-WhatIf</span></span>
<span data-ttu-id="ee52f-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee52f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee52f-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee52f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee52f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee52f-150">CommonParameters</span></span>
<span data-ttu-id="ee52f-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee52f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee52f-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee52f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee52f-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ee52f-153">INPUTS</span></span>

### <span data-ttu-id="ee52f-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ee52f-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ee52f-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ee52f-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="ee52f-156">System.String</span><span class="sxs-lookup"><span data-stu-id="ee52f-156">System.String</span></span>

## <span data-ttu-id="ee52f-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ee52f-157">OUTPUTS</span></span>

### <span data-ttu-id="ee52f-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee52f-158">System.Boolean</span></span>

## <span data-ttu-id="ee52f-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ee52f-159">NOTES</span></span>

## <span data-ttu-id="ee52f-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ee52f-160">RELATED LINKS</span></span>
