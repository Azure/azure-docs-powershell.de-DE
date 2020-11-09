---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 2dae942470dba8a36258ffb8c813e08c664f2e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301702"
---
# <span data-ttu-id="00414-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="00414-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="00414-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00414-102">SYNOPSIS</span></span>
<span data-ttu-id="00414-103">Wiederherstellung eines Synapse Analytics SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="00414-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="00414-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00414-104">SYNTAX</span></span>

### <span data-ttu-id="00414-105">RestoreFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-105">RestoreFromBackupIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00414-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00414-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00414-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00414-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00414-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00414-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00414-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00414-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00414-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00414-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00414-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00414-115">DESCRIPTION</span></span>
<span data-ttu-id="00414-116">Das Cmdlet **Restore-AzSynapseSqlPool** stellt einen Azure Synapse Analytics-SQL-Pool aus einer Sicherung oder einem Wiederherstellungspunkt eines beliebigen SQL-Pools wieder her.</span><span class="sxs-lookup"><span data-stu-id="00414-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="00414-117">Der wiederhergestellte SQL-Pool wird als neuer SQL-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="00414-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="00414-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00414-118">EXAMPLES</span></span>

### <span data-ttu-id="00414-119">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00414-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="00414-120">Mit diesem Befehl wird ein Azure Synapse-Analyse-SQL-Pool erstellt, indem aus der letzten Sicherung eines beliebigen SQL-Pools in diesem Abonnement wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="00414-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="00414-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="00414-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="00414-122">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt, indem ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement zur Wiederherstellung oder zum Kopieren aus einem vorherigen Zustand genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="00414-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="00414-123">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="00414-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="00414-124">Mit diesem Befehl wird ein Azure Synapse Analytics SQL-Pool erstellt, indem aus der letzten Sicherung eines beliebigen SQL-Pools in diesem Abonnement mit Ressourcen-ID wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="00414-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="00414-125">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="00414-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="00414-126">Mit diesem Befehl wird ein Azure Synapse-Analyse-SQL-Pool erstellt, indem ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement zur Wiederherstellung oder zum Kopieren aus einem vorherigen Zustand mit Ressourcen-ID genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="00414-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="00414-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="00414-127">PARAMETERS</span></span>

### <span data-ttu-id="00414-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00414-128">-AsJob</span></span>
<span data-ttu-id="00414-129">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="00414-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00414-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00414-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="00414-131">Der Ressourcengruppenname des bakcup SQL-Pool Objekts, aus dem Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="00414-131">The resource group name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="00414-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="00414-132">-BackupResourceId</span></span>
<span data-ttu-id="00414-133">Der Ressourcenbezeichner des Sicherungs-SQL-Pool Objekts, von dem wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00414-133">The resource identifier of backup SQL pool object to restore from.</span></span>

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

### <span data-ttu-id="00414-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="00414-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="00414-135">Der Name des bakcup SQL-Pool Objekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00414-135">The name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="00414-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="00414-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="00414-137">SQL-Pool Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="00414-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="00414-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="00414-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="00414-139">Der Synapse-Arbeitsbereichsname des bakcup SQL-Pool Objekts, aus dem Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="00414-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="00414-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00414-140">-DefaultProfile</span></span>
<span data-ttu-id="00414-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00414-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00414-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="00414-142">-FromBackup</span></span>
<span data-ttu-id="00414-143">Gibt an, dass die Wiederherstellung aus der letzten Sicherung eines beliebigen SQL-Pools in diesem Abonnement abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="00414-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

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

### <span data-ttu-id="00414-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="00414-144">-FromRestorePoint</span></span>
<span data-ttu-id="00414-145">Gibt an, dass ein Wiederherstellungspunkt aus einem beliebigen SQL-Pool in diesem Abonnement für die Wiederherstellung oder das Kopieren aus einem vorherigen Zustand genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="00414-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

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

### <span data-ttu-id="00414-146">-Name</span><span class="sxs-lookup"><span data-stu-id="00414-146">-Name</span></span>
<span data-ttu-id="00414-147">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="00414-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="00414-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="00414-148">-PerformanceLevel</span></span>
<span data-ttu-id="00414-149">Die SQL-Dienstebene und die Leistungsstufe, die dem SQL-Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00414-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="00414-150">Beispiel: DW2000c.</span><span class="sxs-lookup"><span data-stu-id="00414-150">For example, DW2000c.</span></span>

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

### <span data-ttu-id="00414-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00414-151">-ResourceGroupName</span></span>
<span data-ttu-id="00414-152">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="00414-152">Resource group name.</span></span>

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

### <span data-ttu-id="00414-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="00414-153">-RestorePoint</span></span>
<span data-ttu-id="00414-154">Wiederherstellungszeit für Snapshots.</span><span class="sxs-lookup"><span data-stu-id="00414-154">Snapshot time to restore.</span></span>

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

### <span data-ttu-id="00414-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00414-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="00414-156">Der Ressourcengruppenname des Quell-SQL-Pool Objekts, aus dem Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="00414-156">The resource group name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="00414-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="00414-157">-SourceResourceId</span></span>
<span data-ttu-id="00414-158">Der Ressourcenbezeichner des Quell-SQL-Pool Objekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00414-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="00414-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="00414-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="00414-160">Der Name des Quell-SQL-Pool Objekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00414-160">The name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="00414-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="00414-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="00414-162">SQL-Pool Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="00414-162">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="00414-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="00414-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="00414-164">Der Synapse-Arbeitsbereichsname des Quell-SQL-Pool Objekts, aus dem erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00414-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="00414-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="00414-165">-Tag</span></span>
<span data-ttu-id="00414-166">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="00414-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="00414-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="00414-167">-WorkspaceName</span></span>
<span data-ttu-id="00414-168">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="00414-168">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="00414-169">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="00414-169">-WorkspaceObject</span></span>
<span data-ttu-id="00414-170">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="00414-170">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="00414-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00414-171">-Confirm</span></span>
<span data-ttu-id="00414-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00414-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00414-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00414-173">-WhatIf</span></span>
<span data-ttu-id="00414-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00414-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00414-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00414-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00414-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00414-176">CommonParameters</span></span>
<span data-ttu-id="00414-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00414-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00414-178">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00414-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00414-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00414-179">INPUTS</span></span>

### <span data-ttu-id="00414-180">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="00414-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="00414-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00414-181">OUTPUTS</span></span>

### <span data-ttu-id="00414-182">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="00414-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="00414-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="00414-183">NOTES</span></span>

## <span data-ttu-id="00414-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00414-184">RELATED LINKS</span></span>
