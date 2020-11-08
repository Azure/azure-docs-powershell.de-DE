---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cd715bed20477fae4cbb17d033fd67fefa4e1cdc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173365"
---
# <span data-ttu-id="44997-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="44997-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="44997-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44997-102">SYNOPSIS</span></span>
<span data-ttu-id="44997-103">Löscht einen Synapse Analytics SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="44997-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="44997-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44997-104">SYNTAX</span></span>

### <span data-ttu-id="44997-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="44997-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44997-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44997-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44997-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44997-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44997-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44997-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44997-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44997-109">DESCRIPTION</span></span>
<span data-ttu-id="44997-110">Mit dem Cmdlet **Remove-AzSynapseSqlPool** wird ein Azure Synapse Analytics SQL-Pool endgültig gelöscht.</span><span class="sxs-lookup"><span data-stu-id="44997-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="44997-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44997-111">EXAMPLES</span></span>

### <span data-ttu-id="44997-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44997-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="44997-113">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="44997-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="44997-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="44997-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="44997-115">Dieser Befehl löscht einen Azure Synapse Analytics SQL-Pool durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="44997-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="44997-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="44997-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="44997-117">Dieser Befehl löscht einen Azure Synapse Analytics SQL-Pool durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="44997-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="44997-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="44997-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="44997-119">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool mit der angegebenen Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="44997-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="44997-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="44997-120">PARAMETERS</span></span>

### <span data-ttu-id="44997-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44997-121">-AsJob</span></span>
<span data-ttu-id="44997-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="44997-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44997-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44997-123">-DefaultProfile</span></span>
<span data-ttu-id="44997-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44997-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44997-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="44997-125">-InputObject</span></span>
<span data-ttu-id="44997-126">SQL-Pool Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="44997-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="44997-127">-Name</span><span class="sxs-lookup"><span data-stu-id="44997-127">-Name</span></span>
<span data-ttu-id="44997-128">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="44997-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="44997-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44997-129">-PassThru</span></span>
<span data-ttu-id="44997-130">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="44997-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="44997-131">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="44997-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="44997-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44997-132">-ResourceGroupName</span></span>
<span data-ttu-id="44997-133">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="44997-133">Resource group name.</span></span>

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

### <span data-ttu-id="44997-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="44997-134">-ResourceId</span></span>
<span data-ttu-id="44997-135">Ressourcen-ID des Synapse-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="44997-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="44997-136">-Version</span><span class="sxs-lookup"><span data-stu-id="44997-136">-Version</span></span>
<span data-ttu-id="44997-137">Version des Synapse SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="44997-137">Version of Synapse SQL pool.</span></span> <span data-ttu-id="44997-138">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="44997-138">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="44997-139">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44997-139">-WorkspaceName</span></span>
<span data-ttu-id="44997-140">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="44997-140">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="44997-141">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="44997-141">-WorkspaceObject</span></span>
<span data-ttu-id="44997-142">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="44997-142">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="44997-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44997-143">-Confirm</span></span>
<span data-ttu-id="44997-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44997-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44997-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44997-145">-WhatIf</span></span>
<span data-ttu-id="44997-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44997-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44997-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44997-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44997-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44997-148">CommonParameters</span></span>
<span data-ttu-id="44997-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44997-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44997-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44997-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44997-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44997-151">INPUTS</span></span>

### <span data-ttu-id="44997-152">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="44997-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="44997-153">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="44997-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="44997-154">System. String</span><span class="sxs-lookup"><span data-stu-id="44997-154">System.String</span></span>

## <span data-ttu-id="44997-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44997-155">OUTPUTS</span></span>

### <span data-ttu-id="44997-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44997-156">System.Boolean</span></span>

## <span data-ttu-id="44997-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="44997-157">NOTES</span></span>

## <span data-ttu-id="44997-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44997-158">RELATED LINKS</span></span>
