---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: e9c4c68f794b5ea0c20b0e1fe57677b329b02622
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299864"
---
# <span data-ttu-id="9ec58-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9ec58-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="9ec58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ec58-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec58-103">Löscht einen Synapse Analytics SQL Poolwiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="9ec58-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="9ec58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ec58-104">SYNTAX</span></span>

### <span data-ttu-id="9ec58-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ec58-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String> -Name <String> 
[-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec58-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec58-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -Name <String> -SqlPoolObject <PSSynapseSqlPool> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec58-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec58-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec58-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec58-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ec58-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ec58-109">DESCRIPTION</span></span>
<span data-ttu-id="9ec58-110">Das **Cmdlet "Remove-AzSynapseSqlPoolRestorePoint"** löscht einen Azure Synapse Analytics SQL Poolwiederherstellungspunkt dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="9ec58-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="9ec58-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ec58-111">EXAMPLES</span></span>

### <span data-ttu-id="9ec58-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ec58-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="9ec58-113">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Wiederherstellungspunkt des Pools gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9ec58-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="9ec58-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9ec58-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="9ec58-115">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Poolwiederherstellungspunkt über die Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9ec58-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="9ec58-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9ec58-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="9ec58-117">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Poolwiederherstellungspunkt über die Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9ec58-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="9ec58-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="9ec58-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="9ec58-119">Mit diesem Befehl wird ein Azure Synapse Analytics-SQL-Wiederherstellungspunkt mit der angegebenen Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9ec58-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="9ec58-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ec58-120">PARAMETERS</span></span>

### <span data-ttu-id="9ec58-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ec58-121">-AsJob</span></span>
<span data-ttu-id="9ec58-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9ec58-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ec58-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9ec58-123">-Force</span></span>
<span data-ttu-id="9ec58-124">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="9ec58-124">Do not ask for confirmation.</span></span>

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


### <span data-ttu-id="9ec58-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ec58-125">-InputObject</span></span>
<span data-ttu-id="9ec58-126">SQL eingabeobjekt für die Erstellungszeit des Poolwiederherstellungspunkts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ec58-126">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec58-127">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="9ec58-127">-RestorePointCreationDate</span></span>
<span data-ttu-id="9ec58-128">Name von "Synapse" SQL Erstellungsdatum des Wiederherstellungspunkts.</span><span class="sxs-lookup"><span data-stu-id="9ec58-128">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec58-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ec58-129">-PassThru</span></span>
<span data-ttu-id="9ec58-130">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9ec58-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9ec58-131">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="9ec58-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9ec58-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec58-132">-ResourceGroupName</span></span>
<span data-ttu-id="9ec58-133">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9ec58-133">Resource group name.</span></span>

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

### <span data-ttu-id="9ec58-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ec58-134">-ResourceId</span></span>
<span data-ttu-id="9ec58-135">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="9ec58-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="9ec58-136">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9ec58-136">-SqlPoolName</span></span>
<span data-ttu-id="9ec58-137">Name des Synapse Sql-Pools.</span><span class="sxs-lookup"><span data-stu-id="9ec58-137">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="9ec58-138">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9ec58-138">-SqlPoolObject</span></span>
<span data-ttu-id="9ec58-139">Sql Pool-Eingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ec58-139">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec58-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ec58-140">-WorkspaceName</span></span>
<span data-ttu-id="9ec58-141">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="9ec58-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9ec58-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9ec58-142">-WorkspaceObject</span></span>
<span data-ttu-id="9ec58-143">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ec58-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9ec58-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ec58-144">-Confirm</span></span>
<span data-ttu-id="9ec58-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ec58-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ec58-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9ec58-146">-WhatIf</span></span>
<span data-ttu-id="9ec58-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec58-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ec58-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ec58-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ec58-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec58-149">CommonParameters</span></span>
<span data-ttu-id="9ec58-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec58-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec58-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ec58-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec58-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ec58-152">INPUTS</span></span>

### <span data-ttu-id="9ec58-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ec58-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9ec58-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9ec58-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="9ec58-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9ec58-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="9ec58-156">System.String</span><span class="sxs-lookup"><span data-stu-id="9ec58-156">System.String</span></span>

## <span data-ttu-id="9ec58-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ec58-157">OUTPUTS</span></span>

### <span data-ttu-id="9ec58-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ec58-158">System.Boolean</span></span>

## <span data-ttu-id="9ec58-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ec58-159">NOTES</span></span>

## <span data-ttu-id="9ec58-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ec58-160">RELATED LINKS</span></span>
