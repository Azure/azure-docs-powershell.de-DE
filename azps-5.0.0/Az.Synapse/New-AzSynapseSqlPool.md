---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179500"
---
# <span data-ttu-id="5a3af-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5a3af-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="5a3af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a3af-102">SYNOPSIS</span></span>
<span data-ttu-id="5a3af-103">Erstellt einen Synapse Analytics SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="5a3af-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5a3af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a3af-104">SYNTAX</span></span>

### <span data-ttu-id="5a3af-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a3af-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a3af-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a3af-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a3af-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a3af-107">DESCRIPTION</span></span>
<span data-ttu-id="5a3af-108">Mit dem Cmdlet **New-AzSynapseSqlPool** wird ein Azure Synapse Analytics SQL-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a3af-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5a3af-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a3af-109">EXAMPLES</span></span>

### <span data-ttu-id="5a3af-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a3af-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="5a3af-111">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a3af-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5a3af-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a3af-112">PARAMETERS</span></span>

### <span data-ttu-id="5a3af-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a3af-113">-AsJob</span></span>
<span data-ttu-id="5a3af-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5a3af-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a3af-115">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="5a3af-115">-Collation</span></span>
<span data-ttu-id="5a3af-116">Sortierung definiert die Regeln, die Daten sortieren und vergleichen, und kann nach der SQL Pool-Erstellung nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5a3af-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="5a3af-117">Die Standardsortierung ist SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="5a3af-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="5a3af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a3af-118">-DefaultProfile</span></span>
<span data-ttu-id="5a3af-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a3af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a3af-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5a3af-120">-Name</span></span>
<span data-ttu-id="5a3af-121">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="5a3af-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a3af-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="5a3af-122">-PerformanceLevel</span></span>
<span data-ttu-id="5a3af-123">Die SQL-Dienstebene und die Leistungsstufe, die dem SQL-Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a3af-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="5a3af-124">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="5a3af-124">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a3af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a3af-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a3af-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a3af-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a3af-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a3af-127">-Tag</span></span>
<span data-ttu-id="5a3af-128">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5a3af-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5a3af-129">-Version</span><span class="sxs-lookup"><span data-stu-id="5a3af-129">-Version</span></span>
<span data-ttu-id="5a3af-130">Version des Synapse SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="5a3af-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="5a3af-131">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="5a3af-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="5a3af-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5a3af-132">-WorkspaceName</span></span>
<span data-ttu-id="5a3af-133">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="5a3af-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a3af-134">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5a3af-134">-WorkspaceObject</span></span>
<span data-ttu-id="5a3af-135">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="5a3af-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a3af-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a3af-136">-Confirm</span></span>
<span data-ttu-id="5a3af-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a3af-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a3af-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a3af-138">-WhatIf</span></span>
<span data-ttu-id="5a3af-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a3af-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a3af-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a3af-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a3af-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a3af-141">CommonParameters</span></span>
<span data-ttu-id="5a3af-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a3af-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a3af-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a3af-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a3af-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a3af-144">INPUTS</span></span>

### <span data-ttu-id="5a3af-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5a3af-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5a3af-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a3af-146">OUTPUTS</span></span>

### <span data-ttu-id="5a3af-147">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5a3af-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5a3af-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a3af-148">NOTES</span></span>

## <span data-ttu-id="5a3af-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a3af-149">RELATED LINKS</span></span>
