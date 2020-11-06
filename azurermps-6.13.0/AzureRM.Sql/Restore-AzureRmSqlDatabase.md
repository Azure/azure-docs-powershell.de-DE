---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: b4c444233701a6ecfe66eb77f90dade618c9e08f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497246"
---
# <span data-ttu-id="ba062-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba062-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="ba062-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba062-102">SYNOPSIS</span></span>
<span data-ttu-id="ba062-103">Stellt eine SQL-Datenbank wieder her.</span><span class="sxs-lookup"><span data-stu-id="ba062-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba062-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba062-104">SYNTAX</span></span>

### <span data-ttu-id="ba062-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba062-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="ba062-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba062-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba062-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="ba062-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba062-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-109">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba062-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="ba062-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba062-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba062-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="ba062-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba062-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba062-113">DESCRIPTION</span></span>
<span data-ttu-id="ba062-114">Das Cmdlet **Restore-AzureRmSqlDatabase** stellt eine SQL-Datenbank aus einer Geo-redundanten Sicherung, einer Sicherung einer gelöschten Datenbank, einer langfristigen Aufbewahrungs Sicherung oder einem Zeitpunkt in einer Livedatenbank wieder her.</span><span class="sxs-lookup"><span data-stu-id="ba062-114">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="ba062-115">Die wiederhergestellte Datenbank wird als neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="ba062-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="ba062-116">Sie können eine elastische SQL-Datenbank erstellen, indem Sie den *ElasticPoolName* -Parameter auf einen vorhandenen elastischen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="ba062-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="ba062-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba062-117">EXAMPLES</span></span>

### <span data-ttu-id="ba062-118">Beispiel 1: Wiederherstellen einer Datenbank ab einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="ba062-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="ba062-119">Der erste Befehl ruft die SQL-Datenbank mit dem Namen database01 ab und speichert Sie dann in der $Database-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ba062-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="ba062-120">Der zweite Befehl stellt die Datenbank in $Database aus der angegebenen Point-in-Time-Sicherung in der Datenbank mit dem Namen RestoredDatabase wieder her.</span><span class="sxs-lookup"><span data-stu-id="ba062-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="ba062-121">Beispiel 2: Wiederherstellen einer Datenbank von einem bestimmten Zeitpunkt zu einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="ba062-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ba062-122">Der erste Befehl ruft die SQL-Datenbank mit dem Namen database01 ab und speichert Sie dann in der $Database-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ba062-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="ba062-123">Der zweite Befehl stellt die Datenbank in $Database aus der angegebenen Point-in-Time-Sicherung in der SQL-Datenbank namens RestoredDatabase im elastischen Pool mit dem Namen elasticpool01 wieder her.</span><span class="sxs-lookup"><span data-stu-id="ba062-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="ba062-124">Beispiel 3: Wiederherstellen einer gelöschten Datenbank</span><span class="sxs-lookup"><span data-stu-id="ba062-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="ba062-125">Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ba062-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="ba062-126">Mit dem zweiten Befehl wird die Wiederherstellung aus der gelöschten Datenbanksicherung mit dem Cmdlet [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) gestartet.</span><span class="sxs-lookup"><span data-stu-id="ba062-126">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="ba062-127">Wenn der Parameter-PointInTime nicht angegeben wird, wird die Datenbank in der Lösch Zeit wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="ba062-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="ba062-128">Beispiel 4: Wiederherstellen einer gelöschten Datenbank in einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="ba062-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="ba062-129">Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ba062-129">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="ba062-130">Mit dem zweiten Befehl wird die Wiederherstellung aus der gelöschten Datenbanksicherung mithilfe von [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)gestartet.</span><span class="sxs-lookup"><span data-stu-id="ba062-130">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="ba062-131">Wenn der Parameter-PointInTime nicht angegeben wird, wird die Datenbank in der Lösch Zeit wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="ba062-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="ba062-132">Beispiel 5: Geo-Restore einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="ba062-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="ba062-133">Der erste Befehl ruft die Geo-redundante Sicherung für die Datenbank mit dem Namen database01 ab und speichert Sie dann in der $GeoBackup-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ba062-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="ba062-134">Der zweite Befehl stellt die Sicherung in $GeoBackup in der SQL-Datenbank mit dem Namen RestoredDatabase wieder her.</span><span class="sxs-lookup"><span data-stu-id="ba062-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="ba062-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba062-135">PARAMETERS</span></span>

### <span data-ttu-id="ba062-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba062-136">-AsJob</span></span>
<span data-ttu-id="ba062-137">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ba062-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba062-138">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ba062-138">-ComputeGeneration</span></span>
<span data-ttu-id="ba062-139">Die COMPUTE-Generierung, die der wiederhergestellten Datenbank zugewiesen werden soll</span><span class="sxs-lookup"><span data-stu-id="ba062-139">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="ba062-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba062-140">-DefaultProfile</span></span>
<span data-ttu-id="ba062-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ba062-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba062-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="ba062-142">-DeletionDate</span></span>
<span data-ttu-id="ba062-143">Gibt das Löschdatum als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ba062-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="ba062-144">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba062-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="ba062-145">-Edition</span><span class="sxs-lookup"><span data-stu-id="ba062-145">-Edition</span></span>
<span data-ttu-id="ba062-146">Gibt die Edition der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ba062-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="ba062-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba062-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba062-148">Keine</span><span class="sxs-lookup"><span data-stu-id="ba062-148">None</span></span>
- <span data-ttu-id="ba062-149">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="ba062-149">Basic</span></span>
- <span data-ttu-id="ba062-150">Standard</span><span class="sxs-lookup"><span data-stu-id="ba062-150">Standard</span></span>
- <span data-ttu-id="ba062-151">Premium</span><span class="sxs-lookup"><span data-stu-id="ba062-151">Premium</span></span>
- <span data-ttu-id="ba062-152">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="ba062-152">DataWarehouse</span></span>
- <span data-ttu-id="ba062-153">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="ba062-153">Free</span></span>
- <span data-ttu-id="ba062-154">Stretch</span><span class="sxs-lookup"><span data-stu-id="ba062-154">Stretch</span></span>
- <span data-ttu-id="ba062-155">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="ba062-155">GeneralPurpose</span></span>
- <span data-ttu-id="ba062-156">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="ba062-156">BusinessCritical</span></span>

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

### <span data-ttu-id="ba062-157">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ba062-157">-ElasticPoolName</span></span>
<span data-ttu-id="ba062-158">Gibt den Namen des elastischen Pools an, in dem die SQL-Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba062-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="ba062-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="ba062-160">Gibt an, dass dieses Cmdlet eine Datenbank aus einer Sicherung einer gelöschten SQL-Datenbank wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="ba062-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="ba062-161">Sie können das Get-AzureRMSqlDeletedDatabaseBackup-Cmdlet verwenden, um die Sicherung einer gelöschten SQL-Datenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba062-161">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="ba062-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-162">-FromGeoBackup</span></span>
<span data-ttu-id="ba062-163">Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer Geo-redundanten Sicherung wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="ba062-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="ba062-164">Sie können das Get-AzureRMSqlDatabaseGeoBackup-Cmdlet verwenden, um eine Geo-redundante Sicherung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba062-164">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="ba062-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="ba062-166">Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer langfristigen Aufbewahrungs Sicherung wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="ba062-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="ba062-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="ba062-168">Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer Point-in-Time-Sicherung wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="ba062-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="ba062-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ba062-169">-LicenseType</span></span>
<span data-ttu-id="ba062-170">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba062-170">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="ba062-171">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="ba062-171">-PointInTime</span></span>
<span data-ttu-id="ba062-172">Gibt den Zeitpunkt als **DateTime** -Objekt an, in dem Sie Ihre SQL-Datenbank wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ba062-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="ba062-173">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba062-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="ba062-174">Verwenden Sie diesen Parameter zusammen mit dem *FromPointInTimeBackup* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="ba062-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="ba062-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba062-175">-ResourceGroupName</span></span>
<span data-ttu-id="ba062-176">Gibt den Namen der Ressourcengruppe an, der das Cmdlet die SQL-Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="ba062-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="ba062-177">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ba062-177">-ResourceId</span></span>
<span data-ttu-id="ba062-178">Gibt die ID der wiederherzustellenden Ressource an.</span><span class="sxs-lookup"><span data-stu-id="ba062-178">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="ba062-179">-Servername</span><span class="sxs-lookup"><span data-stu-id="ba062-179">-ServerName</span></span>
<span data-ttu-id="ba062-180">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="ba062-180">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="ba062-181">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ba062-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="ba062-182">Gibt den Namen des Dienst Ziels an.</span><span class="sxs-lookup"><span data-stu-id="ba062-182">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="ba062-183">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="ba062-183">-TargetDatabaseName</span></span>
<span data-ttu-id="ba062-184">Gibt den Namen der Datenbank an, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba062-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="ba062-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="ba062-185">-VCore</span></span>
<span data-ttu-id="ba062-186">Die Vcore-Nummern der wiederhergestellten Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba062-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="ba062-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba062-187">CommonParameters</span></span>
<span data-ttu-id="ba062-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba062-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba062-189">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba062-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba062-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba062-190">INPUTS</span></span>

### <span data-ttu-id="ba062-191">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="ba062-191">System.DateTime</span></span>

### <span data-ttu-id="ba062-192">System. String</span><span class="sxs-lookup"><span data-stu-id="ba062-192">System.String</span></span>

## <span data-ttu-id="ba062-193">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba062-193">OUTPUTS</span></span>

### <span data-ttu-id="ba062-194">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ba062-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ba062-195">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba062-195">NOTES</span></span>

## <span data-ttu-id="ba062-196">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba062-196">RELATED LINKS</span></span>

[<span data-ttu-id="ba062-197">Wiederherstellen einer Azure SQL-Datenbank aus einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="ba062-197">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="ba062-198">Wiederherstellen einer Azure SQL-Datenbank aus einem Benutzer Fehler</span><span class="sxs-lookup"><span data-stu-id="ba062-198">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="ba062-199">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba062-199">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ba062-200">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-200">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="ba062-201">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="ba062-201">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="ba062-202">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ba062-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

