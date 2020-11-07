---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 6ec4e3163d1bcd388ef0b4b8813ece89a41bfd23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825839"
---
# <span data-ttu-id="a6847-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6847-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="a6847-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6847-102">SYNOPSIS</span></span>
<span data-ttu-id="a6847-103">Legt eine kurzfristige Aufbewahrungsrichtlinie für Backups fest.</span><span class="sxs-lookup"><span data-stu-id="a6847-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="a6847-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6847-104">SYNTAX</span></span>

### <span data-ttu-id="a6847-105">PolicyByResourceInstanceDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6847-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6847-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a6847-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6847-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a6847-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6847-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6847-108">DESCRIPTION</span></span>
<span data-ttu-id="a6847-109">Das Cmdlet " **Satz-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** " Ruft die für diese Datenbank registrierte kurzfristige Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="a6847-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="a6847-110">Die Richtlinie ist der Aufbewahrungszeitraum in Tagen für Point-in-Time-Wiederherstellungs Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="a6847-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="a6847-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6847-111">EXAMPLES</span></span>

### <span data-ttu-id="a6847-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6847-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="a6847-113">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Database01 auf 35 Tage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a6847-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="a6847-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a6847-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="a6847-115">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Database01 auf 35 Tage über die Rohrverlegung in einem Datenbankobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a6847-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="a6847-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a6847-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="a6847-117">Dieser Befehl legt die kurzfristige Aufbewahrungsrichtlinie für alle gelöschten Datenbanken mit dem Namen "degressiv" über die Rohrverlegung in einem gelöschten Datenbankobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="a6847-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="a6847-118">Hinweis Sie können den Aufbewahrungszeitraum für gelöschte Datenbanken nur reduzieren.</span><span class="sxs-lookup"><span data-stu-id="a6847-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="a6847-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6847-119">PARAMETERS</span></span>

### <span data-ttu-id="a6847-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a6847-120">-DatabaseName</span></span>
<span data-ttu-id="a6847-121">Der Name der Azure SQL-Instanzen Datenbank, für die Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a6847-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6847-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6847-122">-DefaultProfile</span></span>
<span data-ttu-id="a6847-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6847-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6847-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="a6847-124">-DeletionDate</span></span>
<span data-ttu-id="a6847-125">Das Löschdatum der Azure SQL-Instanzen Datenbank zum Abrufen von Sicherungen für, mit Millisekunden-Genauigkeit (z. b. 2016-02-23T00:21:22.847 z)</span><span class="sxs-lookup"><span data-stu-id="a6847-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6847-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a6847-126">-InputObject</span></span>
<span data-ttu-id="a6847-127">Das Live-oder gelöschte Datenbankobjekt, für das die Richtlinie abgerufen/gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6847-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6847-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a6847-128">-InstanceName</span></span>
<span data-ttu-id="a6847-129">Der Name der verwalteten Azure SQL-Instanz, in der sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="a6847-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6847-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6847-130">-ResourceGroupName</span></span>
<span data-ttu-id="a6847-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a6847-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6847-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a6847-132">-ResourceId</span></span>
<span data-ttu-id="a6847-133">Die Ressourcen-ID für kurzfristige Aufbewahrungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="a6847-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6847-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="a6847-134">-RetentionDays</span></span>
<span data-ttu-id="a6847-135">Tage der Backup-Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="a6847-135">Days of backup retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6847-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6847-136">-Confirm</span></span>
<span data-ttu-id="a6847-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6847-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6847-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6847-138">-WhatIf</span></span>
<span data-ttu-id="a6847-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6847-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6847-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6847-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6847-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6847-141">CommonParameters</span></span>
<span data-ttu-id="a6847-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6847-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6847-143">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6847-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6847-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6847-144">INPUTS</span></span>

### <span data-ttu-id="a6847-145">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="a6847-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="a6847-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a6847-146">System.String</span></span>

## <span data-ttu-id="a6847-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6847-147">OUTPUTS</span></span>

### <span data-ttu-id="a6847-148">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a6847-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="a6847-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6847-149">NOTES</span></span>

## <span data-ttu-id="a6847-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6847-150">RELATED LINKS</span></span>
