---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005632"
---
# <span data-ttu-id="320de-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="320de-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="320de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="320de-102">SYNOPSIS</span></span>
<span data-ttu-id="320de-103">Führt eine Point-in-Time-Wiederherstellung einer Datenbank durch.</span><span class="sxs-lookup"><span data-stu-id="320de-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="320de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="320de-104">SYNTAX</span></span>

### <span data-ttu-id="320de-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="320de-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="320de-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="320de-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="320de-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="320de-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="320de-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="320de-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="320de-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="320de-109">DESCRIPTION</span></span>
<span data-ttu-id="320de-110">Das Cmdlet **Start-AzureSqlDatabaseRestore** führt eine Point-in-Time-Wiederherstellung einer Basic-, Standard-oder Premium-Datenbank durch.</span><span class="sxs-lookup"><span data-stu-id="320de-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="320de-111">Azure SQL-Datenbank speichert grundlegende Datenbanksicherungen 7 Tage, Standard für 14 Tage und Premium für 35 Tage.</span><span class="sxs-lookup"><span data-stu-id="320de-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="320de-112">Beim Wiederherstellungsvorgang wird eine neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="320de-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="320de-113">Wenn die Quelldatenbank nicht gelöscht wird, muss der *sourcedatabasename* -und der *Zieldatenbankname* -Parameter unterschiedliche Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="320de-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="320de-114">Azure SQL-Datenbank unterstützt derzeit keine serverübergreifende Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="320de-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="320de-115">Die Namen der Quell-und Zielserver müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="320de-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="320de-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="320de-116">EXAMPLES</span></span>

### <span data-ttu-id="320de-117">Beispiel 1: Wiederherstellen einer als Objekt angegebenen Datenbank bis zu einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="320de-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="320de-118">Der erste Befehl ruft ein Datenbankobjekt für die Datenbank mit dem Namen Database17 auf dem Server mit dem Namen SERVER01 ab und speichert es dann in der $Database-Variablen.</span><span class="sxs-lookup"><span data-stu-id="320de-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="320de-119">Mit dem zweiten Befehl wird die Datenbank zu einem bestimmten Zeitpunkt wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="320de-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="320de-120">Der Befehl gibt den Namen für die neue Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="320de-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="320de-121">Beispiel 2: Wiederherstellen einer vom Namen angegebenen Datenbank zu einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="320de-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="320de-122">Mit diesem Befehl wird die Datenbank mit dem Namen Database17 zu einem bestimmten Zeitpunkt wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="320de-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="320de-123">Der Befehl gibt den Namen für die neue Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="320de-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="320de-124">Beispiel 3: Wiederherstellen einer gelöschten Datenbank, die als Objekt auf einen Zeitpunkt festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="320de-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="320de-125">Der erste Befehl ruft ein Datenbankobjekt für die Datenbank mit dem Namen Database01 auf dem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="320de-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="320de-126">Der Befehl gibt den *RestorableDropped* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="320de-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="320de-127">Aus diesem Grund erhält das Cmdlet eine wiederherstellbare gelöschte Datenbank zum angegebenen Wiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="320de-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="320de-128">Der Befehl speichert das Datenbankobjekt in der $Database Variablen.</span><span class="sxs-lookup"><span data-stu-id="320de-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="320de-129">Der zweite Befehl stellt die von $Database angegebene gelöschte Datenbank wieder her.</span><span class="sxs-lookup"><span data-stu-id="320de-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="320de-130">Der Befehl gibt den Namen für die neue Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="320de-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="320de-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="320de-131">PARAMETERS</span></span>

### <span data-ttu-id="320de-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="320de-132">-PointInTime</span></span>
<span data-ttu-id="320de-133">Gibt den Wiederherstellungspunkt an, auf den die Datenbank wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="320de-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="320de-134">Nach Abschluss des Wiederherstellungsvorgangs wird die Datenbank in dem Zustand wiederhergestellt, in dem Sie sich zu dem Datum und der Uhrzeit befand, zu dem dieser Parameter angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="320de-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="320de-135">Bei einer Livedatenbank, die auf die aktuelle Uhrzeit und für eine gelöschte Datenbank eingestellt ist, verwendet dieses Cmdlet standardmäßig den Zeitpunkt, zu dem die Datenbank gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="320de-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="320de-136">-Profile</span></span>
<span data-ttu-id="320de-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="320de-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="320de-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="320de-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-139">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="320de-139">-RestorableDropped</span></span>
<span data-ttu-id="320de-140">Gibt an, dass dieses Cmdlet eine wiederherstellbare gelöschte Datenbank wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="320de-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-141">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="320de-141">-SourceDatabase</span></span>
<span data-ttu-id="320de-142">Gibt den Namen der Datenbank an, die von diesem Cmdlet wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="320de-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="320de-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="320de-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="320de-144">Gibt das Datum und die Uhrzeit an, zu dem die Datenbank gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="320de-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="320de-145">Sie müssen Millisekunden einbeziehen, wenn Sie die Zeit angeben, die mit der tatsächlichen Lösch Zeit der Datenbank übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="320de-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="320de-146">-SourceDatabaseName</span></span>
<span data-ttu-id="320de-147">Gibt den Namen der Livedatenbank an, die von diesem Cmdlet wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="320de-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="320de-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="320de-149">Gibt ein Objekt an, das die wiederherstellbare gelöschte Datenbank darstellt, die von diesem Cmdlet wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="320de-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="320de-150">Verwenden Sie zum Abrufen eines **RestorableDroppedDatabase** -Objekts das Get-AzureSqlDatabase-Cmdlet, und geben Sie den *RestorableDropped* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="320de-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="320de-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="320de-151">-SourceServerName</span></span>
<span data-ttu-id="320de-152">Gibt den Namen des Servers an, auf dem die Quelldatenbank Live ausgeführt wird, oder auf dem die Quelldatenbank ausgeführt wurde, bevor Sie gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="320de-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-153">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="320de-153">-TargetDatabaseName</span></span>
<span data-ttu-id="320de-154">Gibt den Namen der neuen Datenbank an, die vom Wiederherstellungsvorgang erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="320de-154">Specifies the name of the new database that the restore operation creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="320de-155">-TargetServerName</span></span>
<span data-ttu-id="320de-156">Gibt den Namen des Servers an, auf dem dieses Cmdlet die Datenbank wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="320de-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="320de-157">Azure SQL-Datenbank unterstützt derzeit keine serverübergreifende Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="320de-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="320de-158">Die Namen der Quell-und Zielserver müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="320de-158">The source and target server names must be the same.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320de-159">CommonParameters</span></span>
<span data-ttu-id="320de-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320de-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320de-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320de-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320de-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="320de-162">INPUTS</span></span>

### <span data-ttu-id="320de-163">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="320de-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="320de-164">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="320de-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="320de-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="320de-165">OUTPUTS</span></span>

### <span data-ttu-id="320de-166">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestoreDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="320de-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="320de-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="320de-167">NOTES</span></span>
* <span data-ttu-id="320de-168">Sie müssen dieses Cmdlet mithilfe der zertifikatbasierten Authentifizierung ausführen.</span><span class="sxs-lookup"><span data-stu-id="320de-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="320de-169">Führen Sie die folgenden Befehle auf dem Computer aus, auf dem dieses Cmdlet ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="320de-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="320de-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="320de-170">RELATED LINKS</span></span>

[<span data-ttu-id="320de-171">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="320de-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="320de-172">Erstellen einer Daten Bank Wiederherstellungsanforderung</span><span class="sxs-lookup"><span data-stu-id="320de-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="320de-173">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="320de-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="320de-174">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="320de-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


