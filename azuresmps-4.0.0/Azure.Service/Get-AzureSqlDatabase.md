---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006504"
---
# <span data-ttu-id="90ffa-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="90ffa-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="90ffa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="90ffa-103">Ruft mindestens eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="90ffa-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="90ffa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90ffa-104">SYNTAX</span></span>

### <span data-ttu-id="90ffa-105">ByConnectionContext (Standard)</span><span class="sxs-lookup"><span data-stu-id="90ffa-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="90ffa-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="90ffa-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="90ffa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90ffa-107">DESCRIPTION</span></span>
<span data-ttu-id="90ffa-108">Mit dem Cmdlet **Get-AzureSqlDatabase können Sie** eine oder mehrere Instanzen einer Azure SQL-Datenbank von einem Azure SQL-Datenbankserver abrufen.</span><span class="sxs-lookup"><span data-stu-id="90ffa-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="90ffa-109">Sie können den Server mit einem Azure SQL-Datenbankserver-Verbindungskontext angeben, den Sie mit dem Cmdlet **New-AzureSqlDatabaseServerContext** erstellen.</span><span class="sxs-lookup"><span data-stu-id="90ffa-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="90ffa-110">Wenn Sie den Azure SQL-Datenbankservernamen angeben, verwendet das Cmdlet die aktuellen Azure-Abonnementinformationen, um die Anforderung für den Zugriff auf den Server zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="90ffa-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="90ffa-111">Wenn Sie keine Datenbank angeben, gibt das Cmdlet " **Get-AzureSqlDatabase** " alle Datenbanken vom angegebenen Server zurück.</span><span class="sxs-lookup"><span data-stu-id="90ffa-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="90ffa-112">Abrufen wiederherstellbarer verworfener Datenbanken:</span><span class="sxs-lookup"><span data-stu-id="90ffa-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="90ffa-113">Abrufen wiederherstellbarer verworfener Datenbanken mithilfe des *RestorableDropped* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="90ffa-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="90ffa-114">Verwenden Sie den *RestorableDropped* -Parameter ohne *DatabaseName* und *DatabaseDeletionDate* , um alle wiederherstellbaren verworfenen Datenbanken zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="90ffa-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="90ffa-115">Wenn Sie eine bestimmte wiederherstellbare gelöschte Datenbank zurückgeben möchten, verwenden Sie den Parameter *RestorableDropped* mit den Parametern *DatabaseName* und *DatabaseDeletionDate* .</span><span class="sxs-lookup"><span data-stu-id="90ffa-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="90ffa-116">Beim Abrufen einer bestimmten wiederherstellbaren gelöschten Datenbank mithilfe des *DatabaseName* -Parameters müssen Sie auch den *DatabaseDeletionDate* -Parameter einbeziehen, und der angegebene *DatabaseDeletionDate* -Wert muss Millisekunden aufweisen, damit er der gewünschten Datenbank entspricht.</span><span class="sxs-lookup"><span data-stu-id="90ffa-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="90ffa-117">Das Cmdlet " **Get-AzureSqlDatabase** " gibt entweder alle wiederherstellbaren gelöschten Datenbanken auf einem Server oder eine bestimmte Datenbank zurück, die sowohl *DatabaseName* als auch *DatabaseDeletionDate* entspricht.</span><span class="sxs-lookup"><span data-stu-id="90ffa-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="90ffa-118">Um wiederherstellbare gelöschte Datenbanken zurückzugeben, die verschiedene Kriterien erfüllen, wie etwa alle wiederherstellbaren verworfenen Datenbanken mit einem bestimmten Namen, müssen Sie alle wiederherstellbaren verworfenen Datenbanken zurückgeben und dann die Ergebnisse auf dem Client filtern.</span><span class="sxs-lookup"><span data-stu-id="90ffa-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="90ffa-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90ffa-119">EXAMPLES</span></span>

### <span data-ttu-id="90ffa-120">Beispiel 1: Abrufen aller Datenbanken auf einem Server</span><span class="sxs-lookup"><span data-stu-id="90ffa-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="90ffa-121">Dieser Befehl ruft alle Datenbanken auf dem Server mit dem Namen lpqd0zbr8y ab.</span><span class="sxs-lookup"><span data-stu-id="90ffa-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="90ffa-122">Beispiel 2: Abrufen aller wiederherstellbaren verworfenen Datenbanken auf einem Server</span><span class="sxs-lookup"><span data-stu-id="90ffa-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="90ffa-123">Dieser Befehl ruft alle wiederherstellbaren verworfenen Datenbanken auf dem Server mit dem Namen lpqd0zbr8y ab.</span><span class="sxs-lookup"><span data-stu-id="90ffa-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="90ffa-124">Beispiel 3: Abrufen einer Datenbank von einem von einem Verbindungskontext angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="90ffa-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="90ffa-125">Dieser Befehl ruft die Datenbank mit dem Namen database01 vom Server ab, der durch den Verbindungskontext $Context angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="90ffa-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="90ffa-126">Beispiel 4: Speichern eines Datenbankobjekts in einer Variablen</span><span class="sxs-lookup"><span data-stu-id="90ffa-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="90ffa-127">Dieser Befehl ruft die Datenbank mit dem Namen database01 vom Server mit dem Namen lpqd0zbr8y ab.</span><span class="sxs-lookup"><span data-stu-id="90ffa-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="90ffa-128">Der Befehl speichert das Datenbankobjekt in der Variablen $Database 01.</span><span class="sxs-lookup"><span data-stu-id="90ffa-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="90ffa-129">Beispiel 5: Abrufen einer wiederherstellbaren gelöschten Datenbank</span><span class="sxs-lookup"><span data-stu-id="90ffa-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="90ffa-130">Dieser Befehl ruft die gelöschte gelöschte Datenbank mit dem Namen database01 ab, die auf 11/9/2012 vom Server mit dem Namen lpqd0zbr8y gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="90ffa-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="90ffa-131">Dieser Befehl speichert die Ergebnisse in der $DroppedDB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="90ffa-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="90ffa-132">Beispiel 6: Abrufen aller wiederherstellbaren gelöschten Datenbanken auf einem Server und Filtern der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="90ffa-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="90ffa-133">Dieser Befehl ruft alle wiederherstellbaren gelöschten Datenbanken auf dem Server mit dem Namen lpqd0zbr8y ab und filtert die Ergebnisse dann nur auf die Datenbanken mit dem Namen ContactDB.</span><span class="sxs-lookup"><span data-stu-id="90ffa-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="90ffa-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="90ffa-134">PARAMETERS</span></span>

### <span data-ttu-id="90ffa-135">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="90ffa-135">-ConnectionContext</span></span>
<span data-ttu-id="90ffa-136">Gibt den Verbindungskontext eines Servers an, von dem eine Datenbank abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="90ffa-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90ffa-137">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="90ffa-137">-Database</span></span>
<span data-ttu-id="90ffa-138">Gibt ein Objekt an, das die Datenbank darstellt, die dieses Cmdlet abruft.</span><span class="sxs-lookup"><span data-stu-id="90ffa-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90ffa-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="90ffa-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="90ffa-140">Gibt das Datum und die Uhrzeit für den Löschvorgang an.</span><span class="sxs-lookup"><span data-stu-id="90ffa-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="90ffa-141">Wenn Sie den *RestorableDropped* -Parameter angeben, geben Sie diesen Parameter an, um eine wiederherstellbare gelöschte Datenbank basierend auf dem Datum und der Uhrzeit des Löschvorgangs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="90ffa-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="90ffa-142">Der *DatabaseDeletionDate* -Parameter muss Millisekunden aufweisen, damit er der Uhrzeit der gewünschten Datenbank entspricht.</span><span class="sxs-lookup"><span data-stu-id="90ffa-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="90ffa-143">Wenn Sie einen Wert ohne Millisekunden angeben, wird die Datenbank nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="90ffa-143">Specifying a value without milliseconds results in the database not being found.</span></span>

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

### <span data-ttu-id="90ffa-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90ffa-144">-DatabaseName</span></span>
<span data-ttu-id="90ffa-145">Gibt den Namen der Datenbank an, die dieses Cmdlet abruft.</span><span class="sxs-lookup"><span data-stu-id="90ffa-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="90ffa-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="90ffa-146">-Profile</span></span>
<span data-ttu-id="90ffa-147">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="90ffa-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="90ffa-148">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="90ffa-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90ffa-149">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="90ffa-149">-RestorableDropped</span></span>
<span data-ttu-id="90ffa-150">Gibt an, dass dieses Cmdlet *RestorableDroppedDatabase* -Objekte anstelle von *Daten Bank* Objekten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="90ffa-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="90ffa-151">Sie können den *DatabaseDeletionDate* -Parameter verwenden, um eine bestimmte zurückgegebene gelöschte Datenbank auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="90ffa-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ffa-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="90ffa-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="90ffa-153">Gibt ein Objekt an, das die zurückgegebene gelöschte Datenbank darstellt, die dieses Cmdlet abruft.</span><span class="sxs-lookup"><span data-stu-id="90ffa-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90ffa-154">-Servername</span><span class="sxs-lookup"><span data-stu-id="90ffa-154">-ServerName</span></span>
<span data-ttu-id="90ffa-155">Gibt den Namen des Servers an, der die Datenbank enthält, die dieses Cmdlet abruft.</span><span class="sxs-lookup"><span data-stu-id="90ffa-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="90ffa-156">Das Cmdlet verwendet das aktuelle Azure-Abonnement für den Zugriff auf den Server.</span><span class="sxs-lookup"><span data-stu-id="90ffa-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ffa-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ffa-157">CommonParameters</span></span>
<span data-ttu-id="90ffa-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ffa-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ffa-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90ffa-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ffa-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90ffa-160">INPUTS</span></span>

### <span data-ttu-id="90ffa-161">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="90ffa-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="90ffa-162">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="90ffa-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="90ffa-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90ffa-163">OUTPUTS</span></span>

### <span data-ttu-id="90ffa-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="90ffa-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="90ffa-165">Dieses Cmdlet gibt ein *Daten Bank* Objekt zurück, wenn Sie den *RestorableDropped* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="90ffa-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="90ffa-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="90ffa-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="90ffa-167">Dieses Cmdlet gibt ein *RestorableDroppedDatabase* -Objekt zurück, wenn Sie den *RestorableDropped* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="90ffa-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="90ffa-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="90ffa-168">NOTES</span></span>

## <span data-ttu-id="90ffa-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90ffa-169">RELATED LINKS</span></span>

[<span data-ttu-id="90ffa-170">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="90ffa-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="90ffa-171">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="90ffa-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="90ffa-172">Neu – AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="90ffa-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="90ffa-173">Neu – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="90ffa-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="90ffa-174">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="90ffa-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="90ffa-175">Satz-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="90ffa-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


