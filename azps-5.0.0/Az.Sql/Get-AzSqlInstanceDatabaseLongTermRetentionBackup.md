---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ccd716b493640afef7b5adea0b2e834c10893c3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300105"
---
# <span data-ttu-id="497dd-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="497dd-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="497dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="497dd-102">SYNOPSIS</span></span>
<span data-ttu-id="497dd-103">Ruft die langfristige Aufbewahrungs Sicherung (en) ab.</span><span class="sxs-lookup"><span data-stu-id="497dd-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="497dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="497dd-104">SYNTAX</span></span>

### <span data-ttu-id="497dd-105">Standort (Standard)</span><span class="sxs-lookup"><span data-stu-id="497dd-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="497dd-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="497dd-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="497dd-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="497dd-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="497dd-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="497dd-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="497dd-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="497dd-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="497dd-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="497dd-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="497dd-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="497dd-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="497dd-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="497dd-112">DESCRIPTION</span></span>
<span data-ttu-id="497dd-113">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="497dd-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="497dd-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="497dd-114">EXAMPLES</span></span>

### <span data-ttu-id="497dd-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="497dd-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="497dd-116">Ruft alle langfristigen Aufbewahrungs Sicherungen für eine bestimmte Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="497dd-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="497dd-117">Die Ressourcengruppe ist optional.</span><span class="sxs-lookup"><span data-stu-id="497dd-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="497dd-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="497dd-118">PARAMETERS</span></span>

### <span data-ttu-id="497dd-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="497dd-119">-BackupName</span></span>
<span data-ttu-id="497dd-120">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="497dd-120">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="497dd-121">-DatabaseName</span></span>
<span data-ttu-id="497dd-122">Der Name der verwalteten Datenbank, unter der die Sicherungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="497dd-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="497dd-123">-DatabaseState</span></span>
<span data-ttu-id="497dd-124">Der Zustand der Datenbank, deren Sicherungen Sie suchen, lebendig, gelöscht oder alle finden möchten.</span><span class="sxs-lookup"><span data-stu-id="497dd-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="497dd-125">Standardwert für alle</span><span class="sxs-lookup"><span data-stu-id="497dd-125">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497dd-126">-DefaultProfile</span></span>
<span data-ttu-id="497dd-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="497dd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="497dd-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="497dd-128">-InputObject</span></span>
<span data-ttu-id="497dd-129">Das Datenbankobjekt, für das Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="497dd-129">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="497dd-130">-InstanceName</span></span>
<span data-ttu-id="497dd-131">Der Name der verwalteten Instanz, unter der die Sicherungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="497dd-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="497dd-132">-Location</span></span>
<span data-ttu-id="497dd-133">Der Speicherort der verwalteten Quellinstanz der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="497dd-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="497dd-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="497dd-135">Gibt an, ob nur die neueste Sicherung pro Datenbank abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="497dd-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="497dd-136">Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="497dd-136">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="497dd-137">-ResourceGroupName</span></span>
<span data-ttu-id="497dd-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="497dd-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-139">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="497dd-139">-ResourceId</span></span>
<span data-ttu-id="497dd-140">Die Datenbankressourcen-ID, für die Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="497dd-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="497dd-141">-Confirm</span></span>
<span data-ttu-id="497dd-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="497dd-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497dd-143">-WhatIf</span></span>
<span data-ttu-id="497dd-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="497dd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="497dd-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="497dd-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497dd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497dd-146">CommonParameters</span></span>
<span data-ttu-id="497dd-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="497dd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497dd-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="497dd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497dd-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="497dd-149">INPUTS</span></span>

### <span data-ttu-id="497dd-150">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="497dd-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="497dd-151">System. String</span><span class="sxs-lookup"><span data-stu-id="497dd-151">System.String</span></span>

## <span data-ttu-id="497dd-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="497dd-152">OUTPUTS</span></span>

### <span data-ttu-id="497dd-153">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="497dd-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="497dd-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="497dd-154">NOTES</span></span>

## <span data-ttu-id="497dd-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="497dd-155">RELATED LINKS</span></span>

[<span data-ttu-id="497dd-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="497dd-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="497dd-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="497dd-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="497dd-158">Satz-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="497dd-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="497dd-159">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="497dd-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)