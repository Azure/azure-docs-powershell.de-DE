---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: fc6c6c2756ecb1c4174fc1255c175a49f66360cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825656"
---
# <span data-ttu-id="5f731-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5f731-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="5f731-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f731-102">SYNOPSIS</span></span>
<span data-ttu-id="5f731-103">Ruft eine oder mehrere langfristige Aufbewahrungs Sicherungen ab.</span><span class="sxs-lookup"><span data-stu-id="5f731-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="5f731-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f731-104">SYNTAX</span></span>

### <span data-ttu-id="5f731-105">Standort (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f731-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [[-ResourceGroupName] <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f731-106">Servername</span><span class="sxs-lookup"><span data-stu-id="5f731-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [[-ResourceGroupName] <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f731-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="5f731-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f731-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f731-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f731-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f731-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f731-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f731-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f731-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f731-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f731-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f731-112">DESCRIPTION</span></span>
<span data-ttu-id="5f731-113">Das Cmdlet " **Get-AzSqlDatabaseLongTermRetentionBackup** " ruft alle langfristigen Aufbewahrungs Sicherungen für einen Standort, einen Server oder eine Datenbank ab oder ruft eine bestimmte langfristige Aufbewahrungs Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="5f731-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="5f731-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f731-114">EXAMPLES</span></span>

### <span data-ttu-id="5f731-115">Beispiel 1: Abrufen aller Sicherungen für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="5f731-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="5f731-116">Dieser Befehl ruft alle langfristigen Aufbewahrungs Sicherungen für alle Datenbanken ab (die möglicherweise lebendig oder gelöscht sind) in northeurope wird die Ressourcengruppe nur dann gesetzt, wenn der Server Live ist.</span><span class="sxs-lookup"><span data-stu-id="5f731-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="5f731-117">Beispiel 2: Abrufen aller Sicherungen für einen Speicherort unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5f731-117">Example 2: Get all backups for a location under a resource group</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ResourceGroup resourceGroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="5f731-118">Dieser Befehl ruft alle langfristigen Aufbewahrungs Sicherungen für alle Datenbanken (die möglicherweise lebendig oder gelöscht sind) unter einer Ressourcengruppe in northeurope ab.</span><span class="sxs-lookup"><span data-stu-id="5f731-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="5f731-119">Beispiel 3: Abrufen einer bestimmten Langzeit-Aufbewahrungs Sicherung</span><span class="sxs-lookup"><span data-stu-id="5f731-119">Example 3: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="5f731-120">Dieser Befehl ruft die Sicherung mit dem Namen 601061b7-D10B-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="5f731-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="5f731-121">Beispiel 4: Abrufen aller langfristigen Aufbewahrungs Sicherungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="5f731-121">Example 4: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="5f731-122">Dieser Befehl ruft alle langfristigen Aufbewahrungs Sicherungen für database01</span><span class="sxs-lookup"><span data-stu-id="5f731-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="5f731-123">Beispiel 5: Abrufen von langfristigen Aufbewahrungs Sicherungen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="5f731-123">Example 5: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server01
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="5f731-124">Dieser Befehl ruft alle Sicherungen mit dem Namen ab, der mit "601061b7" beginnt.</span><span class="sxs-lookup"><span data-stu-id="5f731-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="5f731-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f731-125">PARAMETERS</span></span>

### <span data-ttu-id="5f731-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="5f731-126">-BackupName</span></span>
<span data-ttu-id="5f731-127">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="5f731-127">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f731-128">-DatabaseName</span></span>
<span data-ttu-id="5f731-129">Der Name der Azure SQL-Datenbank, aus der die Sicherung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5f731-129">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="5f731-130">-DatabaseState</span></span>
<span data-ttu-id="5f731-131">Der Zustand der Datenbank, deren Sicherungen Sie suchen, lebendig, gelöscht oder alle finden möchten.</span><span class="sxs-lookup"><span data-stu-id="5f731-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="5f731-132">Standardwert für alle</span><span class="sxs-lookup"><span data-stu-id="5f731-132">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f731-133">-DefaultProfile</span></span>
<span data-ttu-id="5f731-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f731-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f731-135">-InputObject</span></span>
<span data-ttu-id="5f731-136">Das Datenbankobjekt, für das Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f731-136">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="5f731-137">-Location</span></span>
<span data-ttu-id="5f731-138">Der Speicherort des Quellservers für Backups.</span><span class="sxs-lookup"><span data-stu-id="5f731-138">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="5f731-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="5f731-140">Gibt an, ob nur die neueste Sicherung pro Datenbank abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f731-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="5f731-141">Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="5f731-141">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f731-142">-ResourceGroupName</span></span>
<span data-ttu-id="5f731-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f731-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-144">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5f731-144">-ResourceId</span></span>
<span data-ttu-id="5f731-145">Die Datenbankressourcen-ID, für die Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f731-145">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-146">-Servername</span><span class="sxs-lookup"><span data-stu-id="5f731-146">-ServerName</span></span>
<span data-ttu-id="5f731-147">Der Name des Azure SQL Server, unter dem die Sicherungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5f731-147">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f731-148">-Confirm</span></span>
<span data-ttu-id="5f731-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f731-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f731-150">-WhatIf</span></span>
<span data-ttu-id="5f731-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f731-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f731-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f731-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f731-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f731-153">CommonParameters</span></span>
<span data-ttu-id="5f731-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f731-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f731-155">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f731-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f731-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f731-156">INPUTS</span></span>

### <span data-ttu-id="5f731-157">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5f731-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="5f731-158">System. String</span><span class="sxs-lookup"><span data-stu-id="5f731-158">System.String</span></span>

## <span data-ttu-id="5f731-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f731-159">OUTPUTS</span></span>

### <span data-ttu-id="5f731-160">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="5f731-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="5f731-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f731-161">NOTES</span></span>

## <span data-ttu-id="5f731-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f731-162">RELATED LINKS</span></span>

[<span data-ttu-id="5f731-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5f731-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="5f731-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5f731-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="5f731-165">Satz-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5f731-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="5f731-166">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5f731-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)