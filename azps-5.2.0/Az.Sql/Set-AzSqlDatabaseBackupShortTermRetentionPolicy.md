---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296357"
---
# <span data-ttu-id="8edfb-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8edfb-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="8edfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8edfb-102">SYNOPSIS</span></span>
<span data-ttu-id="8edfb-103">Legt eine richtlinie für die kurzfristige Sicherung fest.</span><span class="sxs-lookup"><span data-stu-id="8edfb-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="8edfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8edfb-104">SYNTAX</span></span>

### <span data-ttu-id="8edfb-105">PolicyByResourceServerDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8edfb-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8edfb-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8edfb-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8edfb-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8edfb-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8edfb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8edfb-108">DESCRIPTION</span></span>
<span data-ttu-id="8edfb-109">Das **Cmdlet "Set-AzSqlDatabaseBackupShortTermRetentionPolicy"** ruft die kurzfristige Aufbewahrungsrichtlinie ab, die in dieser Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="8edfb-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="8edfb-110">Die Richtlinie ist der Aufbewahrungszeitraum (in Tagen) für Point-in-Time-Wiederherstellungssicherungen.</span><span class="sxs-lookup"><span data-stu-id="8edfb-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="8edfb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8edfb-111">EXAMPLES</span></span>

### <span data-ttu-id="8edfb-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8edfb-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="8edfb-113">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 auf 35 Tage definiert.</span><span class="sxs-lookup"><span data-stu-id="8edfb-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="8edfb-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8edfb-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="8edfb-115">Mit diesem Befehl wird die Richtlinie für die kurzfristige Aufbewahrung von Datenbank01 über die Piping in einem Datenbankobjekt auf 35 Tage definiert.</span><span class="sxs-lookup"><span data-stu-id="8edfb-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="8edfb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8edfb-116">PARAMETERS</span></span>

### <span data-ttu-id="8edfb-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8edfb-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="8edfb-118">Das Datenbankobjekt, für das die Richtlinie erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8edfb-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="8edfb-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8edfb-119">-DatabaseName</span></span>
<span data-ttu-id="8edfb-120">Der Name der Azure SQL Zu verwendende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8edfb-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="8edfb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8edfb-121">-DefaultProfile</span></span>
<span data-ttu-id="8edfb-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8edfb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8edfb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8edfb-123">-ResourceGroupName</span></span>
<span data-ttu-id="8edfb-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8edfb-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="8edfb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8edfb-125">-ResourceId</span></span>
<span data-ttu-id="8edfb-126">Die ressourcen-ID der kurzfristigen Aufbewahrungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8edfb-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="8edfb-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="8edfb-127">-RetentionDays</span></span>
<span data-ttu-id="8edfb-128">Die Einstellung für die Sicherungsaufbewahrung in Tagen.</span><span class="sxs-lookup"><span data-stu-id="8edfb-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="8edfb-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8edfb-129">-ServerName</span></span>
<span data-ttu-id="8edfb-130">Der Name des Azure-SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="8edfb-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="8edfb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8edfb-131">-Confirm</span></span>
<span data-ttu-id="8edfb-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8edfb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8edfb-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8edfb-133">-WhatIf</span></span>
<span data-ttu-id="8edfb-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8edfb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8edfb-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8edfb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8edfb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8edfb-136">CommonParameters</span></span>
<span data-ttu-id="8edfb-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8edfb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8edfb-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8edfb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8edfb-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8edfb-139">INPUTS</span></span>

### <span data-ttu-id="8edfb-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8edfb-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="8edfb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8edfb-141">System.String</span></span>

## <span data-ttu-id="8edfb-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8edfb-142">OUTPUTS</span></span>

### <span data-ttu-id="8edfb-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8edfb-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="8edfb-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8edfb-144">NOTES</span></span>

## <span data-ttu-id="8edfb-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8edfb-145">RELATED LINKS</span></span>
