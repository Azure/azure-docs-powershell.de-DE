---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: bfe2abe8a59114f69ec27f28ba0b270bfbbd72a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940904"
---
# <span data-ttu-id="f1dbf-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f1dbf-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="f1dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="f1dbf-103">Stellt eine SQL wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-103">Restores a SQL database.</span></span>

## <span data-ttu-id="f1dbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1dbf-104">SYNTAX</span></span>

### <span data-ttu-id="f1dbf-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1dbf-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="f1dbf-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1dbf-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1dbf-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="f1dbf-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1dbf-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1dbf-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="f1dbf-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1dbf-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1dbf-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="f1dbf-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1dbf-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1dbf-113">DESCRIPTION</span></span>
<span data-ttu-id="f1dbf-114">Das **Cmdlet Restore-AzSqlDatabase** stellt eine SQL-Datenbank aus einer georedundierten Sicherung, eine Sicherung einer gelöschten Datenbank, eine langfristige Aufbewahrungssicherung oder einen Zeitpunkt in einer Livedatenbank wieder her.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="f1dbf-115">Die wiederhergestellte Datenbank wird als neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="f1dbf-116">Sie können eine flexible SQL erstellen, indem Sie den *Parameter "ElasticPoolName"* auf einen vorhandenen Pool für einen flexiblen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="f1dbf-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1dbf-117">EXAMPLES</span></span>

### <span data-ttu-id="f1dbf-118">Beispiel 1: Wiederherstellen einer Datenbank von einem Zeitpunkt aus</span><span class="sxs-lookup"><span data-stu-id="f1dbf-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="f1dbf-119">Der erste Befehl ruft die SQL Datenbank mit dem Namen Datenbank01 ab und speichert sie dann in der $Database Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="f1dbf-120">Mit dem zweiten Befehl wird die Datenbank in $Database der angegebenen Punkt-in-Zeit-Sicherung in die Datenbank mit dem Namen RestoredDatabase wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="f1dbf-121">Beispiel 2: Wiederherstellen einer Datenbank von einem Zeitpunkt in einen Pool mit einem Flexiblen Pool</span><span class="sxs-lookup"><span data-stu-id="f1dbf-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f1dbf-122">Der erste Befehl ruft die SQL Datenbank mit dem Namen Datenbank01 ab und speichert sie dann in der $Database Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="f1dbf-123">Mit dem zweiten Befehl wird die Datenbank in $Database von der angegebenen Punkt-in-Zeit-Sicherung in die SQL-Datenbank mit dem Namen RestoredDatabase im Pool mit dem Namen "elasticpool01" wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="f1dbf-124">Beispiel 3: Wiederherstellen einer gelöschten Datenbank</span><span class="sxs-lookup"><span data-stu-id="f1dbf-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="f1dbf-125">Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzSqlDeletedDatabaseBackup wiederherstellen möchten.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="f1dbf-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="f1dbf-126">Der zweite Befehl startet die Wiederherstellung aus der gelöschten Datenbanksicherung mithilfe des [Cmdlets Restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="f1dbf-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="f1dbf-127">Wenn der Parameter -PointInTime nicht angegeben ist, wird die Datenbank zur Löschzeit wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="f1dbf-128">Beispiel 4: Wiederherstellen einer gelöschten Datenbank in einem Pool mit einem Flexiblen Pool</span><span class="sxs-lookup"><span data-stu-id="f1dbf-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="f1dbf-129">Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzSqlDeletedDatabaseBackup wiederherstellen möchten.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="f1dbf-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="f1dbf-130">Der zweite Befehl startet die Wiederherstellung aus der gelöschten Datenbanksicherung mithilfe [von Restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="f1dbf-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="f1dbf-131">Wenn der Parameter -PointInTime nicht angegeben ist, wird die Datenbank zur Löschzeit wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="f1dbf-132">Beispiel 5: Geo-Restore einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="f1dbf-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="f1dbf-133">Der erste Befehl ruft die georedundierte Sicherung für die Datenbank mit dem Namen Datenbank01 ab und speichert sie dann in der $GeoBackup Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="f1dbf-134">Mit dem zweiten Befehl wird die Sicherung in $GeoBackup datenbank SQL wiederhergestelltDatabase wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="f1dbf-135">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f1dbf-135">PARAMETERS</span></span>

### <span data-ttu-id="f1dbf-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1dbf-136">-AsJob</span></span>
<span data-ttu-id="f1dbf-137">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1dbf-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1dbf-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="f1dbf-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="f1dbf-139">Die Redundanz des Sicherungsspeichers zum Speichern von Sicherungen für die SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="f1dbf-140">Optionen sind: Lokal, Zone und Geo.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-140">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="f1dbf-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="f1dbf-141">-ComputeGeneration</span></span>
<span data-ttu-id="f1dbf-142">Die Computegenerierung, die der wiederhergestellten Datenbank zugewiesen werden soll</span><span class="sxs-lookup"><span data-stu-id="f1dbf-142">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="f1dbf-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1dbf-143">-DefaultProfile</span></span>
<span data-ttu-id="f1dbf-144">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f1dbf-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1dbf-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="f1dbf-145">-DeletionDate</span></span>
<span data-ttu-id="f1dbf-146">Gibt das Löschdatum als **DateTime-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="f1dbf-147">Um ein **DateTime-Objekt zu** erhalten, verwenden Sie das Get-Date Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="f1dbf-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="f1dbf-148">-Edition</span></span>
<span data-ttu-id="f1dbf-149">Gibt die Edition der datenbank SQL an.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="f1dbf-150">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="f1dbf-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f1dbf-151">Keine</span><span class="sxs-lookup"><span data-stu-id="f1dbf-151">None</span></span>
- <span data-ttu-id="f1dbf-152">Basic</span><span class="sxs-lookup"><span data-stu-id="f1dbf-152">Basic</span></span>
- <span data-ttu-id="f1dbf-153">Standard</span><span class="sxs-lookup"><span data-stu-id="f1dbf-153">Standard</span></span>
- <span data-ttu-id="f1dbf-154">Premium</span><span class="sxs-lookup"><span data-stu-id="f1dbf-154">Premium</span></span>
- <span data-ttu-id="f1dbf-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="f1dbf-155">DataWarehouse</span></span>
- <span data-ttu-id="f1dbf-156">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="f1dbf-156">Free</span></span>
- <span data-ttu-id="f1dbf-157">Stretch</span><span class="sxs-lookup"><span data-stu-id="f1dbf-157">Stretch</span></span>
- <span data-ttu-id="f1dbf-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="f1dbf-158">GeneralPurpose</span></span>
- <span data-ttu-id="f1dbf-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="f1dbf-159">BusinessCritical</span></span>

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

### <span data-ttu-id="f1dbf-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f1dbf-160">-ElasticPoolName</span></span>
<span data-ttu-id="f1dbf-161">Gibt den Namen des Poolpools an, in dem die Datenbank SQL werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="f1dbf-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="f1dbf-163">Gibt an, dass mit diesem Cmdlet eine Datenbank aus einer Sicherung einer gelöschten SQL wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="f1dbf-164">Sie können das Get-AzSqlDeletedDatabaseBackup-Cmdlet verwenden, um die Sicherung einer gelöschten SQL zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="f1dbf-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-165">-FromGeoBackup</span></span>
<span data-ttu-id="f1dbf-166">Gibt an, dass mit diesem Cmdlet eine SQL aus einer georedundierten Sicherung wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="f1dbf-167">Sie können das Get-AzSqlDatabaseGeoBackup-Cmdlet verwenden, um eine georedundierte Sicherung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="f1dbf-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="f1dbf-169">Gibt an, dass mit diesem Cmdlet eine SQL datenbank aus einer langfristigen Aufbewahrungssicherung wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="f1dbf-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="f1dbf-171">Gibt an, dass mit diesem Cmdlet eine SQL aus einer Punkt-in-Zeit-Sicherung wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="f1dbf-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f1dbf-172">-LicenseType</span></span>
<span data-ttu-id="f1dbf-173">Der Lizenztyp für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-173">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="f1dbf-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="f1dbf-174">-PointInTime</span></span>
<span data-ttu-id="f1dbf-175">Gibt den Zeitpunkt als **DateTime-Objekt** an, in dem Sie ihre SQL wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="f1dbf-176">Um ein **DateTime-Objekt zu** erhalten, verwenden **Sie das Get-Date-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="f1dbf-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="f1dbf-177">Verwenden Sie diesen Parameter zusammen mit *dem FromPointInTimeBackup-Parameter.*</span><span class="sxs-lookup"><span data-stu-id="f1dbf-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="f1dbf-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1dbf-178">-ResourceGroupName</span></span>
<span data-ttu-id="f1dbf-179">Gibt den Namen der Ressourcengruppe an, der dieses Cmdlet die SQL zugibt.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="f1dbf-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1dbf-180">-ResourceId</span></span>
<span data-ttu-id="f1dbf-181">Gibt die ID der ressource an, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-181">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="f1dbf-182">-Servername</span><span class="sxs-lookup"><span data-stu-id="f1dbf-182">-ServerName</span></span>
<span data-ttu-id="f1dbf-183">Gibt den Namen des datenbankservers SQL an.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-183">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="f1dbf-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f1dbf-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="f1dbf-185">Gibt den Namen des Dienstziels an.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-185">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="f1dbf-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f1dbf-186">-TargetDatabaseName</span></span>
<span data-ttu-id="f1dbf-187">Gibt den Namen der Datenbank an, in der wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="f1dbf-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="f1dbf-188">-VCore</span></span>
<span data-ttu-id="f1dbf-189">Die Vcore-Nummern der wiederhergestellten Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="f1dbf-190">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1dbf-190">-Confirm</span></span>
<span data-ttu-id="f1dbf-191">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1dbf-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1dbf-192">-WhatIf</span></span>
<span data-ttu-id="f1dbf-193">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1dbf-194">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1dbf-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1dbf-195">CommonParameters</span></span>
<span data-ttu-id="f1dbf-196">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1dbf-197">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1dbf-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1dbf-198">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1dbf-198">INPUTS</span></span>

### <span data-ttu-id="f1dbf-199">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="f1dbf-199">System.DateTime</span></span>

### <span data-ttu-id="f1dbf-200">System.String</span><span class="sxs-lookup"><span data-stu-id="f1dbf-200">System.String</span></span>

## <span data-ttu-id="f1dbf-201">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1dbf-201">OUTPUTS</span></span>

### <span data-ttu-id="f1dbf-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f1dbf-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f1dbf-203">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f1dbf-203">NOTES</span></span>

## <span data-ttu-id="f1dbf-204">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f1dbf-204">RELATED LINKS</span></span>

[<span data-ttu-id="f1dbf-205">Wiederherstellen einer Azure SQL-Datenbank nach einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="f1dbf-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="f1dbf-206">Wiederherstellen einer Azure SQL-Datenbank nach einem Benutzerfehler</span><span class="sxs-lookup"><span data-stu-id="f1dbf-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="f1dbf-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f1dbf-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="f1dbf-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="f1dbf-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="f1dbf-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="f1dbf-210">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="f1dbf-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

