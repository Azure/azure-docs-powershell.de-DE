---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: bb653669ff15dad78ce3cec10f406aa099808e55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149985"
---
# <span data-ttu-id="963f1-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="963f1-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="963f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="963f1-102">SYNOPSIS</span></span>
<span data-ttu-id="963f1-103">Erstellt einen Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="963f1-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="963f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="963f1-104">SYNTAX</span></span>

### <span data-ttu-id="963f1-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="963f1-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="963f1-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="963f1-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="963f1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="963f1-107">DESCRIPTION</span></span>
<span data-ttu-id="963f1-108">Das **Cmdlet "New-AzSynapseSqlPool"** erstellt einen Azure Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="963f1-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="963f1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="963f1-109">EXAMPLES</span></span>

### <span data-ttu-id="963f1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="963f1-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="963f1-111">Mit diesem Befehl wird ein Azure Synapse Analytics SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="963f1-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="963f1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="963f1-112">PARAMETERS</span></span>

### <span data-ttu-id="963f1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="963f1-113">-AsJob</span></span>
<span data-ttu-id="963f1-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="963f1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="963f1-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="963f1-115">-Collation</span></span>
<span data-ttu-id="963f1-116">Die Sortierung definiert die Regeln zum Sortieren und Vergleichen von Daten und kann nach der Erstellung des SQL nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="963f1-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="963f1-117">Die Standardsortierung ist SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="963f1-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="963f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="963f1-118">-DefaultProfile</span></span>
<span data-ttu-id="963f1-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="963f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="963f1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="963f1-120">-Name</span></span>
<span data-ttu-id="963f1-121">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="963f1-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="963f1-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="963f1-122">-PerformanceLevel</span></span>
<span data-ttu-id="963f1-123">Die SQL Dienstebene und Leistungsstufe, die dem SQL werden soll.</span><span class="sxs-lookup"><span data-stu-id="963f1-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="963f1-124">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="963f1-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="963f1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="963f1-125">-ResourceGroupName</span></span>
<span data-ttu-id="963f1-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="963f1-126">Resource group name.</span></span>

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

### <span data-ttu-id="963f1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="963f1-127">-Tag</span></span>
<span data-ttu-id="963f1-128">Ein Zeichenfolgenverzeichnis mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="963f1-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="963f1-129">-Version</span><span class="sxs-lookup"><span data-stu-id="963f1-129">-Version</span></span>
<span data-ttu-id="963f1-130">Version des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="963f1-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="963f1-131">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="963f1-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="963f1-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="963f1-132">-WorkspaceName</span></span>
<span data-ttu-id="963f1-133">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="963f1-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="963f1-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="963f1-134">-WorkspaceObject</span></span>
<span data-ttu-id="963f1-135">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="963f1-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="963f1-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="963f1-136">-Confirm</span></span>
<span data-ttu-id="963f1-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="963f1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="963f1-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="963f1-138">-WhatIf</span></span>
<span data-ttu-id="963f1-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="963f1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="963f1-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="963f1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="963f1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="963f1-141">CommonParameters</span></span>
<span data-ttu-id="963f1-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="963f1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="963f1-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="963f1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="963f1-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="963f1-144">INPUTS</span></span>

### <span data-ttu-id="963f1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="963f1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="963f1-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="963f1-146">OUTPUTS</span></span>

### <span data-ttu-id="963f1-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="963f1-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="963f1-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="963f1-148">NOTES</span></span>

## <span data-ttu-id="963f1-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="963f1-149">RELATED LINKS</span></span>
