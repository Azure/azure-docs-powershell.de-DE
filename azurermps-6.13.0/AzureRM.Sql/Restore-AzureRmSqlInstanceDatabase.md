---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504265"
---
# <span data-ttu-id="e54bd-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e54bd-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="e54bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e54bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e54bd-103">Stellt eine Azure SQL-Datenbank für verwaltete Instanzen wieder her.</span><span class="sxs-lookup"><span data-stu-id="e54bd-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e54bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e54bd-104">SYNTAX</span></span>

### <span data-ttu-id="e54bd-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="e54bd-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e54bd-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e54bd-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e54bd-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e54bd-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e54bd-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="e54bd-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e54bd-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e54bd-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e54bd-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e54bd-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e54bd-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e54bd-111">DESCRIPTION</span></span>
<span data-ttu-id="e54bd-112">Mit dem Cmdlet **Restore-AzureRmSqlInstanceDatabase** wird eine Instanzen Datenbank ab einem bestimmten Zeitpunkt in einer Livedatenbank wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="e54bd-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="e54bd-113">Die wiederhergestellte Datenbank wird als neue Instanzen Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="e54bd-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="e54bd-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e54bd-114">EXAMPLES</span></span>

### <span data-ttu-id="e54bd-115">Beispiel 1: Wiederherstellen einer Instanzen Datenbank aus einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="e54bd-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="e54bd-116">Der Befehl stellt die Instanzdatenbank database01 aus der angegebenen Point-in-Time-Sicherung in der Instanzdatenbank mit dem Namen Database01_restored wieder her.</span><span class="sxs-lookup"><span data-stu-id="e54bd-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="e54bd-117">Beispiel 2: Wiederherstellen einer Instanzen Datenbank von einem Zeitpunkt zu einer anderen Instanz in einer anderen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e54bd-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="e54bd-118">Der Befehl stellt die Instanzdatenbank Database01 auf Instanz-managedInstance1 auf der Ressourcengruppen-ResourceGroup01 von der angegebenen Point-in-Time-Sicherung in der Instanzdatenbank mit dem Namen Database01_restored auf Instanz managedInstance2 auf der Ressourcengruppen-ResourceGroup02 wieder her.</span><span class="sxs-lookup"><span data-stu-id="e54bd-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="e54bd-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="e54bd-119">PARAMETERS</span></span>

### <span data-ttu-id="e54bd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e54bd-120">-AsJob</span></span>
<span data-ttu-id="e54bd-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e54bd-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e54bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54bd-122">-DefaultProfile</span></span>
<span data-ttu-id="e54bd-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e54bd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="e54bd-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="e54bd-125">Wiederherstellen aus einer Point-in-Time-Sicherung</span><span class="sxs-lookup"><span data-stu-id="e54bd-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e54bd-126">-InputObject</span></span>
<span data-ttu-id="e54bd-127">Das wiederherzustellende Instanzendaten Bank Objekt</span><span class="sxs-lookup"><span data-stu-id="e54bd-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e54bd-128">-InstanceName</span></span>
<span data-ttu-id="e54bd-129">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="e54bd-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e54bd-130">-Name</span></span>
<span data-ttu-id="e54bd-131">Der Name der Instanzdatenbank, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e54bd-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="e54bd-132">-PointInTime</span></span>
<span data-ttu-id="e54bd-133">Der Zeitpunkt, zu dem die Datenbank wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e54bd-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54bd-134">-ResourceGroupName</span></span>
<span data-ttu-id="e54bd-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e54bd-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e54bd-136">-ResourceId</span></span>
<span data-ttu-id="e54bd-137">Die Ressourcen-ID des wiederherzustellenden Instanz-Datenbankobjekts</span><span class="sxs-lookup"><span data-stu-id="e54bd-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-138">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e54bd-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="e54bd-139">Der Name der Ziel Instanzdatenbank, in die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e54bd-139">The name of the target instance database to restore to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-140">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="e54bd-140">-TargetInstanceName</span></span>
<span data-ttu-id="e54bd-141">Der Name der Zielinstanz, in die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e54bd-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="e54bd-142">Wenn Sie nicht angegeben wird, entspricht die Zielinstanz der Quellinstanz.</span><span class="sxs-lookup"><span data-stu-id="e54bd-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54bd-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="e54bd-144">Der Name der Ziel Ressourcengruppe, in der wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e54bd-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="e54bd-145">Wenn keine Ziel Ressourcengruppe angegeben ist, entspricht Sie der Quellressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e54bd-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54bd-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e54bd-146">-Confirm</span></span>
<span data-ttu-id="e54bd-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e54bd-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e54bd-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e54bd-148">-WhatIf</span></span>
<span data-ttu-id="e54bd-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e54bd-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e54bd-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e54bd-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e54bd-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54bd-151">CommonParameters</span></span>
<span data-ttu-id="e54bd-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e54bd-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54bd-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e54bd-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54bd-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e54bd-154">INPUTS</span></span>

### <span data-ttu-id="e54bd-155">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e54bd-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="e54bd-156">System. String</span><span class="sxs-lookup"><span data-stu-id="e54bd-156">System.String</span></span>

## <span data-ttu-id="e54bd-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e54bd-157">OUTPUTS</span></span>

### <span data-ttu-id="e54bd-158">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e54bd-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e54bd-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="e54bd-159">NOTES</span></span>

## <span data-ttu-id="e54bd-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e54bd-160">RELATED LINKS</span></span>
