---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: fe13a82a6662b0f8e9578f4f0fd5143b350538c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922592"
---
# <span data-ttu-id="0a1fc-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a1fc-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="0a1fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1fc-103">Aktualisiert einen Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a1fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a1fc-104">SYNTAX</span></span>

### <span data-ttu-id="0a1fc-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a1fc-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1fc-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a1fc-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1fc-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a1fc-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1fc-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a1fc-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a1fc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a1fc-109">DESCRIPTION</span></span>
<span data-ttu-id="0a1fc-110">Das **Update-AzSynapseSqlPool-Cmdlet** aktualisiert einen Azure Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a1fc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a1fc-111">EXAMPLES</span></span>

### <span data-ttu-id="0a1fc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a1fc-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="0a1fc-113">Mit diesem Befehl wird ein Azure Synapse Analytics SQL aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="0a1fc-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0a1fc-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="0a1fc-115">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="0a1fc-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0a1fc-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="0a1fc-117">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="0a1fc-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="0a1fc-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="0a1fc-119">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool mit Ressourcen-ID aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="0a1fc-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0a1fc-120">PARAMETERS</span></span>

### <span data-ttu-id="0a1fc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a1fc-121">-AsJob</span></span>
<span data-ttu-id="0a1fc-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0a1fc-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a1fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a1fc-123">-DefaultProfile</span></span>
<span data-ttu-id="0a1fc-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a1fc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a1fc-125">-InputObject</span></span>
<span data-ttu-id="0a1fc-126">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0a1fc-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0a1fc-127">-Name</span></span>
<span data-ttu-id="0a1fc-128">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="0a1fc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a1fc-129">-PassThru</span></span>
<span data-ttu-id="0a1fc-130">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0a1fc-131">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0a1fc-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="0a1fc-132">-PerformanceLevel</span></span>
<span data-ttu-id="0a1fc-133">Die SQL Dienstebene und -leistungsstufe, die dem Pool zugewiesen SQL werden.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="0a1fc-134">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="0a1fc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a1fc-135">-ResourceGroupName</span></span>
<span data-ttu-id="0a1fc-136">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-136">Resource group name.</span></span>

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

### <span data-ttu-id="0a1fc-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a1fc-137">-ResourceId</span></span>
<span data-ttu-id="0a1fc-138">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="0a1fc-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a1fc-139">-Tag</span></span>
<span data-ttu-id="0a1fc-140">Eine Zeichenfolge, ein Zeichenfolgenwörterbuch mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="0a1fc-141">-Version</span><span class="sxs-lookup"><span data-stu-id="0a1fc-141">-Version</span></span>
<span data-ttu-id="0a1fc-142">Version von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="0a1fc-143">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="0a1fc-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a1fc-144">-WorkspaceName</span></span>
<span data-ttu-id="0a1fc-145">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0a1fc-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0a1fc-146">-WorkspaceObject</span></span>
<span data-ttu-id="0a1fc-147">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0a1fc-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a1fc-148">-Confirm</span></span>
<span data-ttu-id="0a1fc-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a1fc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a1fc-150">-WhatIf</span></span>
<span data-ttu-id="0a1fc-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a1fc-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a1fc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1fc-153">CommonParameters</span></span>
<span data-ttu-id="0a1fc-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1fc-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a1fc-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1fc-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a1fc-156">INPUTS</span></span>

### <span data-ttu-id="0a1fc-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a1fc-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0a1fc-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a1fc-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0a1fc-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a1fc-159">OUTPUTS</span></span>

### <span data-ttu-id="0a1fc-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a1fc-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0a1fc-161">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0a1fc-161">NOTES</span></span>

## <span data-ttu-id="0a1fc-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0a1fc-162">RELATED LINKS</span></span>
