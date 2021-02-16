---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 25f9c829bd0f2557f4419bcc0c3b95c71a2e4b9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173500"
---
# <span data-ttu-id="406db-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="406db-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="406db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="406db-102">SYNOPSIS</span></span>
<span data-ttu-id="406db-103">Aktualisiert einen Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="406db-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="406db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="406db-104">SYNTAX</span></span>

### <span data-ttu-id="406db-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="406db-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="406db-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="406db-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="406db-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="406db-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="406db-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="406db-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="406db-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="406db-109">DESCRIPTION</span></span>
<span data-ttu-id="406db-110">Das **Cmdlet "Update-AzSynapseSqlPool"** aktualisiert einen Azure Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="406db-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="406db-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="406db-111">EXAMPLES</span></span>

### <span data-ttu-id="406db-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="406db-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="406db-113">Mit diesem Befehl wird ein Azure Synapse Analytics SQL aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="406db-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="406db-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="406db-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="406db-115">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="406db-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="406db-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="406db-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="406db-117">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="406db-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="406db-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="406db-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="406db-119">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Mit Ressourcen-ID aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="406db-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="406db-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="406db-120">PARAMETERS</span></span>

### <span data-ttu-id="406db-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="406db-121">-AsJob</span></span>
<span data-ttu-id="406db-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="406db-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="406db-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406db-123">-DefaultProfile</span></span>
<span data-ttu-id="406db-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="406db-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="406db-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="406db-125">-InputObject</span></span>
<span data-ttu-id="406db-126">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="406db-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="406db-127">-Name</span><span class="sxs-lookup"><span data-stu-id="406db-127">-Name</span></span>
<span data-ttu-id="406db-128">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="406db-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406db-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="406db-129">-PassThru</span></span>
<span data-ttu-id="406db-130">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="406db-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="406db-131">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="406db-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="406db-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="406db-132">-PerformanceLevel</span></span>
<span data-ttu-id="406db-133">Die SQL Dienstebene und Leistungsstufe, die dem SQL werden soll.</span><span class="sxs-lookup"><span data-stu-id="406db-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="406db-134">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="406db-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406db-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="406db-135">-ResourceGroupName</span></span>
<span data-ttu-id="406db-136">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="406db-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406db-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="406db-137">-ResourceId</span></span>
<span data-ttu-id="406db-138">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="406db-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406db-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="406db-139">-Tag</span></span>
<span data-ttu-id="406db-140">Ein Zeichenfolgenverzeichnis mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="406db-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406db-141">-Version</span><span class="sxs-lookup"><span data-stu-id="406db-141">-Version</span></span>
<span data-ttu-id="406db-142">Version des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="406db-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="406db-143">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="406db-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="406db-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="406db-144">-WorkspaceName</span></span>
<span data-ttu-id="406db-145">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="406db-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406db-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="406db-146">-WorkspaceObject</span></span>
<span data-ttu-id="406db-147">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="406db-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="406db-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="406db-148">-Confirm</span></span>
<span data-ttu-id="406db-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="406db-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="406db-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="406db-150">-WhatIf</span></span>
<span data-ttu-id="406db-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="406db-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="406db-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="406db-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="406db-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406db-153">CommonParameters</span></span>
<span data-ttu-id="406db-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="406db-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406db-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="406db-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406db-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="406db-156">INPUTS</span></span>

### <span data-ttu-id="406db-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="406db-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="406db-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="406db-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="406db-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="406db-159">OUTPUTS</span></span>

### <span data-ttu-id="406db-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="406db-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="406db-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="406db-161">NOTES</span></span>

## <span data-ttu-id="406db-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="406db-162">RELATED LINKS</span></span>
