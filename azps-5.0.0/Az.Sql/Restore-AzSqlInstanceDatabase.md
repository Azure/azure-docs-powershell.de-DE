---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: 4d8ece03cc5c1a96d73bcde79aef76c8f329b38a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177174"
---
# <span data-ttu-id="e2a63-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e2a63-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="e2a63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2a63-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a63-103">Stellt eine Azure SQL-Datenbank für verwaltete Instanzen wieder her.</span><span class="sxs-lookup"><span data-stu-id="e2a63-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="e2a63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2a63-104">SYNTAX</span></span>

### <span data-ttu-id="e2a63-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="e2a63-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a63-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e2a63-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a63-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e2a63-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a63-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="e2a63-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a63-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e2a63-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a63-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e2a63-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a63-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="e2a63-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a63-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="e2a63-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a63-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e2a63-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a63-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e2a63-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a63-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e2a63-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-Name] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a63-116">LongTermRetentionBackupRestoreParameter</span><span class="sxs-lookup"><span data-stu-id="e2a63-116">LongTermRetentionBackupRestoreParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromLongTermRetentionBackup] [-SubscriptionId <String>] [-ResourceId] <String>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2a63-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2a63-117">DESCRIPTION</span></span>
<span data-ttu-id="e2a63-118">Das Cmdlet **Restore-AzSqlInstanceDatabase** stellt eine Instanzen Datenbank aus einer Geo-redundanten Sicherung, einem Zeitpunkt in einer Livedatenbank oder einer langfristigen Aufbewahrungs Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="e2a63-118">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup, a point in time in a live database, or a long term retention backup.</span></span>
<span data-ttu-id="e2a63-119">Die wiederhergestellte Datenbank wird als neue Instanzen Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="e2a63-119">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="e2a63-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2a63-120">EXAMPLES</span></span>

### <span data-ttu-id="e2a63-121">Beispiel 1: Wiederherstellen einer Instanzen Datenbank aus einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="e2a63-121">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="e2a63-122">Der Befehl stellt die Instanzdatenbank database01 aus der angegebenen Point-in-Time-Sicherung in der Instanzdatenbank mit dem Namen Database01_restored wieder her.</span><span class="sxs-lookup"><span data-stu-id="e2a63-122">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="e2a63-123">Beispiel 2: Wiederherstellen einer Instanzen Datenbank von einem Zeitpunkt zu einer anderen Instanz in einer anderen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e2a63-123">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="e2a63-124">Der Befehl stellt die Instanzdatenbank Database01 auf Instanz-managedInstance1 auf der Ressourcengruppen-ResourceGroup01 von der angegebenen Point-in-Time-Sicherung in der Instanzdatenbank mit dem Namen Database01_restored auf Instanz managedInstance2 auf der Ressourcengruppen-ResourceGroup02 wieder her.</span><span class="sxs-lookup"><span data-stu-id="e2a63-124">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="e2a63-125">Beispiel 3: Geo-Restore einer Instanzen Datenbank</span><span class="sxs-lookup"><span data-stu-id="e2a63-125">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="e2a63-126">Der erste Befehl ruft die Geo-redundante Sicherung für die Datenbank mit dem Namen database01 ab und speichert Sie dann in der $GeoBackup-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e2a63-126">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="e2a63-127">Der zweite Befehl stellt die Sicherung in $GeoBackup in der Instanzdatenbank mit dem Namen Database01_restored wieder her.</span><span class="sxs-lookup"><span data-stu-id="e2a63-127">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="e2a63-128">Beispiel 4: Wiederherstellen einer gelöschten Instanzen Datenbank aus einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="e2a63-128">Example 4: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -Name $deletedDatabase.Name -InstanceName $deletedDatabase.ManagedInstanceName -ResourceGroupName $deletedDatabase.ResourceGroupName -DeletionDate $deletedDatabase.DeletionDate -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="e2a63-129">Der erste Befehl ruft die gelöschten Instanz-Datenbanken mit dem Namen "degressiv" auf der Instanz "managedInstance1" ab.</span><span class="sxs-lookup"><span data-stu-id="e2a63-129">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="e2a63-130">Der zweite Befehl stellt die abgerufene Datenbank aus der angegebenen Point-in-Time-Sicherung in der Instanzdatenbank mit dem Namen Database01_restored wieder her.</span><span class="sxs-lookup"><span data-stu-id="e2a63-130">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="e2a63-131">Beispiel 5: Wiederherstellen einer gelöschten Instanzen Datenbank aus einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="e2a63-131">Example 5: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -InputObject $deletedDatabase[0] -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="e2a63-132">Der erste Befehl ruft die gelöschten Instanz-Datenbanken mit dem Namen "degressiv" auf der Instanz "managedInstance1" ab.</span><span class="sxs-lookup"><span data-stu-id="e2a63-132">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="e2a63-133">Der zweite Befehl stellt die abgerufene Datenbank aus der angegebenen Point-in-Time-Sicherung in der Instanzdatenbank mit dem Namen Database01_restored mithilfe des Eingabeobjekts wieder her.</span><span class="sxs-lookup"><span data-stu-id="e2a63-133">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored using input object.</span></span>

### <span data-ttu-id="e2a63-134">Beispiel 6: Wiederherstellen einer Datenbank aus der Ltr-Sicherung</span><span class="sxs-lookup"><span data-stu-id="e2a63-134">Example 6: Restore a database from LTR backup.</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -FromLongTermRetentionBackup -ResourceId /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManagedInstances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000 -TargetInstanceDatabaseName restoreTarget -TargetInstanceName testInstance -TargetResourceGroupName testResourceGroup


Location                          : southeastasia
Tags                              :
Collation                         : SQL_Latin1_General_CP1_CI_AS
Status                            : Online
RestorePointInTime                :
DefaultSecondaryLocation          : northeurope
CatalogCollation                  :
CreateMode                        :
StorageContainerUri               :
StorageContainerSasToken          :
SourceDatabaseId                  :
FailoverGroupId                   :
RecoverableDatabaseId             :
RestorableDroppedDatabaseId       :
LongTermRetentionBackupResourceId :
ResourceGroupName                 : testResourceGroup
ManagedInstanceName               : testInstance
Name                              : restoreTarget
CreationDate                      : 3/4/2020 8:12:56 AM
EarliestRestorePoint              : 3/4/2020 8:14:29 AM
Id                                : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/managedInstances/testInstance/databases/restoreTarget
```

<span data-ttu-id="e2a63-135">Stellt die Ltr-Sicherung mit der angegebenen Ressourcen-ID wieder her (die durch Ausführen von Get-AzSqlInstanceDatabaseLongTermRetentionBackup gefunden werden kann).</span><span class="sxs-lookup"><span data-stu-id="e2a63-135">Restores LTR backup with the given resource ID (which can be found by running Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span></span>

## <span data-ttu-id="e2a63-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2a63-136">PARAMETERS</span></span>

### <span data-ttu-id="e2a63-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2a63-137">-AsJob</span></span>
<span data-ttu-id="e2a63-138">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e2a63-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2a63-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a63-139">-DefaultProfile</span></span>
<span data-ttu-id="e2a63-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e2a63-140">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="e2a63-141">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="e2a63-141">-DeletionDate</span></span>
<span data-ttu-id="e2a63-142">Das Löschdatum der gelöschten Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e2a63-142">The deletion date of deleted database.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-143">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="e2a63-143">-FromGeoBackup</span></span>
<span data-ttu-id="e2a63-144">Wiederherstellen aus einer Geo-Sicherung</span><span class="sxs-lookup"><span data-stu-id="e2a63-144">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-145">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e2a63-145">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="e2a63-146">Wiederherstellen aus einer langfristigen Aufbewahrungs Sicherung</span><span class="sxs-lookup"><span data-stu-id="e2a63-146">Restore from a Long Term Retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-147">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="e2a63-147">-FromPointInTimeBackup</span></span>
<span data-ttu-id="e2a63-148">Wiederherstellen aus einer Point-in-Time-Sicherung</span><span class="sxs-lookup"><span data-stu-id="e2a63-148">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-149">-Geobackupobject</span><span class="sxs-lookup"><span data-stu-id="e2a63-149">-GeoBackupObject</span></span>
<span data-ttu-id="e2a63-150">Das wiederherzustellende wiederherstellbare Instanz-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="e2a63-150">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-151">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e2a63-151">-InputObject</span></span>
<span data-ttu-id="e2a63-152">Das wiederherzustellende Instanzendaten Bank Objekt</span><span class="sxs-lookup"><span data-stu-id="e2a63-152">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-153">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e2a63-153">-InstanceName</span></span>
<span data-ttu-id="e2a63-154">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="e2a63-154">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-155">-Name</span><span class="sxs-lookup"><span data-stu-id="e2a63-155">-Name</span></span>
<span data-ttu-id="e2a63-156">Der Name der Instanzdatenbank, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2a63-156">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName, SourceInstanceDatabaseName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-157">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="e2a63-157">-PointInTime</span></span>
<span data-ttu-id="e2a63-158">Der Zeitpunkt, zu dem die Datenbank wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2a63-158">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a63-159">-ResourceGroupName</span></span>
<span data-ttu-id="e2a63-160">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e2a63-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-161">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e2a63-161">-ResourceId</span></span>
<span data-ttu-id="e2a63-162">Die Ressourcen-ID des wiederherzustellenden Instanz-Datenbankobjekts</span><span class="sxs-lookup"><span data-stu-id="e2a63-162">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-163">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e2a63-163">-SubscriptionId</span></span>
<span data-ttu-id="e2a63-164">Quell Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e2a63-164">Source subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, LongTermRetentionBackupRestoreParameter
Aliases: SourceSubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-165">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2a63-165">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="e2a63-166">Der Name der Ziel Instanzdatenbank, in die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2a63-166">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="e2a63-167">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="e2a63-167">-TargetInstanceName</span></span>
<span data-ttu-id="e2a63-168">Der Name der Zielinstanz, in die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2a63-168">The name of the target instance to restore to.</span></span>
<span data-ttu-id="e2a63-169">Wenn Sie nicht angegeben wird, entspricht die Zielinstanz der Quellinstanz.</span><span class="sxs-lookup"><span data-stu-id="e2a63-169">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-170">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a63-170">-TargetResourceGroupName</span></span>
<span data-ttu-id="e2a63-171">Der Name der Ziel Ressourcengruppe, in der wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2a63-171">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="e2a63-172">Wenn keine Ziel Ressourcengruppe angegeben ist, entspricht Sie der Quellressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e2a63-172">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a63-173">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e2a63-173">-Confirm</span></span>
<span data-ttu-id="e2a63-174">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2a63-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2a63-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a63-175">-WhatIf</span></span>
<span data-ttu-id="e2a63-176">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2a63-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2a63-177">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2a63-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2a63-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a63-178">CommonParameters</span></span>
<span data-ttu-id="e2a63-179">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a63-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a63-180">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2a63-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a63-181">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2a63-181">INPUTS</span></span>

### <span data-ttu-id="e2a63-182">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e2a63-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="e2a63-183">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e2a63-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="e2a63-184">System. String</span><span class="sxs-lookup"><span data-stu-id="e2a63-184">System.String</span></span>

## <span data-ttu-id="e2a63-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2a63-185">OUTPUTS</span></span>

### <span data-ttu-id="e2a63-186">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e2a63-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e2a63-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2a63-187">NOTES</span></span>

## <span data-ttu-id="e2a63-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2a63-188">RELATED LINKS</span></span>
