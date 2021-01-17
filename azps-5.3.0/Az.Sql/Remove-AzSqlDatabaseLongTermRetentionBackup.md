---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: be2e9342407cea6ba3da0bf239ee73e7b726dd82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374588"
---
# <span data-ttu-id="21339-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="21339-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="21339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21339-102">SYNOPSIS</span></span>
<span data-ttu-id="21339-103">Löscht eine langfristige Aufbewahrungssicherung.</span><span class="sxs-lookup"><span data-stu-id="21339-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="21339-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21339-104">SYNTAX</span></span>

### <span data-ttu-id="21339-105">RemoveBackupDefault (Standard)</span><span class="sxs-lookup"><span data-stu-id="21339-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21339-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="21339-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21339-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="21339-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21339-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21339-108">DESCRIPTION</span></span>
<span data-ttu-id="21339-109">Das **Cmdlet "Remove-AzSqlDatabaseLongTermRetentionBackup"** löscht die angegebene Sicherung.</span><span class="sxs-lookup"><span data-stu-id="21339-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="21339-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21339-110">EXAMPLES</span></span>

### <span data-ttu-id="21339-111">Beispiel 1: Löschen einer einzelnen Sicherung mit Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="21339-111">Example 1: Delete a single backup with resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000" -ResourceGrouName resourcegroup01


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

<span data-ttu-id="21339-112">Löscht die Sicherung mit dem Namen 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span><span class="sxs-lookup"><span data-stu-id="21339-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="21339-113">Beispiel 2: Löschen einer einzelnen Sicherung ohne Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="21339-113">Example 2: Delete a single backup without resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server02 -DatabaseName database02 -BackupName "55970792-164c-4a4a-88e5-7158d092d503;131656309980000000"


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

<span data-ttu-id="21339-114">Löscht die Sicherung mit dem Namen 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span><span class="sxs-lookup"><span data-stu-id="21339-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="21339-115">Beispiel 3: Löschen aller Sicherungen für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="21339-115">Example 3: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="21339-116">Mit diesem Befehl werden alle langfristigen Aufbewahrungssicherungen für den Nordeuropäischen Speicherort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="21339-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="21339-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21339-117">PARAMETERS</span></span>

### <span data-ttu-id="21339-118">-BackupName</span><span class="sxs-lookup"><span data-stu-id="21339-118">-BackupName</span></span>
<span data-ttu-id="21339-119">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="21339-119">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21339-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="21339-120">-DatabaseName</span></span>
<span data-ttu-id="21339-121">Der Name der Azure SQL-Datenbank, aus der die Sicherung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="21339-121">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21339-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21339-122">-DefaultProfile</span></span>
<span data-ttu-id="21339-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21339-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21339-124">-Force</span><span class="sxs-lookup"><span data-stu-id="21339-124">-Force</span></span>
<span data-ttu-id="21339-125">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="21339-125">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21339-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21339-126">-InputObject</span></span>
<span data-ttu-id="21339-127">Das zu entfernende Objekt "Langfristige Datenbankaufbewahrungssicherung".</span><span class="sxs-lookup"><span data-stu-id="21339-127">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21339-128">-Location</span><span class="sxs-lookup"><span data-stu-id="21339-128">-Location</span></span>
<span data-ttu-id="21339-129">Der Speicherort des Quellservers der Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="21339-129">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21339-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21339-130">-ResourceGroupName</span></span>
<span data-ttu-id="21339-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21339-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21339-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21339-132">-ResourceId</span></span>
<span data-ttu-id="21339-133">Die Ressourcen-ID der zu entfernende langfristige Datenbankaufbewahrungssicherung.</span><span class="sxs-lookup"><span data-stu-id="21339-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21339-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="21339-134">-ServerName</span></span>
<span data-ttu-id="21339-135">Der Name des Azure-SQL Server, unter dem sich die Sicherung befindet.</span><span class="sxs-lookup"><span data-stu-id="21339-135">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21339-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21339-136">-Confirm</span></span>
<span data-ttu-id="21339-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21339-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21339-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="21339-138">-WhatIf</span></span>
<span data-ttu-id="21339-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21339-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21339-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21339-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21339-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21339-141">CommonParameters</span></span>
<span data-ttu-id="21339-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21339-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21339-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21339-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21339-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21339-144">INPUTS</span></span>

### <span data-ttu-id="21339-145">System.String</span><span class="sxs-lookup"><span data-stu-id="21339-145">System.String</span></span>

## <span data-ttu-id="21339-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21339-146">OUTPUTS</span></span>

### <span data-ttu-id="21339-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="21339-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="21339-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="21339-148">NOTES</span></span>

## <span data-ttu-id="21339-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="21339-149">RELATED LINKS</span></span>

[<span data-ttu-id="21339-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="21339-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="21339-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="21339-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="21339-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="21339-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="21339-153">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="21339-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)