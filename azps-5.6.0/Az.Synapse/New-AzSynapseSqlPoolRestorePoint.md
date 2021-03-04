---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 1f30dd8d0757e857934c1f8337e879cf1de8384e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924352"
---
# <span data-ttu-id="2049b-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="2049b-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="2049b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2049b-102">SYNOPSIS</span></span>
<span data-ttu-id="2049b-103">Erstellt einen neuen Wiederherstellungspunkt in einem Azure Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="2049b-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2049b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2049b-104">SYNTAX</span></span>

### <span data-ttu-id="2049b-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2049b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2049b-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2049b-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2049b-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2049b-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2049b-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2049b-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2049b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2049b-109">DESCRIPTION</span></span>
<span data-ttu-id="2049b-110">Das **Cmdlet New-AzSynapseSqlPoolRestorePoint** erstellt einen neuen Wiederherstellungspunkt, aus dem ein Azure Synapse Analytics SQL-Pool wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2049b-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="2049b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2049b-111">EXAMPLES</span></span>

### <span data-ttu-id="2049b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2049b-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="2049b-113">Mit diesem Befehl wird ein Wiederherstellungspunkt für SQL ContosoSqlPool im Arbeitsbereich ContosoWorkspace erstellt.</span><span class="sxs-lookup"><span data-stu-id="2049b-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="2049b-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2049b-114">PARAMETERS</span></span>

### <span data-ttu-id="2049b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2049b-115">-AsJob</span></span>
<span data-ttu-id="2049b-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2049b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2049b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2049b-117">-DefaultProfile</span></span>
<span data-ttu-id="2049b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2049b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2049b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2049b-119">-InputObject</span></span>
<span data-ttu-id="2049b-120">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2049b-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2049b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2049b-121">-Name</span></span>
<span data-ttu-id="2049b-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="2049b-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2049b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2049b-123">-ResourceGroupName</span></span>
<span data-ttu-id="2049b-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2049b-124">Resource group name.</span></span>

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

### <span data-ttu-id="2049b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2049b-125">-ResourceId</span></span>
<span data-ttu-id="2049b-126">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="2049b-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2049b-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="2049b-127">-RestorePointLabel</span></span>
<span data-ttu-id="2049b-128">Die Bezeichnung, der wir einen Wiederherstellungspunkt zuordnen, ist möglicherweise nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="2049b-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="2049b-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2049b-129">-WorkspaceName</span></span>
<span data-ttu-id="2049b-130">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2049b-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2049b-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2049b-131">-WorkspaceObject</span></span>
<span data-ttu-id="2049b-132">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2049b-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2049b-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2049b-133">-Confirm</span></span>
<span data-ttu-id="2049b-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2049b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2049b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2049b-135">-WhatIf</span></span>
<span data-ttu-id="2049b-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2049b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2049b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2049b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2049b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2049b-138">CommonParameters</span></span>
<span data-ttu-id="2049b-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2049b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2049b-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2049b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2049b-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2049b-141">INPUTS</span></span>

### <span data-ttu-id="2049b-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2049b-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2049b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2049b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="2049b-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2049b-144">OUTPUTS</span></span>

### <span data-ttu-id="2049b-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="2049b-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="2049b-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2049b-146">NOTES</span></span>

## <span data-ttu-id="2049b-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2049b-147">RELATED LINKS</span></span>
