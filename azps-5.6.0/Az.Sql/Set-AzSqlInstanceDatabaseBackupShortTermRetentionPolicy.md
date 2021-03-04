---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 0a08176dab2d4bb40d25f11574850d584981063c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933387"
---
# <span data-ttu-id="73c4e-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73c4e-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="73c4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="73c4e-103">Legt eine kurzfristige Sicherungsaufbewahrungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="73c4e-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="73c4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73c4e-104">SYNTAX</span></span>

### <span data-ttu-id="73c4e-105">PolicyByResourceInstanceDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="73c4e-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c4e-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="73c4e-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c4e-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="73c4e-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73c4e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73c4e-108">DESCRIPTION</span></span>
<span data-ttu-id="73c4e-109">Das **Cmdlet Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** ruft die kurzfristige Aufbewahrungsrichtlinie ab, die für diese Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="73c4e-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="73c4e-110">Die Richtlinie ist der Aufbewahrungszeitraum in Tagen für Punkt-in-Zeit-Wiederherstellungssicherungen.</span><span class="sxs-lookup"><span data-stu-id="73c4e-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="73c4e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73c4e-111">EXAMPLES</span></span>

### <span data-ttu-id="73c4e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73c4e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="73c4e-113">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 auf 35 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="73c4e-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="73c4e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="73c4e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="73c4e-115">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 auf 35 Tage über Piping in einem Datenbankobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="73c4e-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="73c4e-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="73c4e-116">Example 3</span></span>
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

<span data-ttu-id="73c4e-117">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für alle gelöschten Datenbanken namens DB1 über Piping in einem gelöschten Datenbankobjekt definiert.</span><span class="sxs-lookup"><span data-stu-id="73c4e-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="73c4e-118">Beachten Sie, dass Sie den Aufbewahrungszeitraum für gelöschte Datenbanken nur verringern können.</span><span class="sxs-lookup"><span data-stu-id="73c4e-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="73c4e-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="73c4e-119">PARAMETERS</span></span>

### <span data-ttu-id="73c4e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="73c4e-120">-DatabaseName</span></span>
<span data-ttu-id="73c4e-121">Der Name der Azure SQL-Instanzdatenbank, für die Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="73c4e-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="73c4e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c4e-122">-DefaultProfile</span></span>
<span data-ttu-id="73c4e-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73c4e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73c4e-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="73c4e-124">-DeletionDate</span></span>
<span data-ttu-id="73c4e-125">Das Löschdatum der Azure SQL-Instanzdatenbank zum Abrufen von Sicherungen mit Millisekundengenauigkeit (z. B. 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="73c4e-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="73c4e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73c4e-126">-InputObject</span></span>
<span data-ttu-id="73c4e-127">Das Live- oder gelöschte Datenbankobjekt, für das sie die Richtlinie erhalten/festlegen soll.</span><span class="sxs-lookup"><span data-stu-id="73c4e-127">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="73c4e-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="73c4e-128">-InstanceName</span></span>
<span data-ttu-id="73c4e-129">Der Name der azure SQL verwaltete Instanz, in der sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="73c4e-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="73c4e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c4e-130">-ResourceGroupName</span></span>
<span data-ttu-id="73c4e-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="73c4e-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="73c4e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73c4e-132">-ResourceId</span></span>
<span data-ttu-id="73c4e-133">Die ressourcen-ID für die kurzfristige Aufbewahrungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="73c4e-133">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="73c4e-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="73c4e-134">-RetentionDays</span></span>
<span data-ttu-id="73c4e-135">Tage der Sicherungsaufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="73c4e-135">Days of backup retention.</span></span>

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

### <span data-ttu-id="73c4e-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73c4e-136">-Confirm</span></span>
<span data-ttu-id="73c4e-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73c4e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c4e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c4e-138">-WhatIf</span></span>
<span data-ttu-id="73c4e-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73c4e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c4e-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73c4e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c4e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c4e-141">CommonParameters</span></span>
<span data-ttu-id="73c4e-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c4e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c4e-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73c4e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c4e-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73c4e-144">INPUTS</span></span>

### <span data-ttu-id="73c4e-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="73c4e-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="73c4e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="73c4e-146">System.String</span></span>

## <span data-ttu-id="73c4e-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73c4e-147">OUTPUTS</span></span>

### <span data-ttu-id="73c4e-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="73c4e-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="73c4e-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="73c4e-149">NOTES</span></span>

## <span data-ttu-id="73c4e-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="73c4e-150">RELATED LINKS</span></span>
