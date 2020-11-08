---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006609"
---
# <span data-ttu-id="92bd0-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="92bd0-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="92bd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="92bd0-103">Beendet eine fortlaufende Kopie-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="92bd0-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="92bd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92bd0-104">SYNTAX</span></span>

### <span data-ttu-id="92bd0-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92bd0-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92bd0-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="92bd0-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92bd0-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="92bd0-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92bd0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92bd0-108">DESCRIPTION</span></span>
<span data-ttu-id="92bd0-109">Das Cmdlet " **Stop-AzureSqlDatabaseCopy** " beendet eine fortlaufende Kopie-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="92bd0-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="92bd0-110">Dieses Cmdlet beendet die Datenverschiebung zwischen der Quelldatenbank und der sekundären oder Zieldatenbank und ändert dann den Zustand der sekundären Datenbank in eine eigenständige Online Datenbank.</span><span class="sxs-lookup"><span data-stu-id="92bd0-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="92bd0-111">Es gibt zwei Möglichkeiten zum Beenden einer fortlaufenden Kopier Beziehung, Kündigung oder geplanter Kündigung sowie zur erzwungenen Kündigung mit einem möglichen Datenverlust.</span><span class="sxs-lookup"><span data-stu-id="92bd0-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="92bd0-112">Auf dem Server, auf dem sich die Quelldatenbank befindet, können Sie dieses Cmdlet im Terminierungs-oder erzwungenen Beendigungsmodus ausführen.</span><span class="sxs-lookup"><span data-stu-id="92bd0-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="92bd0-113">Auf dem Server, auf dem die sekundäre Datenbank gehostet wird, müssen Sie den erzwungenen Beendigungsmodus verwenden.</span><span class="sxs-lookup"><span data-stu-id="92bd0-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="92bd0-114">Eine geplante Terminierung wartet, bis alle zugesicherten Transaktionen in der Quelldatenbank zu dem Zeitpunkt, zu dem Sie das Cmdlet ausführen, in die sekundäre Datenbank repliziert wurden.</span><span class="sxs-lookup"><span data-stu-id="92bd0-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="92bd0-115">Die erzwungene Beendigung wartet nicht auf die Replikation von ausstehenden zugesicherten Transaktionen und kann zu einem möglichen Datenverlust in der sekundären Datenbank führen.</span><span class="sxs-lookup"><span data-stu-id="92bd0-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="92bd0-116">Während der Replikationsstatus aussteht, kann nur erzwungene Beendigung eine fortlaufende Kopie-Beziehung erfolgreich beenden.</span><span class="sxs-lookup"><span data-stu-id="92bd0-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="92bd0-117">Wenn der Replikationsstatus aussteht, wird die nicht erzwungene Kündigung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92bd0-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="92bd0-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92bd0-118">EXAMPLES</span></span>

### <span data-ttu-id="92bd0-119">Beispiel 1: Abbrechen einer fortlaufenden Kopie-Beziehung</span><span class="sxs-lookup"><span data-stu-id="92bd0-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="92bd0-120">Dieser Befehl beendet die fortlaufende Kopier Beziehung der Datenbank namens Orders auf dem Server mit dem Namen lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="92bd0-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="92bd0-121">Der Server mit dem Namen bk0b8kf658 hostet die sekundäre Datenbank.</span><span class="sxs-lookup"><span data-stu-id="92bd0-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="92bd0-122">Beispiel 2: Erzwingen der Beendigung einer fortlaufenden Kopie-Beziehung</span><span class="sxs-lookup"><span data-stu-id="92bd0-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="92bd0-123">Der erste Befehl ruft die Datenbank-Kopier Beziehung für die Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen lpqd0zbr8y ab.</span><span class="sxs-lookup"><span data-stu-id="92bd0-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="92bd0-124">Mit dem zweiten Befehl wird zwangsläufig eine fortlaufende Kopier Beziehung vom Server beendet, auf dem die sekundäre Datenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="92bd0-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="92bd0-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="92bd0-125">PARAMETERS</span></span>

### <span data-ttu-id="92bd0-126">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="92bd0-126">-Database</span></span>
<span data-ttu-id="92bd0-127">Gibt ein Objekt an, das die Azure SQL-Quelldatenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="92bd0-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="92bd0-128">Dieses Cmdlet beendet die fortlaufende Kopier Beziehung der Datenbank, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="92bd0-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92bd0-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="92bd0-129">-DatabaseCopy</span></span>
<span data-ttu-id="92bd0-130">Gibt ein Objekt an, das eine Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="92bd0-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="92bd0-131">Dieses Cmdlet beendet die fortlaufende Kopier Beziehung der Datenbank, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="92bd0-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="92bd0-132">Dieser Parameter akzeptiert Pipelineeingaben.</span><span class="sxs-lookup"><span data-stu-id="92bd0-132">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92bd0-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="92bd0-133">-DatabaseName</span></span>
<span data-ttu-id="92bd0-134">Gibt den Namen einer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="92bd0-134">Specifies the name of a database.</span></span>
<span data-ttu-id="92bd0-135">Dieses Cmdlet beendet die fortlaufende Kopier Beziehung der Datenbank, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="92bd0-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bd0-136">-Force</span><span class="sxs-lookup"><span data-stu-id="92bd0-136">-Force</span></span>
<span data-ttu-id="92bd0-137">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="92bd0-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92bd0-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="92bd0-138">-ForcedTermination</span></span>
<span data-ttu-id="92bd0-139">Gibt an, dass dieses Cmdlet die erzwungene Beendigung der kontinuierlichen Kopie-Beziehung verursacht.</span><span class="sxs-lookup"><span data-stu-id="92bd0-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="92bd0-140">Die erzwungene Kündigung kann zu einem Datenverlust führen.</span><span class="sxs-lookup"><span data-stu-id="92bd0-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="92bd0-141">Wenn Sie dieses Cmdlet auf einem Server ausführen möchten, auf dem die Zieldatenbank gehostet wird, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="92bd0-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="92bd0-142">Wenn Sie dieses Cmdlet auf einem Server ausführen möchten, auf dem die Quelldatenbank gehostet wird, müssen Sie diesen Parameter angeben, wenn die sekundäre Datenbank nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="92bd0-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="92bd0-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="92bd0-143">-PartnerDatabase</span></span>
<span data-ttu-id="92bd0-144">Gibt den Namen der sekundären Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="92bd0-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="92bd0-145">Wenn Sie einen Namen angeben, muss er dem Namen der Quelldatenbank entsprechen.</span><span class="sxs-lookup"><span data-stu-id="92bd0-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bd0-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="92bd0-146">-PartnerServer</span></span>
<span data-ttu-id="92bd0-147">Gibt den Namen des Servers an, der die Zieldatenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="92bd0-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bd0-148">-Profil</span><span class="sxs-lookup"><span data-stu-id="92bd0-148">-Profile</span></span>
<span data-ttu-id="92bd0-149">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="92bd0-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92bd0-150">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="92bd0-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92bd0-151">-Servername</span><span class="sxs-lookup"><span data-stu-id="92bd0-151">-ServerName</span></span>
<span data-ttu-id="92bd0-152">Gibt den Namen des Servers an, auf dem sich die Quelldatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="92bd0-152">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92bd0-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92bd0-153">-Confirm</span></span>
<span data-ttu-id="92bd0-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92bd0-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bd0-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92bd0-155">-WhatIf</span></span>
<span data-ttu-id="92bd0-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92bd0-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92bd0-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92bd0-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bd0-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bd0-158">CommonParameters</span></span>
<span data-ttu-id="92bd0-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92bd0-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bd0-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92bd0-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bd0-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92bd0-161">INPUTS</span></span>

### <span data-ttu-id="92bd0-162">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="92bd0-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="92bd0-163">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="92bd0-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="92bd0-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92bd0-164">OUTPUTS</span></span>

### <span data-ttu-id="92bd0-165">Keine</span><span class="sxs-lookup"><span data-stu-id="92bd0-165">None</span></span>

## <span data-ttu-id="92bd0-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="92bd0-166">NOTES</span></span>
* <span data-ttu-id="92bd0-167">Authentifizierung: Dieses Cmdlet erfordert zertifikatbasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="92bd0-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="92bd0-168">Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Einrichten des aktuellen Abonnements finden Sie unter dem Cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="92bd0-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="92bd0-169">Einschränkungen: auf dem Server, auf dem die sekundäre Datenbank gehostet wird, wird nur die erzwungene Beendigung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92bd0-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="92bd0-170">Auswirkungen der Kündigung in der ehemaligen sekundären Datenbank: nach der Beendigung wird die sekundäre Datenbank zu einer unabhängigen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="92bd0-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="92bd0-171">Wenn das Seeding bereits in der sekundären Datenbank abgeschlossen ist, ist die Datenbank nach Beendigung für den Vollzugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="92bd0-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="92bd0-172">Wenn es sich bei der Quelldatenbank um eine Datenbank mit Lese-/Schreibzugriff handelt, wird auch die frühere sekundäre Datenbank zu einer Datenbank mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="92bd0-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="92bd0-173">Wenn das Seeding gerade ausgeführt wird, wird das Seeding abgebrochen, und die frühere sekundäre Datenbank wird auf dem Server, auf dem die sekundäre Datenbank gehostet wird, nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="92bd0-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="92bd0-174">Sie können die Quelldatenbank auf schreibgeschützten Modus einstellen.</span><span class="sxs-lookup"><span data-stu-id="92bd0-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="92bd0-175">Dadurch wird sichergestellt, dass die Quell-und Sekundär Datenbanken nach der Beendigung synchronisiert werden, und es wird sichergestellt, dass während der Beendigung keine Transaktionen zugesichert werden.</span><span class="sxs-lookup"><span data-stu-id="92bd0-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="92bd0-176">Nachdem die Kündigung abgeschlossen ist, stellen Sie die Quelle wieder in den Schreib-und Schreibmodus ein.</span><span class="sxs-lookup"><span data-stu-id="92bd0-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="92bd0-177">Optional können Sie auch die frühere sekundäre Datenbank auf den Lese-/Schreibzugriff einstellen.</span><span class="sxs-lookup"><span data-stu-id="92bd0-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="92bd0-178">Überwachung: Verwenden Sie das Cmdlet **Get-AzureSqlDatabaseOperation** , um den Status der Vorgänge sowohl auf Quelle als auch auf Ziel der fortlaufenden Kopie-Beziehung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="92bd0-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="92bd0-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92bd0-179">RELATED LINKS</span></span>

[<span data-ttu-id="92bd0-180">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="92bd0-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="92bd0-181">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="92bd0-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="92bd0-182">Beenden der Datenbankkopie</span><span class="sxs-lookup"><span data-stu-id="92bd0-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="92bd0-183">Azure SQL-Datenbank-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="92bd0-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="92bd0-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="92bd0-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="92bd0-185">Anfang-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="92bd0-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


