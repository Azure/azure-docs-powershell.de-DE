---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: fd83b97a7b95760d0ee2ce88295ed14c98a43ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149921"
---
# <span data-ttu-id="6cbbf-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6cbbf-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="6cbbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbbf-103">Stellt einen Synapse Analytics SQL wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6cbbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cbbf-104">SYNTAX</span></span>

### <span data-ttu-id="6cbbf-105">RestoreFromBackupIdByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6cbbf-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cbbf-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbbf-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cbbf-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbbf-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cbbf-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbbf-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cbbf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cbbf-109">DESCRIPTION</span></span>
<span data-ttu-id="6cbbf-110">Das **Cmdlet "Restore-AzSynapseSqlPool"** stellt einen Azure Synapse Analytics SQL-Pool aus einer Sicherung oder einem Wiederherstellungspunkt eines beliebigen SQL wieder her.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="6cbbf-111">Der wiederhergestellte SQL pool wird als neuer SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="6cbbf-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6cbbf-112">EXAMPLES</span></span>

### <span data-ttu-id="6cbbf-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6cbbf-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="6cbbf-114">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt, indem aus der letzten Sicherung eines SQL in diesem Abonnement wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="6cbbf-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6cbbf-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="6cbbf-116">Dieser Befehl erstellt einen Azure Synapse Analytics SQL-Pool, indem ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement zum Wiederherstellen oder Kopieren aus einem vorherigen Zustand verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="6cbbf-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6cbbf-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="6cbbf-118">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt, indem aus der letzten Sicherung eines beliebigen SQL in diesem Abonnement mit Ressourcen-ID wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="6cbbf-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="6cbbf-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="6cbbf-120">Dieser Befehl erstellt einen Azure Synapse Analytics SQL-Pool, indem ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement zum Wiederherstellen oder Kopieren aus einem vorherigen Zustand mit Ressourcen-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="6cbbf-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cbbf-121">PARAMETERS</span></span>

### <span data-ttu-id="6cbbf-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cbbf-122">-AsJob</span></span>
<span data-ttu-id="6cbbf-123">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6cbbf-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cbbf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbbf-124">-DefaultProfile</span></span>
<span data-ttu-id="6cbbf-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cbbf-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="6cbbf-126">-FromBackup</span></span>
<span data-ttu-id="6cbbf-127">Gibt an, dass sie aus der letzten Sicherung eines SQL in diesem Abonnement wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbbf-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6cbbf-128">-FromRestorePoint</span></span>
<span data-ttu-id="6cbbf-129">Gibt an, dass ein Wiederherstellungspunkt aus einem SQL in diesem Abonnement zum Wiederherstellen oder Kopieren aus einem vorherigen Zustand genutzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbbf-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6cbbf-130">-Name</span></span>
<span data-ttu-id="6cbbf-131">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetSqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbbf-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="6cbbf-132">-PerformanceLevel</span></span>
<span data-ttu-id="6cbbf-133">Die SQL Dienstebene und Leistungsstufe, die dem SQL werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="6cbbf-134">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbbf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cbbf-135">-ResourceGroupName</span></span>
<span data-ttu-id="6cbbf-136">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbbf-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cbbf-137">-ResourceId</span></span>
<span data-ttu-id="6cbbf-138">Die Ressourcen-ID der wiederherzustellende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-138">The resource ID of the database to restore.</span></span>

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

### <span data-ttu-id="6cbbf-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="6cbbf-139">-RestorePoint</span></span>
<span data-ttu-id="6cbbf-140">Momentaufnahmezeit, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-140">Snapshot time to restore.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases: PointInTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbbf-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6cbbf-141">-WorkspaceName</span></span>
<span data-ttu-id="6cbbf-142">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbbf-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6cbbf-143">-WorkspaceObject</span></span>
<span data-ttu-id="6cbbf-144">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cbbf-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cbbf-145">-Confirm</span></span>
<span data-ttu-id="6cbbf-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cbbf-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6cbbf-147">-WhatIf</span></span>
<span data-ttu-id="6cbbf-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cbbf-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cbbf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbbf-150">CommonParameters</span></span>
<span data-ttu-id="6cbbf-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cbbf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbbf-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cbbf-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbbf-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6cbbf-153">INPUTS</span></span>

### <span data-ttu-id="6cbbf-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6cbbf-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6cbbf-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6cbbf-155">OUTPUTS</span></span>

### <span data-ttu-id="6cbbf-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6cbbf-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6cbbf-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6cbbf-157">NOTES</span></span>

## <span data-ttu-id="6cbbf-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6cbbf-158">RELATED LINKS</span></span>
