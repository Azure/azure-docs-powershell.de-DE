---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006314"
---
# <span data-ttu-id="3abf6-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3abf6-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="3abf6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3abf6-102">SYNOPSIS</span></span>
<span data-ttu-id="3abf6-103">Löscht eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3abf6-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="3abf6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3abf6-104">SYNTAX</span></span>

### <span data-ttu-id="3abf6-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="3abf6-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3abf6-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="3abf6-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3abf6-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="3abf6-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3abf6-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="3abf6-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3abf6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3abf6-109">DESCRIPTION</span></span>
<span data-ttu-id="3abf6-110">Das Cmdlet **Remove-AzureSqlDatabase** löscht eine Azure SQL-Datenbank nach dem Server Verbindungskontext oder Servernamen.</span><span class="sxs-lookup"><span data-stu-id="3abf6-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="3abf6-111">Sie können einen Azure SQL-Datenbankserver-Verbindungskontext mithilfe des Cmdlets **New-AzureSqlDatabaseServerContext** erstellen und dann mit diesem Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="3abf6-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="3abf6-112">Wenn Sie eine Datenbank löschen, indem Sie einen Azure SQL-Datenbankservernamen angeben, verwendet das Cmdlet **Remove-AzureSqlDatabase** den Namen und die aktuellen Azure-Abonnementinformationen, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3abf6-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="3abf6-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3abf6-113">EXAMPLES</span></span>

### <span data-ttu-id="3abf6-114">Beispiel 1: Entfernen einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="3abf6-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="3abf6-115">Mit diesem Befehl wird die Datenbank namens database01 aus dem Azure SQL-Datenbankserver-Verbindungskontext $Context entfernt.</span><span class="sxs-lookup"><span data-stu-id="3abf6-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="3abf6-116">Beispiel 2: Entfernen einer Datenbank mit einem Servernamen</span><span class="sxs-lookup"><span data-stu-id="3abf6-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="3abf6-117">Dieser Befehl entfernt die Datenbank mit dem Namen database01 aus dem Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="3abf6-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="3abf6-118">Beispiel 3: Entfernen einer Datenbank mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="3abf6-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="3abf6-119">In diesem Beispiel wird die alternative Methode zum Übergeben des Datenbankobjekts durch die Pipeline veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3abf6-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="3abf6-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="3abf6-120">PARAMETERS</span></span>

### <span data-ttu-id="3abf6-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="3abf6-121">-ConnectionContext</span></span>
<span data-ttu-id="3abf6-122">Gibt den Verbindungskontext eines Servers an, auf dem mit diesem Cmdlet eine Datenbank entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3abf6-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abf6-123">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="3abf6-123">-Database</span></span>
<span data-ttu-id="3abf6-124">Gibt ein Objekt an, das die von diesem Cmdlet entfernte Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="3abf6-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3abf6-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3abf6-125">-DatabaseName</span></span>
<span data-ttu-id="3abf6-126">Gibt den Namen der Datenbank an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3abf6-126">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abf6-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3abf6-127">-Force</span></span>
<span data-ttu-id="3abf6-128">Ermöglicht die Ausführung der Aktion, ohne dass der Benutzer zur Bestätigung aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="3abf6-128">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="3abf6-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="3abf6-129">-Profile</span></span>
<span data-ttu-id="3abf6-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3abf6-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3abf6-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3abf6-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3abf6-132">-Servername</span><span class="sxs-lookup"><span data-stu-id="3abf6-132">-ServerName</span></span>
<span data-ttu-id="3abf6-133">Gibt den Namen des Servers an, auf dem dieses Cmdlet die Datenbank löscht.</span><span class="sxs-lookup"><span data-stu-id="3abf6-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abf6-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3abf6-134">-Confirm</span></span>
<span data-ttu-id="3abf6-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3abf6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3abf6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3abf6-136">-WhatIf</span></span>
<span data-ttu-id="3abf6-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3abf6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3abf6-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3abf6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3abf6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3abf6-139">CommonParameters</span></span>
<span data-ttu-id="3abf6-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3abf6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3abf6-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3abf6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3abf6-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3abf6-142">INPUTS</span></span>

### <span data-ttu-id="3abf6-143">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="3abf6-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="3abf6-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3abf6-144">OUTPUTS</span></span>

## <span data-ttu-id="3abf6-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="3abf6-145">NOTES</span></span>
* <span data-ttu-id="3abf6-146">Aufgrund des Schweregrads des Vorgangs werden Sie von diesem Cmdlet standardmäßig zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3abf6-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="3abf6-147">Um die Bestätigung zu überspringen, geben Sie den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="3abf6-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="3abf6-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3abf6-148">RELATED LINKS</span></span>

[<span data-ttu-id="3abf6-149">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="3abf6-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="3abf6-150">Datenbank löschen</span><span class="sxs-lookup"><span data-stu-id="3abf6-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="3abf6-151">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="3abf6-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="3abf6-152">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3abf6-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="3abf6-153">Neu – AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3abf6-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="3abf6-154">Neu – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="3abf6-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="3abf6-155">Satz-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3abf6-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


