---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: 61f66a61d14738da034644fc3dfef865c8719181
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481445"
---
# <span data-ttu-id="c683e-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c683e-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="c683e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c683e-102">SYNOPSIS</span></span>
<span data-ttu-id="c683e-103">Stellt eine SQL-Datenbank wieder her.</span><span class="sxs-lookup"><span data-stu-id="c683e-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c683e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c683e-104">SYNTAX</span></span>

### <span data-ttu-id="c683e-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c683e-106">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c683e-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c683e-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c683e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-109">DESCRIPTION</span></span>
<span data-ttu-id="c683e-110">Das Cmdlet **Restore-AzureRmSqlDatabase** stellt eine SQL-Datenbank aus einer Geo-redundanten Sicherung, einer Sicherung einer gelöschten Datenbank, einer langfristigen Aufbewahrungs Sicherung oder einem Zeitpunkt in einer Livedatenbank wieder her.</span><span class="sxs-lookup"><span data-stu-id="c683e-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="c683e-111">Die wiederhergestellte Datenbank wird als neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="c683e-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="c683e-112">Sie können eine elastische SQL-Datenbank erstellen, indem Sie den *ElasticPoolName* -Parameter auf einen vorhandenen elastischen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="c683e-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="c683e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c683e-113">EXAMPLES</span></span>

### <span data-ttu-id="c683e-114">Beispiel 1: Wiederherstellen einer Datenbank ab einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="c683e-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="c683e-115">Der erste Befehl ruft die SQL-Datenbank mit dem Namen database01 ab und speichert Sie dann in der $Database-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c683e-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="c683e-116">Der zweite Befehl stellt die Datenbank in $Database aus der angegebenen Point-in-Time-Sicherung in der Datenbank mit dem Namen RestoredDatabase wieder her.</span><span class="sxs-lookup"><span data-stu-id="c683e-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="c683e-117">Beispiel 2: Wiederherstellen einer Datenbank von einem bestimmten Zeitpunkt zu einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="c683e-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="c683e-118">Der erste Befehl ruft die SQL-Datenbank mit dem Namen database01 ab und speichert Sie dann in der $Database-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c683e-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="c683e-119">Der zweite Befehl stellt die Datenbank in $Database aus der angegebenen Point-in-Time-Sicherung in der SQL-Datenbank namens RestoredDatabase im elastischen Pool mit dem Namen elasticpool01 wieder her.</span><span class="sxs-lookup"><span data-stu-id="c683e-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="c683e-120">Beispiel 3: Wiederherstellen einer gelöschten Datenbank</span><span class="sxs-lookup"><span data-stu-id="c683e-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="c683e-121">Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="c683e-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="c683e-122">Mit dem zweiten Befehl wird die Wiederherstellung aus der gelöschten Datenbanksicherung mit dem Cmdlet [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) gestartet.</span><span class="sxs-lookup"><span data-stu-id="c683e-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="c683e-123">Wenn der Parameter-PointInTime nicht angegeben wird, wird die Datenbank in der Lösch Zeit wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="c683e-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="c683e-124">Beispiel 4: Wiederherstellen einer gelöschten Datenbank in einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="c683e-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="c683e-125">Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="c683e-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="c683e-126">Mit dem zweiten Befehl wird die Wiederherstellung aus der gelöschten Datenbanksicherung mithilfe von [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)gestartet.</span><span class="sxs-lookup"><span data-stu-id="c683e-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="c683e-127">Wenn der Parameter-PointInTime nicht angegeben wird, wird die Datenbank in der Lösch Zeit wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="c683e-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="c683e-128">Beispiel 5: Geo-Restore einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="c683e-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="c683e-129">Der erste Befehl ruft die Geo-redundante Sicherung für die Datenbank mit dem Namen database01 ab und speichert Sie dann in der $GeoBackup-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c683e-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="c683e-130">Der zweite Befehl stellt die Sicherung in $GeoBackup in der SQL-Datenbank mit dem Namen RestoredDatabase wieder her.</span><span class="sxs-lookup"><span data-stu-id="c683e-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="c683e-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-131">PARAMETERS</span></span>

### <span data-ttu-id="c683e-132">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="c683e-132">-DeletionDate</span></span>
<span data-ttu-id="c683e-133">Gibt das Löschdatum als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c683e-133">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="c683e-134">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c683e-134">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c683e-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="c683e-135">-Edition</span></span>
<span data-ttu-id="c683e-136">Gibt die Edition der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="c683e-136">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="c683e-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c683e-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c683e-138">Keine</span><span class="sxs-lookup"><span data-stu-id="c683e-138">None</span></span>
- <span data-ttu-id="c683e-139">Premium</span><span class="sxs-lookup"><span data-stu-id="c683e-139">Premium</span></span>
- <span data-ttu-id="c683e-140">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="c683e-140">Basic</span></span>
- <span data-ttu-id="c683e-141">Standard</span><span class="sxs-lookup"><span data-stu-id="c683e-141">Standard</span></span>
- <span data-ttu-id="c683e-142">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="c683e-142">DataWarehouse</span></span>
- <span data-ttu-id="c683e-143">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="c683e-143">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c683e-144">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c683e-144">-ElasticPoolName</span></span>
<span data-ttu-id="c683e-145">Gibt den Namen des elastischen Pools an, in dem die SQL-Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c683e-145">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c683e-146">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-146">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="c683e-147">Gibt an, dass dieses Cmdlet eine Datenbank aus einer Sicherung einer gelöschten SQL-Datenbank wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="c683e-147">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="c683e-148">Sie können das Get-AzureRMSqlDeletedDatabaseBackup-Cmdlet verwenden, um die Sicherung einer gelöschten SQL-Datenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c683e-148">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c683e-149">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-149">-FromGeoBackup</span></span>
<span data-ttu-id="c683e-150">Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer Geo-redundanten Sicherung wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="c683e-150">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="c683e-151">Sie können das Get-AzureRMSqlDatabaseGeoBackup-Cmdlet verwenden, um eine Geo-redundante Sicherung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c683e-151">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c683e-152">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-152">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="c683e-153">Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer langfristigen Aufbewahrungs Sicherung wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="c683e-153">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c683e-154">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-154">-FromPointInTimeBackup</span></span>
<span data-ttu-id="c683e-155">Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer Point-in-Time-Sicherung wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="c683e-155">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c683e-156">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="c683e-156">-PointInTime</span></span>
<span data-ttu-id="c683e-157">Gibt den Zeitpunkt als **DateTime** -Objekt an, in dem Sie Ihre SQL-Datenbank wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="c683e-157">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="c683e-158">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c683e-158">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="c683e-159">Verwenden Sie diesen Parameter zusammen mit dem *FromPointInTimeBackup* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="c683e-159">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c683e-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c683e-160">-ResourceGroupName</span></span>
<span data-ttu-id="c683e-161">Gibt den Namen der Ressourcengruppe an, der das Cmdlet die SQL-Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="c683e-161">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="c683e-162">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c683e-162">-ResourceId</span></span>
<span data-ttu-id="c683e-163">Gibt die ID der wiederherzustellenden Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c683e-163">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="c683e-164">-Servername</span><span class="sxs-lookup"><span data-stu-id="c683e-164">-ServerName</span></span>
<span data-ttu-id="c683e-165">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="c683e-165">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="c683e-166">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="c683e-166">-ServiceObjectiveName</span></span>
<span data-ttu-id="c683e-167">Gibt den Namen des Dienst Ziels an.</span><span class="sxs-lookup"><span data-stu-id="c683e-167">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c683e-168">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="c683e-168">-TargetDatabaseName</span></span>
<span data-ttu-id="c683e-169">Gibt den Namen der Datenbank an, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c683e-169">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="c683e-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c683e-170">-DefaultProfile</span></span>
<span data-ttu-id="c683e-171">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c683e-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c683e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c683e-172">CommonParameters</span></span>
<span data-ttu-id="c683e-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c683e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c683e-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c683e-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c683e-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c683e-175">INPUTS</span></span>

## <span data-ttu-id="c683e-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c683e-176">OUTPUTS</span></span>

### <span data-ttu-id="c683e-177">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c683e-177">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c683e-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="c683e-178">NOTES</span></span>

## <span data-ttu-id="c683e-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c683e-179">RELATED LINKS</span></span>

[<span data-ttu-id="c683e-180">Wiederherstellen einer Azure SQL-Datenbank aus einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="c683e-180">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="c683e-181">Wiederherstellen einer Azure SQL-Datenbank aus einem Benutzer Fehler</span><span class="sxs-lookup"><span data-stu-id="c683e-181">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="c683e-182">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c683e-182">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="c683e-183">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-183">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="c683e-184">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="c683e-184">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="c683e-185">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c683e-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

