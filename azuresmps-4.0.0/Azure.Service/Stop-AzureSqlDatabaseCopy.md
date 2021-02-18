---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405617"
---
# <span data-ttu-id="03f87-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="03f87-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="03f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03f87-102">SYNOPSIS</span></span>
<span data-ttu-id="03f87-103">Beendet eine fortlaufende Kopierbeziehung.</span><span class="sxs-lookup"><span data-stu-id="03f87-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="03f87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03f87-104">SYNTAX</span></span>

### <span data-ttu-id="03f87-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03f87-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03f87-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="03f87-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03f87-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="03f87-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03f87-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03f87-108">DESCRIPTION</span></span>
<span data-ttu-id="03f87-109">Das **Cmdlet "Stop-AzureSqlDatabaseCopy"** beendet eine fortlaufende Kopierbeziehung.</span><span class="sxs-lookup"><span data-stu-id="03f87-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="03f87-110">Dieses Cmdlet stoppt die Datenbewegung zwischen der Quelldatenbank und der sekundären oder Zieldatenbank und ändert dann den Zustand der sekundären Datenbank in eine eigenständige Onlinedatenbank.</span><span class="sxs-lookup"><span data-stu-id="03f87-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="03f87-111">Es gibt zwei Möglichkeiten, eine fortlaufende Kopierbeziehung zu beenden: Beendigung oder geplante Beendigung und erzwungene Beendigung mit möglichem Datenverlust.</span><span class="sxs-lookup"><span data-stu-id="03f87-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="03f87-112">Auf dem Server, der die Quelldatenbank hostet, können Sie dieses Cmdlet im Beendigungs- oder Beendigungsmodus ausführen.</span><span class="sxs-lookup"><span data-stu-id="03f87-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="03f87-113">Auf dem Server, der die sekundäre Datenbank hostet, müssen Sie den Modus für erzwungene Beendigung verwenden.</span><span class="sxs-lookup"><span data-stu-id="03f87-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="03f87-114">Eine geplante Beendigung wartet, bis alle für die Quelldatenbank vorgesehenen Transaktionen zum Zeitpunkt der Ausführung des Cmdlets in der sekundären Datenbank repliziert wurden.</span><span class="sxs-lookup"><span data-stu-id="03f87-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="03f87-115">Bei einer erzwungenen Beendigung wird nicht auf die Replikation noch ausstehender gebundener Transaktionen gewartet, und es kann zu einem möglichen Datenverlust in der sekundären Datenbank kommen.</span><span class="sxs-lookup"><span data-stu-id="03f87-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="03f87-116">Während der Replikationsstatus AUSSTEHEND ist, kann eine fortlaufende Kopierbeziehung nur durch eine erzwungene Beendigung erfolgreich beendet werden.</span><span class="sxs-lookup"><span data-stu-id="03f87-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="03f87-117">Wenn der Replikationsstatus "AUSSTEHEND" ist, wird eine nicht erzwungene Beendigung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03f87-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="03f87-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03f87-118">EXAMPLES</span></span>

### <span data-ttu-id="03f87-119">Beispiel 1: Beenden einer fortlaufenden Kopierbeziehung</span><span class="sxs-lookup"><span data-stu-id="03f87-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="03f87-120">Dieser Befehl beendet die fortlaufende Kopierbeziehung der Datenbank "Orders" auf dem Server mit dem Namen "lpqd0zbr8y".</span><span class="sxs-lookup"><span data-stu-id="03f87-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="03f87-121">Der Server mit dem Namen bk0b8kf658 hostet die sekundäre Datenbank.</span><span class="sxs-lookup"><span data-stu-id="03f87-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="03f87-122">Beispiel 2: Zcibly terminate a continuous copy relationship</span><span class="sxs-lookup"><span data-stu-id="03f87-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="03f87-123">Der erste Befehl ruft die Datenbankkopiebeziehung für die Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen "lpqd0zbr8y" ab.</span><span class="sxs-lookup"><span data-stu-id="03f87-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="03f87-124">Der zweite Befehl beendet eine fortlaufende Kopierbeziehung vom Server, der die sekundäre Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="03f87-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="03f87-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03f87-125">PARAMETERS</span></span>

### <span data-ttu-id="03f87-126">-Database</span><span class="sxs-lookup"><span data-stu-id="03f87-126">-Database</span></span>
<span data-ttu-id="03f87-127">Gibt ein Objekt an, das die Azure SQL darstellt.</span><span class="sxs-lookup"><span data-stu-id="03f87-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="03f87-128">Dieses Cmdlet beendet die fortlaufende Kopierbeziehung der Datenbank, die mit diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="03f87-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="03f87-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="03f87-129">-DatabaseCopy</span></span>
<span data-ttu-id="03f87-130">Gibt ein Objekt an, das eine Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="03f87-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="03f87-131">Dieses Cmdlet beendet die fortlaufende Kopierbeziehung der Datenbank, die mit diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="03f87-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="03f87-132">Dieser Parameter akzeptiert die Pipelineeingabe.</span><span class="sxs-lookup"><span data-stu-id="03f87-132">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="03f87-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="03f87-133">-DatabaseName</span></span>
<span data-ttu-id="03f87-134">Gibt den Namen einer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="03f87-134">Specifies the name of a database.</span></span>
<span data-ttu-id="03f87-135">Dieses Cmdlet beendet die fortlaufende Kopierbeziehung der Datenbank, die mit diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="03f87-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="03f87-136">-Force</span><span class="sxs-lookup"><span data-stu-id="03f87-136">-Force</span></span>
<span data-ttu-id="03f87-137">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="03f87-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03f87-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="03f87-138">-ForcedTermination</span></span>
<span data-ttu-id="03f87-139">Gibt an, dass dieses Cmdlet eine erzwungene Beendigung der fortlaufenden Kopierbeziehung bewirkt.</span><span class="sxs-lookup"><span data-stu-id="03f87-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="03f87-140">Eine erzwungene Beendigung kann zu Datenverlust führen.</span><span class="sxs-lookup"><span data-stu-id="03f87-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="03f87-141">Um dieses Cmdlet auf einem Server ausführen zu können, der die Zieldatenbank hostet, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="03f87-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="03f87-142">Wenn Sie dieses Cmdlet auf einem Server ausführen möchten, der die Quelldatenbank hostet, müssen Sie diesen Parameter angeben, wenn die sekundäre Datenbank nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="03f87-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="03f87-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="03f87-143">-PartnerDatabase</span></span>
<span data-ttu-id="03f87-144">Gibt den Namen der sekundären Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="03f87-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="03f87-145">Wenn Sie einen Namen angeben, muss er mit dem Namen der Quelldatenbank übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="03f87-145">If you specify a name, it must match the name of the source database.</span></span>

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

### <span data-ttu-id="03f87-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="03f87-146">-PartnerServer</span></span>
<span data-ttu-id="03f87-147">Gibt den Namen des Servers an, der die Zieldatenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="03f87-147">Specifies the name of the server that hosts the target database.</span></span>

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

### <span data-ttu-id="03f87-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="03f87-148">-Profile</span></span>
<span data-ttu-id="03f87-149">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="03f87-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03f87-150">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="03f87-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="03f87-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="03f87-151">-ServerName</span></span>
<span data-ttu-id="03f87-152">Gibt den Namen des Servers an, auf dem sich die Quelldatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="03f87-152">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="03f87-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03f87-153">-Confirm</span></span>
<span data-ttu-id="03f87-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03f87-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03f87-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="03f87-155">-WhatIf</span></span>
<span data-ttu-id="03f87-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03f87-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03f87-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03f87-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03f87-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f87-158">CommonParameters</span></span>
<span data-ttu-id="03f87-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03f87-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f87-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03f87-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f87-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03f87-161">INPUTS</span></span>

### <span data-ttu-id="03f87-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="03f87-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="03f87-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="03f87-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="03f87-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03f87-164">OUTPUTS</span></span>

### <span data-ttu-id="03f87-165">Keine</span><span class="sxs-lookup"><span data-stu-id="03f87-165">None</span></span>

## <span data-ttu-id="03f87-166">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="03f87-166">NOTES</span></span>
* <span data-ttu-id="03f87-167">Authentifizierung: Für dieses Cmdlet ist zertifikatbasierte Authentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="03f87-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="03f87-168">Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Festlegen des aktuellen Abonnements finden Sie im **Cmdlet "New-AzureSqlDatabaseServerContext".**</span><span class="sxs-lookup"><span data-stu-id="03f87-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="03f87-169">Einschränkungen: Auf dem Server, der die sekundäre Datenbank hostet, wird nur eine erzwungene Beendigung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03f87-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="03f87-170">Auswirkungen einer Beendigung auf die ehemalige sekundäre Datenbank: Nach der Beendigung wird die sekundäre Datenbank zu einer unabhängigen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="03f87-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="03f87-171">Wenn das Starting für die sekundäre Datenbank bereits abgeschlossen ist, ist diese Datenbank nach dem Beenden für den Vollzugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="03f87-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="03f87-172">Wenn es sich bei der Quelldatenbank um eine Datenbank mit Lese-/Schreibzugriff handelt, wird aus der früheren sekundären Datenbank auch eine Datenbank mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="03f87-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="03f87-173">Wenn das Startprojekt zurzeit ausgeführt wird, wird das Startprojekt abgebrochen, und die frühere sekundäre Datenbank wird auf dem Server, auf dem sich die sekundäre Datenbank befindet, nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="03f87-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="03f87-174">Sie können für die Quelldatenbank den schreibgeschützten Modus festlegen.</span><span class="sxs-lookup"><span data-stu-id="03f87-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="03f87-175">Dadurch wird sichergestellt, dass Quelldatenbanken und sekundäre Datenbanken nach dem Beenden synchronisiert werden, und es wird sichergestellt, dass während der Beendigung keine Transaktionen gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="03f87-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="03f87-176">Nachdem die Beendigung abgeschlossen ist, legen Sie die Quelle wieder auf den Lese-/Schreibmodus zurück.</span><span class="sxs-lookup"><span data-stu-id="03f87-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="03f87-177">Optional können Sie auch die frühere sekundäre Datenbank auf den Lese-/Schreibmodus festlegen.</span><span class="sxs-lookup"><span data-stu-id="03f87-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="03f87-178">Überwachung: Verwenden Sie das Cmdlet **"Get-AzureSqlDatabaseOperation",** um den Status der Vorgänge sowohl an der Quelle als auch am Ziel der fortlaufenden Kopierbeziehung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="03f87-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="03f87-179">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="03f87-179">RELATED LINKS</span></span>

[<span data-ttu-id="03f87-180">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="03f87-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="03f87-181">Vorgänge für Azure SQL Datenbanken</span><span class="sxs-lookup"><span data-stu-id="03f87-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="03f87-182">Beenden der Datenbankkopie</span><span class="sxs-lookup"><span data-stu-id="03f87-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[<span data-ttu-id="03f87-183">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="03f87-183">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="03f87-184">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="03f87-184">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


