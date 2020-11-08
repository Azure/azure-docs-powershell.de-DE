---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995661"
---
# <span data-ttu-id="def4a-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="def4a-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="def4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="def4a-102">SYNOPSIS</span></span>
<span data-ttu-id="def4a-103">Legt eine kurzfristige Aufbewahrungsrichtlinie für Backups fest.</span><span class="sxs-lookup"><span data-stu-id="def4a-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="def4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="def4a-104">SYNTAX</span></span>

### <span data-ttu-id="def4a-105">PolicyByResourceServerDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="def4a-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def4a-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="def4a-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def4a-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="def4a-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="def4a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="def4a-108">DESCRIPTION</span></span>
<span data-ttu-id="def4a-109">Das Cmdlet " **Satz-AzSqlDatabaseBackupShortTermRetentionPolicy** " Ruft die für diese Datenbank registrierte kurzfristige Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="def4a-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="def4a-110">Die Richtlinie ist der Aufbewahrungszeitraum in Tagen für Point-in-Time-Wiederherstellungs Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="def4a-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="def4a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="def4a-111">EXAMPLES</span></span>

### <span data-ttu-id="def4a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="def4a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="def4a-113">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Database01 auf 35 Tage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="def4a-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="def4a-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="def4a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="def4a-115">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Database01 auf 35 Tage über die Rohrverlegung in einem Datenbankobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="def4a-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="def4a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="def4a-116">PARAMETERS</span></span>

### <span data-ttu-id="def4a-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="def4a-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="def4a-118">Das Datenbankobjekt, für das die Richtlinie abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="def4a-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="def4a-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="def4a-119">-DatabaseName</span></span>
<span data-ttu-id="def4a-120">Der Name der zu verwendenden Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="def4a-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="def4a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def4a-121">-DefaultProfile</span></span>
<span data-ttu-id="def4a-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="def4a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="def4a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="def4a-123">-ResourceGroupName</span></span>
<span data-ttu-id="def4a-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="def4a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="def4a-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="def4a-125">-ResourceId</span></span>
<span data-ttu-id="def4a-126">Die Ressourcen-ID für kurzfristige Aufbewahrungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="def4a-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="def4a-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="def4a-127">-RetentionDays</span></span>
<span data-ttu-id="def4a-128">Die Einstellung für die Sicherungs Aufbewahrung in Tagen.</span><span class="sxs-lookup"><span data-stu-id="def4a-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="def4a-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="def4a-129">-ServerName</span></span>
<span data-ttu-id="def4a-130">Der Name des Azure SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="def4a-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="def4a-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="def4a-131">-Confirm</span></span>
<span data-ttu-id="def4a-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="def4a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="def4a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def4a-133">-WhatIf</span></span>
<span data-ttu-id="def4a-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="def4a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def4a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="def4a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="def4a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def4a-136">CommonParameters</span></span>
<span data-ttu-id="def4a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def4a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def4a-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="def4a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def4a-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="def4a-139">INPUTS</span></span>

### <span data-ttu-id="def4a-140">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="def4a-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="def4a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="def4a-141">System.String</span></span>

## <span data-ttu-id="def4a-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="def4a-142">OUTPUTS</span></span>

### <span data-ttu-id="def4a-143">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="def4a-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="def4a-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="def4a-144">NOTES</span></span>

## <span data-ttu-id="def4a-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="def4a-145">RELATED LINKS</span></span>
