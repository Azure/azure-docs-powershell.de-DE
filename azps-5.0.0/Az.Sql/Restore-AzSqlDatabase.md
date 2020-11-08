---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176024"
---
# <span data-ttu-id="a87c1-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a87c1-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="a87c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a87c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a87c1-103">Stellt eine SQL-Datenbank wieder her.</span><span class="sxs-lookup"><span data-stu-id="a87c1-103">Restores a SQL database.</span></span>

## <span data-ttu-id="a87c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a87c1-104">SYNTAX</span></span>

### <span data-ttu-id="a87c1-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a87c1-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="a87c1-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a87c1-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a87c1-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="a87c1-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a87c1-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a87c1-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="a87c1-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a87c1-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a87c1-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="a87c1-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a87c1-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a87c1-113">DESCRIPTION</span></span>
<span data-ttu-id="a87c1-114">Das Cmdlet **Restore-AzSqlDatabase** stellt eine SQL-Datenbank aus einer Geo-redundanten Sicherung, einer Sicherung einer gelöschten Datenbank, einer langfristigen Aufbewahrungs Sicherung oder einem Zeitpunkt in einer Livedatenbank wieder her.</span><span class="sxs-lookup"><span data-stu-id="a87c1-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="a87c1-115">Die wiederhergestellte Datenbank wird als neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="a87c1-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="a87c1-116">Sie können eine elastische SQL-Datenbank erstellen, indem Sie den *ElasticPoolName* -Parameter auf einen vorhandenen elastischen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="a87c1-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="a87c1-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a87c1-117">EXAMPLES</span></span>

### <span data-ttu-id="a87c1-118">Beispiel 1: Wiederherstellen einer Datenbank ab einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="a87c1-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="a87c1-119">Der erste Befehl ruft die SQL-Datenbank mit dem Namen database01 ab und speichert Sie dann in der $Database-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a87c1-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="a87c1-120">Der zweite Befehl stellt die Datenbank in $Database aus der angegebenen Point-in-Time-Sicherung in der Datenbank mit dem Namen RestoredDatabase wieder her.</span><span class="sxs-lookup"><span data-stu-id="a87c1-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="a87c1-121">Beispiel 2: Wiederherstellen einer Datenbank von einem bestimmten Zeitpunkt zu einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="a87c1-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="a87c1-122">Der erste Befehl ruft die SQL-Datenbank mit dem Namen database01 ab und speichert Sie dann in der $Database-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a87c1-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="a87c1-123">Der zweite Befehl stellt die Datenbank in $Database aus der angegebenen Point-in-Time-Sicherung in der SQL-Datenbank namens RestoredDatabase im elastischen Pool mit dem Namen elasticpool01 wieder her.</span><span class="sxs-lookup"><span data-stu-id="a87c1-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="a87c1-124">Beispiel 3: Wiederherstellen einer gelöschten Datenbank</span><span class="sxs-lookup"><span data-stu-id="a87c1-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="a87c1-125">Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="a87c1-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="a87c1-126">Mit dem zweiten Befehl wird die Wiederherstellung aus der gelöschten Datenbanksicherung mit dem Cmdlet [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) gestartet.</span><span class="sxs-lookup"><span data-stu-id="a87c1-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="a87c1-127">Wenn der Parameter-PointInTime nicht angegeben wird, wird die Datenbank in der Lösch Zeit wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="a87c1-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="a87c1-128">Beispiel 4: Wiederherstellen einer gelöschten Datenbank in einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="a87c1-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="a87c1-129">Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="a87c1-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="a87c1-130">Mit dem zweiten Befehl wird die Wiederherstellung aus der gelöschten Datenbanksicherung mithilfe von [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)gestartet.</span><span class="sxs-lookup"><span data-stu-id="a87c1-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="a87c1-131">Wenn der Parameter-PointInTime nicht angegeben wird, wird die Datenbank in der Lösch Zeit wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="a87c1-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="a87c1-132">Beispiel 5: Geo-Restore einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="a87c1-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="a87c1-133">Der erste Befehl ruft die Geo-redundante Sicherung für die Datenbank mit dem Namen database01 ab und speichert Sie dann in der $GeoBackup-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a87c1-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="a87c1-134">Der zweite Befehl stellt die Sicherung in $GeoBackup in der SQL-Datenbank mit dem Namen RestoredDatabase wieder her.</span><span class="sxs-lookup"><span data-stu-id="a87c1-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="a87c1-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="a87c1-135">PARAMETERS</span></span>

### <span data-ttu-id="a87c1-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a87c1-136">-AsJob</span></span>
<span data-ttu-id="a87c1-137">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a87c1-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a87c1-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="a87c1-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="a87c1-139">Die Backup-Speicherredundanz, die zum Speichern von Sicherungen für die SQL-Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a87c1-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="a87c1-140">Die Optionen sind: local, Zone und Geo.</span><span class="sxs-lookup"><span data-stu-id="a87c1-140">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a87c1-141">-ComputeGeneration</span></span>
<span data-ttu-id="a87c1-142">Die COMPUTE-Generierung, die der wiederhergestellten Datenbank zugewiesen werden soll</span><span class="sxs-lookup"><span data-stu-id="a87c1-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a87c1-143">-DefaultProfile</span></span>
<span data-ttu-id="a87c1-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a87c1-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a87c1-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="a87c1-145">-DeletionDate</span></span>
<span data-ttu-id="a87c1-146">Gibt das Löschdatum als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a87c1-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="a87c1-147">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a87c1-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="a87c1-148">-Edition</span></span>
<span data-ttu-id="a87c1-149">Gibt die Edition der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="a87c1-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="a87c1-150">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a87c1-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a87c1-151">Keine</span><span class="sxs-lookup"><span data-stu-id="a87c1-151">None</span></span>
- <span data-ttu-id="a87c1-152">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="a87c1-152">Basic</span></span>
- <span data-ttu-id="a87c1-153">Standard</span><span class="sxs-lookup"><span data-stu-id="a87c1-153">Standard</span></span>
- <span data-ttu-id="a87c1-154">Premium</span><span class="sxs-lookup"><span data-stu-id="a87c1-154">Premium</span></span>
- <span data-ttu-id="a87c1-155">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="a87c1-155">DataWarehouse</span></span>
- <span data-ttu-id="a87c1-156">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="a87c1-156">Free</span></span>
- <span data-ttu-id="a87c1-157">Stretch</span><span class="sxs-lookup"><span data-stu-id="a87c1-157">Stretch</span></span>
- <span data-ttu-id="a87c1-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="a87c1-158">GeneralPurpose</span></span>
- <span data-ttu-id="a87c1-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="a87c1-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a87c1-160">-ElasticPoolName</span></span>
<span data-ttu-id="a87c1-161">Gibt den Namen des elastischen Pools an, in dem die SQL-Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a87c1-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="a87c1-163">Gibt an, dass dieses Cmdlet eine Datenbank aus einer Sicherung einer gelöschten SQL-Datenbank wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="a87c1-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="a87c1-164">Sie können das Get-AzSqlDeletedDatabaseBackup-Cmdlet verwenden, um die Sicherung einer gelöschten SQL-Datenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a87c1-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-165">-FromGeoBackup</span></span>
<span data-ttu-id="a87c1-166">Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer Geo-redundanten Sicherung wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="a87c1-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="a87c1-167">Sie können das Get-AzSqlDatabaseGeoBackup-Cmdlet verwenden, um eine Geo-redundante Sicherung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a87c1-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="a87c1-169">Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer langfristigen Aufbewahrungs Sicherung wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="a87c1-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="a87c1-171">Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer Point-in-Time-Sicherung wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="a87c1-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a87c1-172">-LicenseType</span></span>
<span data-ttu-id="a87c1-173">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a87c1-173">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="a87c1-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="a87c1-174">-PointInTime</span></span>
<span data-ttu-id="a87c1-175">Gibt den Zeitpunkt als **DateTime** -Objekt an, in dem Sie Ihre SQL-Datenbank wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="a87c1-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="a87c1-176">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a87c1-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="a87c1-177">Verwenden Sie diesen Parameter zusammen mit dem *FromPointInTimeBackup* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="a87c1-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a87c1-178">-ResourceGroupName</span></span>
<span data-ttu-id="a87c1-179">Gibt den Namen der Ressourcengruppe an, der das Cmdlet die SQL-Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="a87c1-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-180">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a87c1-180">-ResourceId</span></span>
<span data-ttu-id="a87c1-181">Gibt die ID der wiederherzustellenden Ressource an.</span><span class="sxs-lookup"><span data-stu-id="a87c1-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-182">-Servername</span><span class="sxs-lookup"><span data-stu-id="a87c1-182">-ServerName</span></span>
<span data-ttu-id="a87c1-183">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="a87c1-183">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a87c1-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="a87c1-185">Gibt den Namen des Dienst Ziels an.</span><span class="sxs-lookup"><span data-stu-id="a87c1-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-186">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="a87c1-186">-TargetDatabaseName</span></span>
<span data-ttu-id="a87c1-187">Gibt den Namen der Datenbank an, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a87c1-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="a87c1-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="a87c1-188">-VCore</span></span>
<span data-ttu-id="a87c1-189">Die Vcore-Nummern der wiederhergestellten Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a87c1-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87c1-190">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a87c1-190">-Confirm</span></span>
<span data-ttu-id="a87c1-191">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a87c1-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a87c1-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a87c1-192">-WhatIf</span></span>
<span data-ttu-id="a87c1-193">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a87c1-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a87c1-194">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a87c1-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a87c1-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87c1-195">CommonParameters</span></span>
<span data-ttu-id="a87c1-196">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a87c1-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87c1-197">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a87c1-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87c1-198">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a87c1-198">INPUTS</span></span>

### <span data-ttu-id="a87c1-199">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="a87c1-199">System.DateTime</span></span>

### <span data-ttu-id="a87c1-200">System. String</span><span class="sxs-lookup"><span data-stu-id="a87c1-200">System.String</span></span>

## <span data-ttu-id="a87c1-201">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a87c1-201">OUTPUTS</span></span>

### <span data-ttu-id="a87c1-202">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a87c1-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a87c1-203">Notizen</span><span class="sxs-lookup"><span data-stu-id="a87c1-203">NOTES</span></span>

## <span data-ttu-id="a87c1-204">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a87c1-204">RELATED LINKS</span></span>

[<span data-ttu-id="a87c1-205">Wiederherstellen einer Azure SQL-Datenbank aus einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="a87c1-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="a87c1-206">Wiederherstellen einer Azure SQL-Datenbank aus einem Benutzer Fehler</span><span class="sxs-lookup"><span data-stu-id="a87c1-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="a87c1-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a87c1-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="a87c1-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="a87c1-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="a87c1-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="a87c1-210">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="a87c1-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

