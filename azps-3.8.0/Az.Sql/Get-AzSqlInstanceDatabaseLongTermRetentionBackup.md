---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 9408e51cfcdab3cd2c82617ee7f8cb9bc7d3918a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004482"
---
# <span data-ttu-id="c2c46-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c2c46-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="c2c46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2c46-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c46-103">Ruft die langfristige Aufbewahrungs Sicherung (en) ab.</span><span class="sxs-lookup"><span data-stu-id="c2c46-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="c2c46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2c46-104">SYNTAX</span></span>

### <span data-ttu-id="c2c46-105">Standort (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2c46-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c46-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2c46-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c46-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2c46-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c46-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="c2c46-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c46-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2c46-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c46-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2c46-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c46-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2c46-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2c46-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2c46-112">DESCRIPTION</span></span>
<span data-ttu-id="c2c46-113">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="c2c46-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="c2c46-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2c46-114">EXAMPLES</span></span>

### <span data-ttu-id="c2c46-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2c46-115">Example 1</span></span>
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

<span data-ttu-id="c2c46-116">Ruft alle langfristigen Aufbewahrungs Sicherungen für eine bestimmte Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="c2c46-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="c2c46-117">Die Ressourcengruppe ist optional.</span><span class="sxs-lookup"><span data-stu-id="c2c46-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="c2c46-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2c46-118">PARAMETERS</span></span>

### <span data-ttu-id="c2c46-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="c2c46-119">-BackupName</span></span>
<span data-ttu-id="c2c46-120">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="c2c46-120">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2c46-121">-DatabaseName</span></span>
<span data-ttu-id="c2c46-122">Der Name der verwalteten Datenbank, unter der die Sicherungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c2c46-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="c2c46-123">-DatabaseState</span></span>
<span data-ttu-id="c2c46-124">Der Zustand der Datenbank, deren Sicherungen Sie suchen, lebendig, gelöscht oder alle finden möchten.</span><span class="sxs-lookup"><span data-stu-id="c2c46-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="c2c46-125">Standardwert für alle</span><span class="sxs-lookup"><span data-stu-id="c2c46-125">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c46-126">-DefaultProfile</span></span>
<span data-ttu-id="c2c46-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2c46-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2c46-128">-InputObject</span></span>
<span data-ttu-id="c2c46-129">Das Datenbankobjekt, für das Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c2c46-129">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2c46-130">-InstanceName</span></span>
<span data-ttu-id="c2c46-131">Der Name der verwalteten Instanz, unter der die Sicherungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c2c46-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="c2c46-132">-Location</span></span>
<span data-ttu-id="c2c46-133">Der Speicherort der verwalteten Quellinstanz der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="c2c46-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="c2c46-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="c2c46-135">Gibt an, ob nur die neueste Sicherung pro Datenbank abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2c46-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="c2c46-136">Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="c2c46-136">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c46-137">-ResourceGroupName</span></span>
<span data-ttu-id="c2c46-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2c46-138">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-139">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c2c46-139">-ResourceId</span></span>
<span data-ttu-id="c2c46-140">Die Datenbankressourcen-ID, für die Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c2c46-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2c46-141">-Confirm</span></span>
<span data-ttu-id="c2c46-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2c46-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c46-143">-WhatIf</span></span>
<span data-ttu-id="c2c46-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2c46-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2c46-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2c46-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c46-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c46-146">CommonParameters</span></span>
<span data-ttu-id="c2c46-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c46-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c46-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2c46-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c46-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2c46-149">INPUTS</span></span>

### <span data-ttu-id="c2c46-150">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c2c46-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="c2c46-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c2c46-151">System.String</span></span>

## <span data-ttu-id="c2c46-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2c46-152">OUTPUTS</span></span>

### <span data-ttu-id="c2c46-153">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="c2c46-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="c2c46-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2c46-154">NOTES</span></span>

## <span data-ttu-id="c2c46-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2c46-155">RELATED LINKS</span></span>

[<span data-ttu-id="c2c46-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c2c46-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c2c46-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2c46-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c2c46-158">Satz-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2c46-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c2c46-159">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c2c46-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)