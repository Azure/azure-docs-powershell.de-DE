---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006499"
---
# <span data-ttu-id="f9053-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="f9053-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="f9053-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9053-102">SYNOPSIS</span></span>
<span data-ttu-id="f9053-103">Ruft den Status von Datenbankvorgängen auf einem Azure-Server ab.</span><span class="sxs-lookup"><span data-stu-id="f9053-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="f9053-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9053-104">SYNTAX</span></span>

### <span data-ttu-id="f9053-105">ByConnectionContext (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9053-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f9053-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="f9053-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f9053-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9053-107">DESCRIPTION</span></span>
<span data-ttu-id="f9053-108">Das Cmdlet " **Get-AzureSqlDatabaseOperation** " Ruft den Status von Datenbankvorgängen auf dem angegebenen Azure-Server ab.</span><span class="sxs-lookup"><span data-stu-id="f9053-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="f9053-109">Wenn Sie nur den Parameter *Servername* oder *ConnectionContext* angeben, ruft das Cmdlet alle Datenbankvorgänge für den Server ab.</span><span class="sxs-lookup"><span data-stu-id="f9053-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="f9053-110">Wenn Sie auch eine Datenbank mithilfe des *Database* -oder *DatabaseName* -Parameters angeben, ruft dieses Cmdlet alle Vorgänge für die angegebene Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="f9053-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="f9053-111">Wenn Sie eine Vorgangs-GUID und *Servername* oder *ConnectionContext* angeben, ruft das Cmdlet einen einzelnen Datenbankvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="f9053-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="f9053-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9053-112">EXAMPLES</span></span>

### <span data-ttu-id="f9053-113">Beispiel 1: Abrufen des Status aller Datenbankvorgänge für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="f9053-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="f9053-114">Dieser Befehl ruft den Status aller Datenbankvorgänge in der Datenbank mit dem Namen Database17 auf dem Server ab, der vom Verbindungskontext $Context angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9053-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="f9053-115">Beispiel 2: Abrufen des Status aller Datenbankvorgänge für einen Server</span><span class="sxs-lookup"><span data-stu-id="f9053-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="f9053-116">Dieser Befehl ruft den Status aller Datenbankvorgänge auf dem Server ab, die vom Verbindungskontext $Context angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f9053-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="f9053-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9053-117">PARAMETERS</span></span>

### <span data-ttu-id="f9053-118">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="f9053-118">-ConnectionContext</span></span>
<span data-ttu-id="f9053-119">Gibt den Verbindungskontext eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="f9053-119">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="f9053-120">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f9053-120">-Database</span></span>
<span data-ttu-id="f9053-121">Gibt ein Objekt an, das eine Azure SQL-Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="f9053-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="f9053-122">Wenn Sie diesen Parameter angeben, müssen Sie den Parameter *Servername* oder *ConnectionContext* angeben.</span><span class="sxs-lookup"><span data-stu-id="f9053-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

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

### <span data-ttu-id="f9053-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f9053-123">-DatabaseName</span></span>
<span data-ttu-id="f9053-124">Gibt den Namen einer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="f9053-124">Specifies the name of a database.</span></span>
<span data-ttu-id="f9053-125">Wenn Sie diesen Parameter angeben, müssen Sie den *Servername* -Parameter oder den *ConnectionContext* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f9053-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9053-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="f9053-126">-OperationGuid</span></span>
<span data-ttu-id="f9053-127">Gibt die Vorgangs-ID an, die einen bestimmten Datenbankvorgang darstellt, für den dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="f9053-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="f9053-128">Sie können Vorgangs-IDs abrufen, indem Sie alle Datenbankvorgänge für eine Azure SQL-Datenbank oder einen Server anfordern.</span><span class="sxs-lookup"><span data-stu-id="f9053-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="f9053-129">Wenn Sie diesen Parameter angeben, müssen Sie den *Servername* -Parameter oder den *ConnectionContext* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f9053-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9053-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="f9053-130">-Profile</span></span>
<span data-ttu-id="f9053-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f9053-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f9053-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f9053-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f9053-133">-Servername</span><span class="sxs-lookup"><span data-stu-id="f9053-133">-ServerName</span></span>
<span data-ttu-id="f9053-134">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="f9053-134">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="f9053-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9053-135">CommonParameters</span></span>
<span data-ttu-id="f9053-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9053-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9053-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9053-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9053-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9053-138">INPUTS</span></span>

### <span data-ttu-id="f9053-139">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="f9053-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="f9053-140">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f9053-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="f9053-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f9053-141">System.Guid</span></span>

## <span data-ttu-id="f9053-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9053-142">OUTPUTS</span></span>

### <span data-ttu-id="f9053-143">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponseList []</span><span class="sxs-lookup"><span data-stu-id="f9053-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="f9053-144">Dieses Cmdlet gibt ein Array von **DatabaseOperationResponseList** -Objekten zurück, wenn mehrere Vorgänge abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9053-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="f9053-145">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f9053-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="f9053-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9053-146">NOTES</span></span>

## <span data-ttu-id="f9053-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9053-147">RELATED LINKS</span></span>

[<span data-ttu-id="f9053-148">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f9053-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="f9053-149">Status des Datenbankvorgangs</span><span class="sxs-lookup"><span data-stu-id="f9053-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="f9053-150">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="f9053-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f9053-151">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9053-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="f9053-152">Neu – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f9053-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


