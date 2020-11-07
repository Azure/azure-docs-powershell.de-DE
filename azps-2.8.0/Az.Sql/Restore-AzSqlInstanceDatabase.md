---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: d513c186f621329510582c9cd69a64461f9e068f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825900"
---
# <span data-ttu-id="9ee32-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9ee32-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="9ee32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ee32-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee32-103">Stellt eine Azure SQL-Datenbank für verwaltete Instanzen wieder her.</span><span class="sxs-lookup"><span data-stu-id="9ee32-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="9ee32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ee32-104">SYNTAX</span></span>

### <span data-ttu-id="9ee32-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ee32-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee32-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="9ee32-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee32-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="9ee32-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ee32-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="9ee32-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee32-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="9ee32-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ee32-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="9ee32-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee32-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9ee32-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee32-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9ee32-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee32-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="9ee32-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ee32-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ee32-114">DESCRIPTION</span></span>
<span data-ttu-id="9ee32-115">Das Cmdlet **Restore-AzSqlInstanceDatabase** stellt eine Instanzen Datenbank aus einer Geo-redundanten Sicherung oder einem Zeitpunkt in einer Livedatenbank wieder her.</span><span class="sxs-lookup"><span data-stu-id="9ee32-115">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup or a point in time in a live database.</span></span>
<span data-ttu-id="9ee32-116">Die wiederhergestellte Datenbank wird als neue Instanzen Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ee32-116">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="9ee32-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ee32-117">EXAMPLES</span></span>

### <span data-ttu-id="9ee32-118">Beispiel 1: Wiederherstellen einer Instanzen Datenbank aus einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="9ee32-118">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="9ee32-119">Der Befehl stellt die Instanzdatenbank database01 aus der angegebenen Point-in-Time-Sicherung in der Instanzdatenbank mit dem Namen Database01_restored wieder her.</span><span class="sxs-lookup"><span data-stu-id="9ee32-119">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="9ee32-120">Beispiel 2: Wiederherstellen einer Instanzen Datenbank von einem Zeitpunkt zu einer anderen Instanz in einer anderen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9ee32-120">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="9ee32-121">Der Befehl stellt die Instanzdatenbank Database01 auf Instanz-managedInstance1 auf der Ressourcengruppen-ResourceGroup01 von der angegebenen Point-in-Time-Sicherung in der Instanzdatenbank mit dem Namen Database01_restored auf Instanz managedInstance2 auf der Ressourcengruppen-ResourceGroup02 wieder her.</span><span class="sxs-lookup"><span data-stu-id="9ee32-121">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="9ee32-122">Beispiel 3: Geo-Restore einer Instanzen Datenbank</span><span class="sxs-lookup"><span data-stu-id="9ee32-122">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="9ee32-123">Der erste Befehl ruft die Geo-redundante Sicherung für die Datenbank mit dem Namen database01 ab und speichert Sie dann in der $GeoBackup-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9ee32-123">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="9ee32-124">Der zweite Befehl stellt die Sicherung in $GeoBackup in der Instanzdatenbank mit dem Namen Database01_restored wieder her.</span><span class="sxs-lookup"><span data-stu-id="9ee32-124">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

## <span data-ttu-id="9ee32-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ee32-125">PARAMETERS</span></span>

### <span data-ttu-id="9ee32-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ee32-126">-AsJob</span></span>
<span data-ttu-id="9ee32-127">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9ee32-127">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee32-128">-DefaultProfile</span></span>
<span data-ttu-id="9ee32-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9ee32-129">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="9ee32-130">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="9ee32-130">-FromGeoBackup</span></span>
<span data-ttu-id="9ee32-131">Wiederherstellen aus einer Geo-Sicherung</span><span class="sxs-lookup"><span data-stu-id="9ee32-131">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-132">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="9ee32-132">-FromPointInTimeBackup</span></span>
<span data-ttu-id="9ee32-133">Wiederherstellen aus einer Point-in-Time-Sicherung</span><span class="sxs-lookup"><span data-stu-id="9ee32-133">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-134">-Geobackupobject</span><span class="sxs-lookup"><span data-stu-id="9ee32-134">-GeoBackupObject</span></span>
<span data-ttu-id="9ee32-135">Das wiederherzustellende wiederherstellbare Instanz-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="9ee32-135">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ee32-136">-InputObject</span></span>
<span data-ttu-id="9ee32-137">Das wiederherzustellende Instanzendaten Bank Objekt</span><span class="sxs-lookup"><span data-stu-id="9ee32-137">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-138">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9ee32-138">-InstanceName</span></span>
<span data-ttu-id="9ee32-139">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="9ee32-139">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-140">-Name</span><span class="sxs-lookup"><span data-stu-id="9ee32-140">-Name</span></span>
<span data-ttu-id="9ee32-141">Der Name der Instanzdatenbank, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ee32-141">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-142">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="9ee32-142">-PointInTime</span></span>
<span data-ttu-id="9ee32-143">Der Zeitpunkt, zu dem die Datenbank wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ee32-143">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee32-144">-ResourceGroupName</span></span>
<span data-ttu-id="9ee32-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ee32-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-146">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9ee32-146">-ResourceId</span></span>
<span data-ttu-id="9ee32-147">Die Ressourcen-ID des wiederherzustellenden Instanz-Datenbankobjekts</span><span class="sxs-lookup"><span data-stu-id="9ee32-147">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-148">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ee32-148">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="9ee32-149">Der Name der Ziel Instanzdatenbank, in die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ee32-149">The name of the target instance database to restore to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-150">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="9ee32-150">-TargetInstanceName</span></span>
<span data-ttu-id="9ee32-151">Der Name der Zielinstanz, in die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ee32-151">The name of the target instance to restore to.</span></span>
<span data-ttu-id="9ee32-152">Wenn Sie nicht angegeben wird, entspricht die Zielinstanz der Quellinstanz.</span><span class="sxs-lookup"><span data-stu-id="9ee32-152">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-153">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee32-153">-TargetResourceGroupName</span></span>
<span data-ttu-id="9ee32-154">Der Name der Ziel Ressourcengruppe, in der wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ee32-154">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="9ee32-155">Wenn keine Ziel Ressourcengruppe angegeben ist, entspricht Sie der Quellressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9ee32-155">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee32-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ee32-156">-Confirm</span></span>
<span data-ttu-id="9ee32-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ee32-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ee32-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ee32-158">-WhatIf</span></span>
<span data-ttu-id="9ee32-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ee32-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ee32-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ee32-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ee32-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee32-161">CommonParameters</span></span>
<span data-ttu-id="9ee32-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee32-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee32-163">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ee32-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee32-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ee32-164">INPUTS</span></span>

### <span data-ttu-id="9ee32-165">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9ee32-165">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="9ee32-166">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9ee32-166">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="9ee32-167">System. String</span><span class="sxs-lookup"><span data-stu-id="9ee32-167">System.String</span></span>

## <span data-ttu-id="9ee32-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ee32-168">OUTPUTS</span></span>

### <span data-ttu-id="9ee32-169">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9ee32-169">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="9ee32-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ee32-170">NOTES</span></span>

## <span data-ttu-id="9ee32-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ee32-171">RELATED LINKS</span></span>
