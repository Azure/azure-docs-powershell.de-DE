---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006501"
---
# <span data-ttu-id="8de6c-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8de6c-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="8de6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8de6c-102">SYNOPSIS</span></span>
<span data-ttu-id="8de6c-103">Überprüft den Status von Kopier Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="8de6c-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="8de6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8de6c-104">SYNTAX</span></span>

### <span data-ttu-id="8de6c-105">ByServerNameOnly (Standard)</span><span class="sxs-lookup"><span data-stu-id="8de6c-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8de6c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8de6c-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="8de6c-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="8de6c-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8de6c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8de6c-108">DESCRIPTION</span></span>
<span data-ttu-id="8de6c-109">Das Cmdlet " **Get-AzureSqlDatabaseCopy** " überprüft den Status einer oder mehrerer aktiver Kopier Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="8de6c-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="8de6c-110">Führen Sie dieses Cmdlet aus, nachdem Sie das Start-AzureSqlDatabaseCopy-oder Stop-AzureSqlDatabaseCopy-Cmdlet ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="8de6c-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="8de6c-111">Sie können eine bestimmte Kopier Beziehung, alle Kopier Beziehungen oder eine gefilterte Liste von Kopier Beziehungen überprüfen, beispielsweise alle Kopien auf einem bestimmten Zielserver.</span><span class="sxs-lookup"><span data-stu-id="8de6c-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="8de6c-112">Sie können dieses Cmdlet auf dem Server ausführen, der die Quell-oder Zieldatenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="8de6c-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="8de6c-113">Dieses Cmdlet ist synchron.</span><span class="sxs-lookup"><span data-stu-id="8de6c-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="8de6c-114">Das Cmdlet blockiert die Azure PowerShell-Konsole, bis ein Statusobjekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8de6c-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="8de6c-115">Die Parameter *PartnerServer* und *PartnerDatabase* sind optional.</span><span class="sxs-lookup"><span data-stu-id="8de6c-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="8de6c-116">Wenn Sie keinen der Parameter angeben, gibt dieses Cmdlet eine Tabelle mit Ergebnissen zurück.</span><span class="sxs-lookup"><span data-stu-id="8de6c-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="8de6c-117">Wenn Sie den Status nur für eine bestimmte Datenbank anzeigen möchten, geben Sie beide Parameter an.</span><span class="sxs-lookup"><span data-stu-id="8de6c-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="8de6c-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8de6c-118">EXAMPLES</span></span>

### <span data-ttu-id="8de6c-119">Beispiel 1: Abrufen des Kopierstatus einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="8de6c-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="8de6c-120">Dieser Befehl ruft den Status der Datenbank Orders auf dem Server mit dem Namen lpqd0zbr8y ab.</span><span class="sxs-lookup"><span data-stu-id="8de6c-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="8de6c-121">Der *PartnerServer* -Parameter schränkt diesen Befehl auf den bk0b8kf658-Server ein.</span><span class="sxs-lookup"><span data-stu-id="8de6c-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="8de6c-122">Beispiel 2: Abrufen des Status aller Kopien auf einem serverGet des Status aller Kopien auf einem Server</span><span class="sxs-lookup"><span data-stu-id="8de6c-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="8de6c-123">Dieser Befehl ruft den Status aller aktiven Kopien auf dem Server mit dem Namen lpqd0zbr8y ab.</span><span class="sxs-lookup"><span data-stu-id="8de6c-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="8de6c-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="8de6c-124">PARAMETERS</span></span>

### <span data-ttu-id="8de6c-125">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8de6c-125">-Database</span></span>
<span data-ttu-id="8de6c-126">Gibt ein Objekt an, das die Azure SQL-Quelldatenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="8de6c-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="8de6c-127">Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8de6c-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="8de6c-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8de6c-128">-DatabaseCopy</span></span>
<span data-ttu-id="8de6c-129">Gibt ein Objekt an, das eine Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="8de6c-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="8de6c-130">Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8de6c-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="8de6c-131">Dieser Parameter akzeptiert Pipelineeingaben.</span><span class="sxs-lookup"><span data-stu-id="8de6c-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="8de6c-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8de6c-132">-DatabaseName</span></span>
<span data-ttu-id="8de6c-133">Gibt den Namen der Quelldatenbank an.</span><span class="sxs-lookup"><span data-stu-id="8de6c-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="8de6c-134">Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8de6c-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de6c-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="8de6c-135">-PartnerDatabase</span></span>
<span data-ttu-id="8de6c-136">Gibt den Namen der sekundären Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="8de6c-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="8de6c-137">Wenn diese Datenbank in der sys.dm_database_copies dynamischen Verwaltungsansicht nicht gefunden wird, gibt dieses Cmdlet ein leeres Statusobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8de6c-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de6c-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="8de6c-138">-PartnerServer</span></span>
<span data-ttu-id="8de6c-139">Gibt den Namen des Servers an, der die Zieldatenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="8de6c-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="8de6c-140">Wenn dieser Server nicht in der sys.dm_database_copies dynamischen Verwaltungsansicht zu finden ist, gibt dieses Cmdlet ein leeres Statusobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8de6c-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de6c-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="8de6c-141">-Profile</span></span>
<span data-ttu-id="8de6c-142">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8de6c-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8de6c-143">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8de6c-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8de6c-144">-Servername</span><span class="sxs-lookup"><span data-stu-id="8de6c-144">-ServerName</span></span>
<span data-ttu-id="8de6c-145">Gibt den Namen des Servers an, auf dem sich die Datenbankkopie befindet.</span><span class="sxs-lookup"><span data-stu-id="8de6c-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="8de6c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de6c-146">CommonParameters</span></span>
<span data-ttu-id="8de6c-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de6c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de6c-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de6c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de6c-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8de6c-149">INPUTS</span></span>

### <span data-ttu-id="8de6c-150">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8de6c-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="8de6c-151">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="8de6c-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="8de6c-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8de6c-152">OUTPUTS</span></span>

### <span data-ttu-id="8de6c-153">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8de6c-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="8de6c-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="8de6c-154">NOTES</span></span>
* <span data-ttu-id="8de6c-155">Authentifizierung: Dieses Cmdlet erfordert zertifikatbasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="8de6c-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="8de6c-156">Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Einrichten des aktuellen Abonnements finden Sie unter New-AzureSqlDatabaseServerContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8de6c-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="8de6c-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8de6c-157">RELATED LINKS</span></span>

[<span data-ttu-id="8de6c-158">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8de6c-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="8de6c-159">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="8de6c-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="8de6c-160">Azure SQL-Datenbank-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8de6c-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="8de6c-161">Anfang-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8de6c-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="8de6c-162">Stopp-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8de6c-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


