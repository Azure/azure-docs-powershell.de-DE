---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144209"
---
# <span data-ttu-id="4a353-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4a353-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="4a353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a353-102">SYNOPSIS</span></span>
<span data-ttu-id="4a353-103">Ruft mindestens eine langfristige Aufbewahrungssicherung ab.</span><span class="sxs-lookup"><span data-stu-id="4a353-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="4a353-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a353-104">SYNTAX</span></span>

### <span data-ttu-id="4a353-105">Ort (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a353-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a353-106">Servername</span><span class="sxs-lookup"><span data-stu-id="4a353-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a353-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="4a353-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a353-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a353-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a353-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a353-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a353-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a353-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a353-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a353-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a353-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a353-112">DESCRIPTION</span></span>
<span data-ttu-id="4a353-113">Das **Cmdlet "Get-AzSqlDatabaseLongTermRetentionBackup"** ruft alle langfristigen Aufbewahrungssicherungen für einen Speicherort, Server oder eine Datenbank ab oder ruft eine bestimmte langfristige Aufbewahrungssicherung ab.</span><span class="sxs-lookup"><span data-stu-id="4a353-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="4a353-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a353-114">EXAMPLES</span></span>

### <span data-ttu-id="4a353-115">Beispiel 1: Alle Sicherungen für einen Speicherort erhalten</span><span class="sxs-lookup"><span data-stu-id="4a353-115">Example 1: Get all backups for a location</span></span>
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

<span data-ttu-id="4a353-116">Mit diesem Befehl werden alle langfristigen Aufbewahrungssicherungen für alle Datenbanken (die in Northeurope gespeichert oder gelöscht werden können) nur dann festgelegt, wenn der Server live ist.</span><span class="sxs-lookup"><span data-stu-id="4a353-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="4a353-117">Beispiel 2: Alle Sicherungen für einen Speicherort unter einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="4a353-117">Example 2: Get all backups for a location under a resource group</span></span>
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

<span data-ttu-id="4a353-118">Dieser Befehl ruft alle langfristigen Aufbewahrungssicherungen für alle Datenbanken (die möglicherweise lebendig oder gelöscht werden) unter einer Ressourcengruppe in Northeurope ab.</span><span class="sxs-lookup"><span data-stu-id="4a353-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="4a353-119">Beispiel 3: Erhalten einer bestimmten langfristigen Aufbewahrungssicherung</span><span class="sxs-lookup"><span data-stu-id="4a353-119">Example 3: Get a specific long term retention backup</span></span>
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

<span data-ttu-id="4a353-120">Dieser Befehl ruft die Sicherung mit dem Namen 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span><span class="sxs-lookup"><span data-stu-id="4a353-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="4a353-121">Beispiel 4: Alle langfristigen Aufbewahrungssicherungen für eine Datenbank erhalten</span><span class="sxs-lookup"><span data-stu-id="4a353-121">Example 4: Get all long term retention backups for a database</span></span>
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

<span data-ttu-id="4a353-122">Dieser Befehl ruft alle langfristigen Aufbewahrungssicherungen für Datenbank01 ab.</span><span class="sxs-lookup"><span data-stu-id="4a353-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="4a353-123">Beispiel 5: Erhalten von langfristigen Aufbewahrungssicherungen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="4a353-123">Example 5: Get long term retention backups using filtering</span></span>
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

<span data-ttu-id="4a353-124">Dieser Befehl ruft alle Sicherungen mit dem Namen ab, der mit "601061b7" beginnt.</span><span class="sxs-lookup"><span data-stu-id="4a353-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="4a353-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a353-125">PARAMETERS</span></span>

### <span data-ttu-id="4a353-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="4a353-126">-BackupName</span></span>
<span data-ttu-id="4a353-127">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="4a353-127">The name of the backup.</span></span>

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

### <span data-ttu-id="4a353-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a353-128">-DatabaseName</span></span>
<span data-ttu-id="4a353-129">Der Name der Azure SQL-Datenbank, aus der die Sicherung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4a353-129">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="4a353-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="4a353-130">-DatabaseState</span></span>
<span data-ttu-id="4a353-131">Der Status der Datenbank, deren Sicherungen Sie suchen möchten, "Alive", "Deleted" oder "All".</span><span class="sxs-lookup"><span data-stu-id="4a353-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="4a353-132">Standardwerte für "Alle"</span><span class="sxs-lookup"><span data-stu-id="4a353-132">Defaults to All</span></span>

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

### <span data-ttu-id="4a353-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a353-133">-DefaultProfile</span></span>
<span data-ttu-id="4a353-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a353-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a353-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a353-135">-InputObject</span></span>
<span data-ttu-id="4a353-136">Das Datenbankobjekt, für das Sicherungen erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a353-136">The database object to get backups for.</span></span>

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

### <span data-ttu-id="4a353-137">-Location</span><span class="sxs-lookup"><span data-stu-id="4a353-137">-Location</span></span>
<span data-ttu-id="4a353-138">Der Speicherort des Quellservers der Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="4a353-138">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="4a353-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="4a353-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="4a353-140">Gibt an, ob sie nur die neueste Sicherung pro Datenbank erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="4a353-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="4a353-141">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="4a353-141">Defaults to false.</span></span>

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

### <span data-ttu-id="4a353-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a353-142">-ResourceGroupName</span></span>
<span data-ttu-id="4a353-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a353-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a353-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a353-144">-ResourceId</span></span>
<span data-ttu-id="4a353-145">Die Datenbankressourcen-ID, für die Sicherungen erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a353-145">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="4a353-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a353-146">-ServerName</span></span>
<span data-ttu-id="4a353-147">Der Name des Azure-SQL Server, unter dem die Sicherungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4a353-147">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="4a353-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a353-148">-Confirm</span></span>
<span data-ttu-id="4a353-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a353-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a353-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4a353-150">-WhatIf</span></span>
<span data-ttu-id="4a353-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a353-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a353-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a353-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a353-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a353-153">CommonParameters</span></span>
<span data-ttu-id="4a353-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a353-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a353-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a353-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a353-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a353-156">INPUTS</span></span>

### <span data-ttu-id="4a353-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4a353-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="4a353-158">System.String</span><span class="sxs-lookup"><span data-stu-id="4a353-158">System.String</span></span>

## <span data-ttu-id="4a353-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a353-159">OUTPUTS</span></span>

### <span data-ttu-id="4a353-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="4a353-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="4a353-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a353-161">NOTES</span></span>

## <span data-ttu-id="4a353-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a353-162">RELATED LINKS</span></span>

[<span data-ttu-id="4a353-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4a353-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="4a353-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a353-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="4a353-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a353-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="4a353-166">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="4a353-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)