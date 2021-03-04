---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: ccdcf55b61b57b54848f3310d7366bb76e0f6805
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940848"
---
# <span data-ttu-id="9ce16-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9ce16-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="9ce16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ce16-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce16-103">Legt eine kurzfristige Sicherungsaufbewahrungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="9ce16-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="9ce16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ce16-104">SYNTAX</span></span>

### <span data-ttu-id="9ce16-105">PolicyByResourceServerDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ce16-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ce16-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ce16-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ce16-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9ce16-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ce16-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ce16-108">DESCRIPTION</span></span>
<span data-ttu-id="9ce16-109">Das **Cmdlet Set-AzSqlDatabaseBackupShortTermRetentionPolicy** ruft die kurzfristige Aufbewahrungsrichtlinie ab, die für diese Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9ce16-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="9ce16-110">Die Richtlinie ist der Aufbewahrungszeitraum in Tagen für Punkt-in-Zeit-Wiederherstellungssicherungen.</span><span class="sxs-lookup"><span data-stu-id="9ce16-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="9ce16-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ce16-111">EXAMPLES</span></span>

### <span data-ttu-id="9ce16-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ce16-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="9ce16-113">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 auf 35 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="9ce16-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="9ce16-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9ce16-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="9ce16-115">Mit diesem Befehl wird die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 auf 35 Tage über Piping in einem Datenbankobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="9ce16-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="9ce16-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9ce16-116">PARAMETERS</span></span>

### <span data-ttu-id="9ce16-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9ce16-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="9ce16-118">Das Datenbankobjekt, für das die Richtlinie angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ce16-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="9ce16-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ce16-119">-DatabaseName</span></span>
<span data-ttu-id="9ce16-120">Der Name der azure SQL zu verwendende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9ce16-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="9ce16-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce16-121">-DefaultProfile</span></span>
<span data-ttu-id="9ce16-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ce16-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ce16-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ce16-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ce16-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ce16-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9ce16-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ce16-125">-ResourceId</span></span>
<span data-ttu-id="9ce16-126">Die ressourcen-ID für die kurzfristige Aufbewahrungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="9ce16-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="9ce16-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="9ce16-127">-RetentionDays</span></span>
<span data-ttu-id="9ce16-128">Die Einstellung für die Sicherungsaufbewahrung in Tagen.</span><span class="sxs-lookup"><span data-stu-id="9ce16-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="9ce16-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="9ce16-129">-ServerName</span></span>
<span data-ttu-id="9ce16-130">Der Name des Azure-SQL Server in der Datenbank enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9ce16-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="9ce16-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ce16-131">-Confirm</span></span>
<span data-ttu-id="9ce16-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ce16-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ce16-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ce16-133">-WhatIf</span></span>
<span data-ttu-id="9ce16-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ce16-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ce16-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ce16-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ce16-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce16-136">CommonParameters</span></span>
<span data-ttu-id="9ce16-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce16-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce16-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ce16-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce16-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ce16-139">INPUTS</span></span>

### <span data-ttu-id="9ce16-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9ce16-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="9ce16-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9ce16-141">System.String</span></span>

## <span data-ttu-id="9ce16-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ce16-142">OUTPUTS</span></span>

### <span data-ttu-id="9ce16-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9ce16-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="9ce16-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9ce16-144">NOTES</span></span>

## <span data-ttu-id="9ce16-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9ce16-145">RELATED LINKS</span></span>
