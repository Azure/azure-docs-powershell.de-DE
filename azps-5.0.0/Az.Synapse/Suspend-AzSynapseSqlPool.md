---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175369"
---
# <span data-ttu-id="c5632-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c5632-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="c5632-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5632-102">SYNOPSIS</span></span>
<span data-ttu-id="c5632-103">Unterbricht einen Synapse Analytics SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="c5632-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c5632-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5632-104">SYNTAX</span></span>

### <span data-ttu-id="c5632-105">SuspendByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5632-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5632-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5632-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5632-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5632-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5632-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5632-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5632-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5632-109">DESCRIPTION</span></span>
<span data-ttu-id="c5632-110">Mit dem Cmdlet **Suspend-AzSynapseSqlPool** wird ein Azure Synapse Analytics SQL-Pool angehalten.</span><span class="sxs-lookup"><span data-stu-id="c5632-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c5632-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5632-111">EXAMPLES</span></span>

### <span data-ttu-id="c5632-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5632-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="c5632-113">Dieser Befehl unterbricht einen Active Azure Synapse Analytics SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="c5632-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c5632-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5632-114">PARAMETERS</span></span>

### <span data-ttu-id="c5632-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5632-115">-AsJob</span></span>
<span data-ttu-id="c5632-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c5632-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5632-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5632-117">-DefaultProfile</span></span>
<span data-ttu-id="c5632-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5632-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5632-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c5632-119">-InputObject</span></span>
<span data-ttu-id="c5632-120">SQL-Pool Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="c5632-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5632-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c5632-121">-Name</span></span>
<span data-ttu-id="c5632-122">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="c5632-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5632-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5632-123">-PassThru</span></span>
<span data-ttu-id="c5632-124">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c5632-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c5632-125">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c5632-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c5632-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5632-126">-ResourceGroupName</span></span>
<span data-ttu-id="c5632-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c5632-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5632-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c5632-128">-ResourceId</span></span>
<span data-ttu-id="c5632-129">Ressourcen-ID des Synapse-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="c5632-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5632-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5632-130">-WorkspaceName</span></span>
<span data-ttu-id="c5632-131">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c5632-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5632-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c5632-132">-WorkspaceObject</span></span>
<span data-ttu-id="c5632-133">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="c5632-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5632-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5632-134">-Confirm</span></span>
<span data-ttu-id="c5632-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5632-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5632-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5632-136">-WhatIf</span></span>
<span data-ttu-id="c5632-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5632-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5632-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5632-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5632-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5632-139">CommonParameters</span></span>
<span data-ttu-id="c5632-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5632-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5632-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5632-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5632-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5632-142">INPUTS</span></span>

### <span data-ttu-id="c5632-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5632-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c5632-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c5632-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c5632-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5632-145">OUTPUTS</span></span>

### <span data-ttu-id="c5632-146">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c5632-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c5632-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5632-147">NOTES</span></span>

## <span data-ttu-id="c5632-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5632-148">RELATED LINKS</span></span>
