---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402421"
---
# <span data-ttu-id="ea196-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ea196-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="ea196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea196-102">SYNOPSIS</span></span>
<span data-ttu-id="ea196-103">Überprüft den Status von Kopierbeziehungen.</span><span class="sxs-lookup"><span data-stu-id="ea196-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="ea196-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea196-104">SYNTAX</span></span>

### <span data-ttu-id="ea196-105">ByServerNameOnly (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea196-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea196-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea196-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea196-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="ea196-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ea196-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea196-108">DESCRIPTION</span></span>
<span data-ttu-id="ea196-109">Das **Cmdlet "Get-AzureSqlDatabaseCopy"** überprüft den Status einer oder mehreren aktiven Kopierbeziehungen.</span><span class="sxs-lookup"><span data-stu-id="ea196-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="ea196-110">Führen Sie dieses Cmdlet aus, nachdem Sie das cmdlet Start-AzureSqlDatabaseCopy oder Stop-AzureSqlDatabaseCopy ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="ea196-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="ea196-111">Sie können eine bestimmte Kopierbeziehung, alle Kopierbeziehungen oder eine gefilterte Liste von Kopierbeziehungen überprüfen, z. B. alle Kopien auf einem bestimmten Zielserver.</span><span class="sxs-lookup"><span data-stu-id="ea196-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="ea196-112">Sie können dieses Cmdlet auf dem Server ausführen, der die Quell- oder Zieldatenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="ea196-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="ea196-113">Dieses Cmdlet ist synchron.</span><span class="sxs-lookup"><span data-stu-id="ea196-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="ea196-114">Das Cmdlet blockiert die Azure PowerShell-Konsole, bis ein Statusobjekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ea196-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="ea196-115">Die *Parameter "PartnerServer"* *und "PartnerDatabase"* sind optional.</span><span class="sxs-lookup"><span data-stu-id="ea196-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="ea196-116">Wenn Sie keinen der Parameter angeben, gibt dieses Cmdlet eine Ergebnistabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="ea196-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="ea196-117">Wenn Sie nur den Status einer bestimmten Datenbank anzeigen möchten, geben Sie beide Parameter an.</span><span class="sxs-lookup"><span data-stu-id="ea196-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="ea196-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea196-118">EXAMPLES</span></span>

### <span data-ttu-id="ea196-119">Beispiel 1: Anzeigen des Kopierstatus einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="ea196-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="ea196-120">Dieser Befehl ruft den Status der Datenbank mit dem Namen "Orders" auf dem Server namens lpqd0zbr8y ab.</span><span class="sxs-lookup"><span data-stu-id="ea196-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="ea196-121">Der *Parameter "PartnerServer"* schränkt diesen Befehl auf den Server bk0b8kf658 ein.</span><span class="sxs-lookup"><span data-stu-id="ea196-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="ea196-122">Beispiel 2: Den Status aller Kopien auf einem Server erhalten: Anzeigen des Status aller Kopien auf einem Server</span><span class="sxs-lookup"><span data-stu-id="ea196-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="ea196-123">Dieser Befehl ruft den Status aller aktiven Kopien auf dem Server mit dem Namen lpqd0zbr8y ab.</span><span class="sxs-lookup"><span data-stu-id="ea196-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="ea196-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea196-124">PARAMETERS</span></span>

### <span data-ttu-id="ea196-125">-Database</span><span class="sxs-lookup"><span data-stu-id="ea196-125">-Database</span></span>
<span data-ttu-id="ea196-126">Gibt ein Objekt an, das die Azure SQL darstellt.</span><span class="sxs-lookup"><span data-stu-id="ea196-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="ea196-127">Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea196-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea196-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ea196-128">-DatabaseCopy</span></span>
<span data-ttu-id="ea196-129">Gibt ein Objekt an, das eine Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="ea196-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="ea196-130">Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea196-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="ea196-131">Dieser Parameter akzeptiert die Pipelineeingabe.</span><span class="sxs-lookup"><span data-stu-id="ea196-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="ea196-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea196-132">-DatabaseName</span></span>
<span data-ttu-id="ea196-133">Gibt den Namen der Quelldatenbank an.</span><span class="sxs-lookup"><span data-stu-id="ea196-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="ea196-134">Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea196-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea196-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="ea196-135">-PartnerDatabase</span></span>
<span data-ttu-id="ea196-136">Gibt den Namen der sekundären Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ea196-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="ea196-137">Wenn diese Datenbank nicht in der dynamischen sys.dm_database_copies gefunden wird, gibt dieses Cmdlet ein leeres Statusobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ea196-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="ea196-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="ea196-138">-PartnerServer</span></span>
<span data-ttu-id="ea196-139">Gibt den Namen des Servers an, der die Zieldatenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="ea196-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="ea196-140">Wenn dieser Server in der dynamischen sys.dm_database_copies nicht gefunden wird, gibt dieses Cmdlet ein leeres Statusobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ea196-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="ea196-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="ea196-141">-Profile</span></span>
<span data-ttu-id="ea196-142">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ea196-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea196-143">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ea196-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ea196-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea196-144">-ServerName</span></span>
<span data-ttu-id="ea196-145">Gibt den Namen des Servers an, auf dem sich die Datenbankkopie befindet.</span><span class="sxs-lookup"><span data-stu-id="ea196-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="ea196-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea196-146">CommonParameters</span></span>
<span data-ttu-id="ea196-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea196-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea196-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea196-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea196-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea196-149">INPUTS</span></span>

### <span data-ttu-id="ea196-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ea196-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="ea196-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="ea196-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="ea196-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea196-152">OUTPUTS</span></span>

### <span data-ttu-id="ea196-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ea196-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="ea196-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea196-154">NOTES</span></span>
* <span data-ttu-id="ea196-155">Authentifizierung: Für dieses Cmdlet ist zertifikatbasierte Authentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea196-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="ea196-156">Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Festlegen des aktuellen Abonnements finden Sie im New-AzureSqlDatabaseServerContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea196-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="ea196-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea196-157">RELATED LINKS</span></span>

[<span data-ttu-id="ea196-158">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="ea196-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="ea196-159">Vorgänge für Azure SQL Datenbanken</span><span class="sxs-lookup"><span data-stu-id="ea196-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[<span data-ttu-id="ea196-160">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ea196-160">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="ea196-161">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ea196-161">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


