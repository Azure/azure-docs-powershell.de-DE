---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176521"
---
# <span data-ttu-id="022b9-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="022b9-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="022b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="022b9-102">SYNOPSIS</span></span>
<span data-ttu-id="022b9-103">Aktualisiert einen Synapse Analytics SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="022b9-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="022b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="022b9-104">SYNTAX</span></span>

### <span data-ttu-id="022b9-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="022b9-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022b9-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="022b9-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022b9-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="022b9-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022b9-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="022b9-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="022b9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="022b9-109">DESCRIPTION</span></span>
<span data-ttu-id="022b9-110">Das Cmdlet **Update-AzSynapseSqlPool** aktualisiert einen Azure Synapse Analytics SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="022b9-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="022b9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="022b9-111">EXAMPLES</span></span>

### <span data-ttu-id="022b9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="022b9-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="022b9-113">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="022b9-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="022b9-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="022b9-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="022b9-115">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool durch Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="022b9-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="022b9-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="022b9-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="022b9-117">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool durch Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="022b9-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="022b9-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="022b9-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="022b9-119">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool mit Ressourcen-ID aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="022b9-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="022b9-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="022b9-120">PARAMETERS</span></span>

### <span data-ttu-id="022b9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="022b9-121">-AsJob</span></span>
<span data-ttu-id="022b9-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="022b9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="022b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="022b9-123">-DefaultProfile</span></span>
<span data-ttu-id="022b9-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="022b9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="022b9-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="022b9-125">-InputObject</span></span>
<span data-ttu-id="022b9-126">SQL-Pool Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="022b9-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="022b9-127">-Name</span><span class="sxs-lookup"><span data-stu-id="022b9-127">-Name</span></span>
<span data-ttu-id="022b9-128">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="022b9-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="022b9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="022b9-129">-PassThru</span></span>
<span data-ttu-id="022b9-130">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="022b9-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="022b9-131">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="022b9-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="022b9-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="022b9-132">-PerformanceLevel</span></span>
<span data-ttu-id="022b9-133">Die SQL-Dienstebene und die Leistungsstufe, die dem SQL-Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="022b9-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="022b9-134">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="022b9-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="022b9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="022b9-135">-ResourceGroupName</span></span>
<span data-ttu-id="022b9-136">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="022b9-136">Resource group name.</span></span>

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

### <span data-ttu-id="022b9-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="022b9-137">-ResourceId</span></span>
<span data-ttu-id="022b9-138">Ressourcen-ID des Synapse-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="022b9-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="022b9-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="022b9-139">-Tag</span></span>
<span data-ttu-id="022b9-140">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="022b9-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="022b9-141">-Version</span><span class="sxs-lookup"><span data-stu-id="022b9-141">-Version</span></span>
<span data-ttu-id="022b9-142">Version des Synapse SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="022b9-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="022b9-143">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="022b9-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="022b9-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="022b9-144">-WorkspaceName</span></span>
<span data-ttu-id="022b9-145">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="022b9-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="022b9-146">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="022b9-146">-WorkspaceObject</span></span>
<span data-ttu-id="022b9-147">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="022b9-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="022b9-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="022b9-148">-Confirm</span></span>
<span data-ttu-id="022b9-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="022b9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="022b9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="022b9-150">-WhatIf</span></span>
<span data-ttu-id="022b9-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="022b9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="022b9-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="022b9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="022b9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="022b9-153">CommonParameters</span></span>
<span data-ttu-id="022b9-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="022b9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="022b9-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="022b9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="022b9-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="022b9-156">INPUTS</span></span>

### <span data-ttu-id="022b9-157">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="022b9-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="022b9-158">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="022b9-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="022b9-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="022b9-159">OUTPUTS</span></span>

### <span data-ttu-id="022b9-160">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="022b9-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="022b9-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="022b9-161">NOTES</span></span>

## <span data-ttu-id="022b9-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="022b9-162">RELATED LINKS</span></span>
