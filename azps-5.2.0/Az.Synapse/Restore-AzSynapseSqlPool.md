---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 7fbc6cedf039cca33d0a30b39a21f9cdcb350b61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294646"
---
# <span data-ttu-id="66b34-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="66b34-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="66b34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66b34-102">SYNOPSIS</span></span>
<span data-ttu-id="66b34-103">Stellt einen Synapse Analytics SQL wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="66b34-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="66b34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66b34-104">SYNTAX</span></span>

### <span data-ttu-id="66b34-105">RestoreFromBackupIdByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="66b34-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b34-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b34-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66b34-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b34-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66b34-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b34-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b34-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b34-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b34-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b34-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66b34-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b34-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b34-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b34-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b34-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b34-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66b34-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b34-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66b34-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66b34-115">DESCRIPTION</span></span>
<span data-ttu-id="66b34-116">Das **Cmdlet "Restore-AzSynapseSqlPool"** stellt einen Azure Synapse Analytics SQL-Pool aus einer Sicherung oder einem Wiederherstellungspunkt eines beliebigen SQL wieder her.</span><span class="sxs-lookup"><span data-stu-id="66b34-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="66b34-117">Der wiederhergestellte SQL pool wird als neuer SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="66b34-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="66b34-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66b34-118">EXAMPLES</span></span>

### <span data-ttu-id="66b34-119">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66b34-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="66b34-120">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt, indem aus der letzten Sicherung eines SQL in diesem Abonnement wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="66b34-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="66b34-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="66b34-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="66b34-122">Dieser Befehl erstellt einen Azure Synapse Analytics SQL-Pool, indem ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement zum Wiederherstellen oder Kopieren aus einem vorherigen Zustand verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66b34-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="66b34-123">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="66b34-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="66b34-124">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt, indem aus der letzten Sicherung eines beliebigen SQL in diesem Abonnement mit Ressourcen-ID wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="66b34-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="66b34-125">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="66b34-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="66b34-126">Dieser Befehl erstellt einen Azure Synapse Analytics SQL-Pool, indem ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement zum Wiederherstellen oder Kopieren aus einem vorherigen Zustand mit Ressourcen-ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66b34-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="66b34-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66b34-127">PARAMETERS</span></span>

### <span data-ttu-id="66b34-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66b34-128">-AsJob</span></span>
<span data-ttu-id="66b34-129">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="66b34-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66b34-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b34-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="66b34-131">Der Ressourcengruppenname des Bakcups SQL Poolobjekt, aus dem sie erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="66b34-132">-BackupResourceId</span></span>
<span data-ttu-id="66b34-133">Der Ressourcenbezeichner der SQL Poolobjekts, aus dem sie wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="66b34-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="66b34-135">Der Name des Bakcups SQL Poolobjekt, aus dem sie erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="66b34-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="66b34-137">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="66b34-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66b34-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="66b34-139">Der Name des Synapse-Arbeitsbereichs, aus SQL pool-Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b34-140">-DefaultProfile</span></span>
<span data-ttu-id="66b34-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66b34-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66b34-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="66b34-142">-FromBackup</span></span>
<span data-ttu-id="66b34-143">Gibt an, dass sie aus der letzten Sicherung eines SQL in diesem Abonnement wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="66b34-144">-FromRestorePoint</span></span>
<span data-ttu-id="66b34-145">Gibt an, dass ein Wiederherstellungspunkt aus einem SQL in diesem Abonnement zum Wiederherstellen oder Kopieren aus einem vorherigen Zustand genutzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-146">-Name</span><span class="sxs-lookup"><span data-stu-id="66b34-146">-Name</span></span>
<span data-ttu-id="66b34-147">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="66b34-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="66b34-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="66b34-148">-PerformanceLevel</span></span>
<span data-ttu-id="66b34-149">Die SQL Dienststufe und Leistungsstufe, die dem SQL werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="66b34-150">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="66b34-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b34-151">-ResourceGroupName</span></span>
<span data-ttu-id="66b34-152">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="66b34-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="66b34-153">-RestorePoint</span></span>
<span data-ttu-id="66b34-154">Momentaufnahmezeit, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b34-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="66b34-156">Der Ressourcengruppenname des SQL Poolobjekts, aus dem sie erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="66b34-157">-SourceResourceId</span></span>
<span data-ttu-id="66b34-158">Der Ressourcenbezeichner des SQL Poolobjekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="66b34-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="66b34-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="66b34-160">Der Name des Quellobjekts SQL Poolobjekts, aus dem sie erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="66b34-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="66b34-162">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="66b34-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66b34-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="66b34-164">Der Name des Synapse-Arbeitsbereichs der SQL Poolobjekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b34-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="66b34-165">-Tag</span></span>
<span data-ttu-id="66b34-166">Ein Zeichenfolgenverzeichnis mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="66b34-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="66b34-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66b34-167">-WorkspaceName</span></span>
<span data-ttu-id="66b34-168">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="66b34-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="66b34-169">-WorkspaceObject</span></span>
<span data-ttu-id="66b34-170">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="66b34-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66b34-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66b34-171">-Confirm</span></span>
<span data-ttu-id="66b34-172">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66b34-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b34-173">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="66b34-173">-WhatIf</span></span>
<span data-ttu-id="66b34-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66b34-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b34-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66b34-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b34-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b34-176">CommonParameters</span></span>
<span data-ttu-id="66b34-177">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b34-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b34-178">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66b34-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b34-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66b34-179">INPUTS</span></span>

### <span data-ttu-id="66b34-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="66b34-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="66b34-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66b34-181">OUTPUTS</span></span>

### <span data-ttu-id="66b34-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="66b34-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="66b34-183">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="66b34-183">NOTES</span></span>

## <span data-ttu-id="66b34-184">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="66b34-184">RELATED LINKS</span></span>
