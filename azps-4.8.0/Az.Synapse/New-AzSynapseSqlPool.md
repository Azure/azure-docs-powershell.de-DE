---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174880"
---
# <span data-ttu-id="84062-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="84062-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="84062-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84062-102">SYNOPSIS</span></span>
<span data-ttu-id="84062-103">Erstellt einen Synapse Analytics SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="84062-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="84062-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84062-104">SYNTAX</span></span>

### <span data-ttu-id="84062-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="84062-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84062-106">CreateFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84062-107">CreateFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84062-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84062-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84062-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84062-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84062-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84062-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84062-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84062-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84062-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84062-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84062-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84062-117">DESCRIPTION</span></span>
<span data-ttu-id="84062-118">Mit dem Cmdlet **New-AzSynapseSqlPool** wird ein Azure Synapse Analytics SQL-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="84062-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="84062-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84062-119">EXAMPLES</span></span>

### <span data-ttu-id="84062-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84062-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="84062-121">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="84062-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="84062-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="84062-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="84062-123">Mit diesem Befehl wird ein Azure Synapse-Analyse-SQL-Pool erstellt, indem aus der letzten Sicherung eines beliebigen SQL-Pools in diesem Abonnement wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="84062-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="84062-124">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="84062-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="84062-125">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt, indem ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement zur Wiederherstellung oder zum Kopieren aus einem vorherigen Zustand genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="84062-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="84062-126">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="84062-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="84062-127">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt, indem aus der letzten Sicherung eines beliebigen SQL-Pools in diesem Abonnement mit Ressourcen-ID wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="84062-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="84062-128">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="84062-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="84062-129">Mit diesem Befehl wird ein Azure Synapse-Analyse-SQL-Pool erstellt, indem ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement zur Wiederherstellung oder zum Kopieren aus einem vorherigen Zustand mit Ressourcen-ID genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="84062-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="84062-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="84062-130">PARAMETERS</span></span>

### <span data-ttu-id="84062-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84062-131">-AsJob</span></span>
<span data-ttu-id="84062-132">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="84062-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84062-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84062-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="84062-134">Der Ressourcengruppenname des bakcup SQL-Pool Objekts, aus dem Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="84062-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-135">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="84062-135">-BackupResourceId</span></span>
<span data-ttu-id="84062-136">Der Ressourcenbezeichner des Sicherungs-SQL-Pool Objekts, von dem wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="84062-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="84062-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="84062-138">Der Name des bakcup SQL-Pool Objekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="84062-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-139">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="84062-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="84062-140">SQL-Pool Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="84062-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-141">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="84062-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="84062-142">Der Synapse-Arbeitsbereichsname des bakcup SQL-Pool Objekts, aus dem Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="84062-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-143">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="84062-143">-Collation</span></span>
<span data-ttu-id="84062-144">Sortierung definiert die Regeln, die Daten sortieren und vergleichen, und kann nach der SQL Pool-Erstellung nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="84062-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="84062-145">Die Standardsortierung ist SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="84062-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84062-146">-DefaultProfile</span></span>
<span data-ttu-id="84062-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84062-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84062-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="84062-148">-FromBackup</span></span>
<span data-ttu-id="84062-149">Gibt an, dass die Wiederherstellung aus der letzten Sicherung eines beliebigen SQL-Pools in diesem Abonnement abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="84062-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="84062-150">-FromRestorePoint</span></span>
<span data-ttu-id="84062-151">Gibt an, dass ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement für die Wiederherstellung oder das Kopieren aus einem vorherigen Zustand genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="84062-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-152">-Name</span><span class="sxs-lookup"><span data-stu-id="84062-152">-Name</span></span>
<span data-ttu-id="84062-153">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="84062-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="84062-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="84062-154">-PerformanceLevel</span></span>
<span data-ttu-id="84062-155">Die SQL-Dienstebene und die Leistungsstufe, die dem SQL-Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="84062-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="84062-156">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="84062-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84062-157">-ResourceGroupName</span></span>
<span data-ttu-id="84062-158">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84062-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="84062-159">-RestorePoint</span></span>
<span data-ttu-id="84062-160">Wiederherstellungszeit für Snapshots.</span><span class="sxs-lookup"><span data-stu-id="84062-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84062-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="84062-162">Der Ressourcengruppenname des Quell-SQL-Pool Objekts, aus dem Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="84062-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-163">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="84062-163">-SourceResourceId</span></span>
<span data-ttu-id="84062-164">Der Ressourcenbezeichner des Quell-SQL-Pool Objekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="84062-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-165">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="84062-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="84062-166">Der Name des Quell-SQL-Pool Objekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="84062-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-167">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="84062-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="84062-168">SQL-Pool Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="84062-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-169">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="84062-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="84062-170">Der Synapse-Arbeitsbereichsname des Quell-SQL-Pool Objekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="84062-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="84062-171">-Tag</span></span>
<span data-ttu-id="84062-172">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="84062-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="84062-173">-Version</span><span class="sxs-lookup"><span data-stu-id="84062-173">-Version</span></span>
<span data-ttu-id="84062-174">Version des Synapse SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="84062-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="84062-175">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="84062-175">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="84062-176">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="84062-176">-WorkspaceName</span></span>
<span data-ttu-id="84062-177">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="84062-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84062-178">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="84062-178">-WorkspaceObject</span></span>
<span data-ttu-id="84062-179">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="84062-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84062-180">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84062-180">-Confirm</span></span>
<span data-ttu-id="84062-181">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84062-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84062-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84062-182">-WhatIf</span></span>
<span data-ttu-id="84062-183">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84062-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84062-184">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84062-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84062-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84062-185">CommonParameters</span></span>
<span data-ttu-id="84062-186">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84062-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84062-187">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84062-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84062-188">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84062-188">INPUTS</span></span>

### <span data-ttu-id="84062-189">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="84062-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="84062-190">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84062-190">OUTPUTS</span></span>

### <span data-ttu-id="84062-191">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="84062-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="84062-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="84062-192">NOTES</span></span>

## <span data-ttu-id="84062-193">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84062-193">RELATED LINKS</span></span>
