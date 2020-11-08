---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005629"
---
# <span data-ttu-id="5dc32-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="5dc32-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="5dc32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5dc32-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc32-103">Initiiert eine Wiederherstellungsanforderung für eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5dc32-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="5dc32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dc32-104">SYNTAX</span></span>

### <span data-ttu-id="5dc32-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5dc32-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5dc32-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5dc32-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5dc32-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dc32-107">DESCRIPTION</span></span>
<span data-ttu-id="5dc32-108">Das Cmdlet **Start-AzureSqlDatabaseRecovery** initiiert eine Wiederherstellungsanforderung für eine Live-oder gelöschte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5dc32-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="5dc32-109">Dieses Cmdlet unterstützt die grundlegende Wiederherstellung, die die letzte bekanntermaßen verfügbare Sicherung für die Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="5dc32-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="5dc32-110">Beim Wiederherstellungsvorgang wird eine neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="5dc32-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="5dc32-111">Wenn Sie eine Livedatenbank auf demselben Server wiederherstellen, müssen Sie einen anderen Namen für die neue Datenbank angeben.</span><span class="sxs-lookup"><span data-stu-id="5dc32-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="5dc32-112">Wenn Sie eine Point-in-Time-Wiederherstellung für eine Datenbank ausführen möchten, verwenden Sie stattdessen das Cmdlet **Start-AzureSqlDatabaseRestore** .</span><span class="sxs-lookup"><span data-stu-id="5dc32-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="5dc32-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5dc32-113">EXAMPLES</span></span>

### <span data-ttu-id="5dc32-114">Beispiel 1: Wiederherstellen einer als Objekt angegebenen Datenbank</span><span class="sxs-lookup"><span data-stu-id="5dc32-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="5dc32-115">Der erste Befehl ruft ein Datenbankobjekt mit dem Cmdlet **Get-AzureSqlRecoverableDatabase** ab.</span><span class="sxs-lookup"><span data-stu-id="5dc32-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="5dc32-116">Der Befehl speichert das Objekt in der $Database Variablen.</span><span class="sxs-lookup"><span data-stu-id="5dc32-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="5dc32-117">Mit dem zweiten Befehl wird die in $Database gespeicherte Datenbank erneut hergestellt.</span><span class="sxs-lookup"><span data-stu-id="5dc32-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="5dc32-118">Beispiel 2: Wiederherstellen einer durch den Namen angegebenen Datenbank</span><span class="sxs-lookup"><span data-stu-id="5dc32-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="5dc32-119">Mit diesem Befehl wird eine Datenbank mit dem Datenbanknamen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5dc32-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="5dc32-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dc32-120">PARAMETERS</span></span>

### <span data-ttu-id="5dc32-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="5dc32-121">-Profile</span></span>
<span data-ttu-id="5dc32-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5dc32-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5dc32-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5dc32-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5dc32-124">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="5dc32-124">-SourceDatabase</span></span>
<span data-ttu-id="5dc32-125">Gibt das Database-Objekt an, das die Datenbank darstellt, die von diesem Cmdlet erneut hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5dc32-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dc32-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5dc32-126">-SourceDatabaseName</span></span>
<span data-ttu-id="5dc32-127">Gibt den Namen der Datenbank an, die von diesem Cmdlet erneut hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5dc32-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dc32-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="5dc32-128">-SourceServerName</span></span>
<span data-ttu-id="5dc32-129">Gibt den Namen des Servers an, auf dem die Quelldatenbank Live ausgeführt wird, oder auf dem die Quelldatenbank ausgeführt wurde, bevor Sie gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="5dc32-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dc32-130">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="5dc32-130">-TargetDatabaseName</span></span>
<span data-ttu-id="5dc32-131">Gibt den Namen der wiederhergestellten Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="5dc32-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="5dc32-132">Wenn die Quelldatenbank weiterhin aktiv ist, müssen Sie einen Namen angeben, der vom Quelldaten Banknamen abweicht, um ihn auf demselben Server wiederherstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="5dc32-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

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

### <span data-ttu-id="5dc32-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="5dc32-133">-TargetServerName</span></span>
<span data-ttu-id="5dc32-134">Gibt den Namen des Servers an, für den eine Datenbank wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dc32-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="5dc32-135">Sie können eine Datenbank auf demselben Server oder auf einem anderen Server wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="5dc32-135">You can restore a database to the same server or to a different server.</span></span>

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

### <span data-ttu-id="5dc32-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc32-136">CommonParameters</span></span>
<span data-ttu-id="5dc32-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dc32-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc32-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dc32-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc32-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5dc32-139">INPUTS</span></span>

### <span data-ttu-id="5dc32-140">Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="5dc32-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="5dc32-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5dc32-141">OUTPUTS</span></span>

### <span data-ttu-id="5dc32-142">Microsoft. WindowsAzure. Management. SQL. Models. RecoverDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="5dc32-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="5dc32-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5dc32-143">NOTES</span></span>
* <span data-ttu-id="5dc32-144">Sie müssen dieses Cmdlet mithilfe der zertifikatbasierten Authentifizierung ausführen.</span><span class="sxs-lookup"><span data-stu-id="5dc32-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="5dc32-145">Führen Sie die folgenden Befehle auf dem Computer aus, auf dem Sie dieses Cmdlet ausführen:</span><span class="sxs-lookup"><span data-stu-id="5dc32-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="5dc32-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5dc32-146">RELATED LINKS</span></span>

[<span data-ttu-id="5dc32-147">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5dc32-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5dc32-148">Erstellen einer Daten Bank Wiederherstellungsanforderung</span><span class="sxs-lookup"><span data-stu-id="5dc32-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="5dc32-149">Geo-Replikation in Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5dc32-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="5dc32-150">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="5dc32-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5dc32-151">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="5dc32-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="5dc32-152">Anfang-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="5dc32-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)


