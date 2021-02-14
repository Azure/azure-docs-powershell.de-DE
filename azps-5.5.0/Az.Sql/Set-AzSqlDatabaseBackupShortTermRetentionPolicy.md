---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163212"
---
# <span data-ttu-id="26c2e-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="26c2e-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="26c2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="26c2e-103">Legt eine richtlinie für die kurzfristige Sicherung fest.</span><span class="sxs-lookup"><span data-stu-id="26c2e-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="26c2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26c2e-104">SYNTAX</span></span>

### <span data-ttu-id="26c2e-105">PolicyByResourceServerDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="26c2e-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c2e-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="26c2e-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c2e-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="26c2e-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c2e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26c2e-108">DESCRIPTION</span></span>
<span data-ttu-id="26c2e-109">Das **Cmdlet "Set-AzSqlDatabaseBackupShortTermRetentionPolicy"** ruft die kurzfristige Aufbewahrungsrichtlinie ab, die in dieser Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="26c2e-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="26c2e-110">Die Richtlinie ist der Aufbewahrungszeitraum (in Tagen) für Point-in-Time-Wiederherstellungssicherungen.</span><span class="sxs-lookup"><span data-stu-id="26c2e-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="26c2e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26c2e-111">EXAMPLES</span></span>

### <span data-ttu-id="26c2e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="26c2e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="26c2e-113">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 auf 35 Tage definiert.</span><span class="sxs-lookup"><span data-stu-id="26c2e-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="26c2e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="26c2e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="26c2e-115">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 über die Piping in einem Datenbankobjekt auf 35 Tage definiert.</span><span class="sxs-lookup"><span data-stu-id="26c2e-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="26c2e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26c2e-116">PARAMETERS</span></span>

### <span data-ttu-id="26c2e-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="26c2e-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="26c2e-118">Das Datenbankobjekt, für das die Richtlinie erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="26c2e-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26c2e-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26c2e-119">-DatabaseName</span></span>
<span data-ttu-id="26c2e-120">Der Name der Azure SQL Zu verwendende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="26c2e-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26c2e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c2e-121">-DefaultProfile</span></span>
<span data-ttu-id="26c2e-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26c2e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26c2e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c2e-123">-ResourceGroupName</span></span>
<span data-ttu-id="26c2e-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="26c2e-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26c2e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26c2e-125">-ResourceId</span></span>
<span data-ttu-id="26c2e-126">Die ressourcen-ID der kurzfristigen Aufbewahrungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="26c2e-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26c2e-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="26c2e-127">-RetentionDays</span></span>
<span data-ttu-id="26c2e-128">Die Einstellung für die Sicherungsaufbewahrung in Tagen.</span><span class="sxs-lookup"><span data-stu-id="26c2e-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="26c2e-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="26c2e-129">-ServerName</span></span>
<span data-ttu-id="26c2e-130">Der Name des Azure-SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="26c2e-130">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26c2e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26c2e-131">-Confirm</span></span>
<span data-ttu-id="26c2e-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26c2e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26c2e-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="26c2e-133">-WhatIf</span></span>
<span data-ttu-id="26c2e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26c2e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26c2e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26c2e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26c2e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c2e-136">CommonParameters</span></span>
<span data-ttu-id="26c2e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26c2e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c2e-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26c2e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c2e-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26c2e-139">INPUTS</span></span>

### <span data-ttu-id="26c2e-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="26c2e-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="26c2e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="26c2e-141">System.String</span></span>

## <span data-ttu-id="26c2e-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26c2e-142">OUTPUTS</span></span>

### <span data-ttu-id="26c2e-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="26c2e-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="26c2e-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="26c2e-144">NOTES</span></span>

## <span data-ttu-id="26c2e-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="26c2e-145">RELATED LINKS</span></span>
