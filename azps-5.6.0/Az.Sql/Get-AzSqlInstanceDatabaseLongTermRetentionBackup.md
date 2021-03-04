---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 464334aa67be554a20c7d1b15e7d591a25979809
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929760"
---
# <span data-ttu-id="d87fa-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d87fa-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="d87fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d87fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d87fa-103">Ruft langfristige Aufbewahrungssicherungen ab.</span><span class="sxs-lookup"><span data-stu-id="d87fa-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="d87fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d87fa-104">SYNTAX</span></span>

### <span data-ttu-id="d87fa-105">Speicherort (Standard)</span><span class="sxs-lookup"><span data-stu-id="d87fa-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87fa-106">Instanzname</span><span class="sxs-lookup"><span data-stu-id="d87fa-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87fa-107">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="d87fa-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87fa-108">Sicherungsname</span><span class="sxs-lookup"><span data-stu-id="d87fa-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87fa-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="d87fa-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87fa-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="d87fa-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87fa-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="d87fa-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d87fa-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d87fa-112">DESCRIPTION</span></span>
<span data-ttu-id="d87fa-113">{{ Ausfüllen der Beschreibung }}</span><span class="sxs-lookup"><span data-stu-id="d87fa-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="d87fa-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d87fa-114">EXAMPLES</span></span>

### <span data-ttu-id="d87fa-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d87fa-115">Example 1</span></span>
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

<span data-ttu-id="d87fa-116">Ruft alle langfristigen Aufbewahrungssicherungen für eine bestimmte Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="d87fa-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="d87fa-117">Ressourcengruppe ist optional.</span><span class="sxs-lookup"><span data-stu-id="d87fa-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="d87fa-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d87fa-118">PARAMETERS</span></span>

### <span data-ttu-id="d87fa-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="d87fa-119">-BackupName</span></span>
<span data-ttu-id="d87fa-120">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="d87fa-120">The name of the backup.</span></span>

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

### <span data-ttu-id="d87fa-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d87fa-121">-DatabaseName</span></span>
<span data-ttu-id="d87fa-122">Der Name der verwalteten Datenbank, unter der sich die Sicherungen befinden.</span><span class="sxs-lookup"><span data-stu-id="d87fa-122">The name of the Managed Database the backups are under.</span></span>

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

### <span data-ttu-id="d87fa-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="d87fa-123">-DatabaseState</span></span>
<span data-ttu-id="d87fa-124">Der Zustand der Datenbank, deren Sicherungen Sie suchen möchten, Alive, Deleted oder All.</span><span class="sxs-lookup"><span data-stu-id="d87fa-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="d87fa-125">Standardwerte für "Alle"</span><span class="sxs-lookup"><span data-stu-id="d87fa-125">Defaults to All</span></span>

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

### <span data-ttu-id="d87fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87fa-126">-DefaultProfile</span></span>
<span data-ttu-id="d87fa-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d87fa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d87fa-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d87fa-128">-InputObject</span></span>
<span data-ttu-id="d87fa-129">Das Datenbankobjekt, für das Sicherungen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d87fa-129">The database object to get backups for.</span></span>

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

### <span data-ttu-id="d87fa-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d87fa-130">-InstanceName</span></span>
<span data-ttu-id="d87fa-131">Der Name der verwalteten Instanz, unter der sich die Sicherungen befinden.</span><span class="sxs-lookup"><span data-stu-id="d87fa-131">The name of the Managed Instance the backups are under.</span></span>

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

### <span data-ttu-id="d87fa-132">-Location</span><span class="sxs-lookup"><span data-stu-id="d87fa-132">-Location</span></span>
<span data-ttu-id="d87fa-133">Der Speicherort der verwalteten Quellinstanz der Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="d87fa-133">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="d87fa-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="d87fa-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="d87fa-135">Ob sie nur die neueste Sicherung pro Datenbank erhalten möchten oder nicht.</span><span class="sxs-lookup"><span data-stu-id="d87fa-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="d87fa-136">Standardmäßig ist "false" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d87fa-136">Defaults to false.</span></span>

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

### <span data-ttu-id="d87fa-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d87fa-137">-ResourceGroupName</span></span>
<span data-ttu-id="d87fa-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d87fa-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="d87fa-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d87fa-139">-ResourceId</span></span>
<span data-ttu-id="d87fa-140">Die Datenbankressourcen-ID zum Erhalten von Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="d87fa-140">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="d87fa-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d87fa-141">-Confirm</span></span>
<span data-ttu-id="d87fa-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d87fa-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d87fa-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d87fa-143">-WhatIf</span></span>
<span data-ttu-id="d87fa-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d87fa-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d87fa-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d87fa-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d87fa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87fa-146">CommonParameters</span></span>
<span data-ttu-id="d87fa-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d87fa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87fa-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d87fa-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87fa-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d87fa-149">INPUTS</span></span>

### <span data-ttu-id="d87fa-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d87fa-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="d87fa-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d87fa-151">System.String</span></span>

## <span data-ttu-id="d87fa-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d87fa-152">OUTPUTS</span></span>

### <span data-ttu-id="d87fa-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="d87fa-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="d87fa-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d87fa-154">NOTES</span></span>

## <span data-ttu-id="d87fa-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d87fa-155">RELATED LINKS</span></span>

[<span data-ttu-id="d87fa-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d87fa-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d87fa-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d87fa-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d87fa-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d87fa-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d87fa-159">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="d87fa-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)