---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 9726d945b4e0fada340d06e780008f1921fb6f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940875"
---
# <span data-ttu-id="e6c73-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e6c73-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="e6c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6c73-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c73-103">Legt eine langfristige Aufbewahrungsrichtlinie für den Server fest.</span><span class="sxs-lookup"><span data-stu-id="e6c73-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="e6c73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6c73-104">SYNTAX</span></span>

### <span data-ttu-id="e6c73-105">WeeklyRetentionRequired (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6c73-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6c73-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="e6c73-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c73-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="e6c73-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6c73-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="e6c73-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6c73-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6c73-109">DESCRIPTION</span></span>
<span data-ttu-id="e6c73-110">Das **Cmdlet Set-AzSqlDatabaseBackupLongTermRetentionPolicy** legt die langfristige Aufbewahrungsrichtlinie fest, die für diese Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="e6c73-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="e6c73-111">Die Richtlinie ist eine Azure Backup-Ressource, die zum Definieren der Sicherungsspeicherrichtlinie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6c73-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="e6c73-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6c73-112">EXAMPLES</span></span>

### <span data-ttu-id="e6c73-113">Beispiel 1: Festlegen der wöchentlichen Aufbewahrung für die aktuelle Version einer langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e6c73-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="e6c73-114">Dadurch wird die langfristige Aufbewahrungsrichtlinie von Datenbank01 so definiert, dass jede wöchentliche vollständige Sicherung zwei Wochen lang gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e6c73-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="e6c73-115">Beispiel 2: Festlegen der monatlichen Aufbewahrung für die aktuelle Version einer langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e6c73-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="e6c73-116">Dadurch wird die langfristige Aufbewahrungsrichtlinie der Datenbank01 so definiert, dass die erste vollständige Sicherung jedes Monats für 5 Jahre gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e6c73-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="e6c73-117">Beispiel 3: Festlegen der jährlichen Aufbewahrung für die aktuelle Version einer langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e6c73-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="e6c73-118">Dadurch wird die langfristige Aufbewahrungsrichtlinie von Datenbank01 so definiert, dass die vollständige Sicherung, die in der 26. Woche des Jahres für 10 Jahre erstellt wurde, gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e6c73-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="e6c73-119">Beispiel 4: Festlegen jeder Aufbewahrung für die aktuelle Version einer langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e6c73-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="e6c73-120">Dadurch wird die langfristige Aufbewahrungsrichtlinie von Datenbank01 so definiert, dass jede vollständige Sicherung für 14 Tage, die erste vollständige Sicherung jedes Monats für 24 Wochen und die vollständige Sicherung, die in der 26. Woche des Jahres für 10 Jahre erstellt wurde, gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e6c73-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="e6c73-121">Beispiel 5: Entfernen der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e6c73-121">Example 5: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="e6c73-122">Entfernt die Richtlinie für Datenbank01, sodass keine langfristigen Aufbewahrungssicherungen mehr gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e6c73-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="e6c73-123">Dies wirkt sich nicht auf Sicherungen aus, die bereits erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e6c73-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="e6c73-124">Beispiel 6: Entfernen der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e6c73-124">Example 6: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="e6c73-125">Dies ist eine weitere Möglichkeit zum Entfernen der Richtlinie für Datenbank01, sodass keine langfristigen Aufbewahrungssicherungen mehr gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e6c73-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="e6c73-126">Dies wirkt sich nicht auf Sicherungen aus, die bereits erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e6c73-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="e6c73-127">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e6c73-127">PARAMETERS</span></span>

### <span data-ttu-id="e6c73-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6c73-128">-DatabaseName</span></span>
<span data-ttu-id="e6c73-129">Der Name der azure SQL zu verwendende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e6c73-129">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c73-130">-DefaultProfile</span></span>
<span data-ttu-id="e6c73-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6c73-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6c73-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="e6c73-132">-MonthlyRetention</span></span>
<span data-ttu-id="e6c73-133">Die monatliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="e6c73-133">The Monthly Retention.</span></span>
<span data-ttu-id="e6c73-134">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="e6c73-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="e6c73-135">Es gibt mindestens 7 Tage und maximal 10 Jahre.</span><span class="sxs-lookup"><span data-stu-id="e6c73-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="e6c73-136">-RemovePolicy</span></span>
<span data-ttu-id="e6c73-137">Wenn angegeben, wird die Richtlinie für die Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="e6c73-137">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c73-138">-ResourceGroupName</span></span>
<span data-ttu-id="e6c73-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e6c73-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-140">-Servername</span><span class="sxs-lookup"><span data-stu-id="e6c73-140">-ServerName</span></span>
<span data-ttu-id="e6c73-141">Der Name des Azure-SQL Server in der Datenbank enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e6c73-141">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="e6c73-142">-WeeklyRetention</span></span>
<span data-ttu-id="e6c73-143">Die wöchentliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="e6c73-143">The Weekly Retention.</span></span>
<span data-ttu-id="e6c73-144">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="e6c73-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="e6c73-145">Es gibt mindestens 7 Tage und maximal 10 Jahre.</span><span class="sxs-lookup"><span data-stu-id="e6c73-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="e6c73-146">-WeekOfYear</span></span>
<span data-ttu-id="e6c73-147">Die Woche des Jahres( 1 bis 52), die sie für die jährlichen Aufbewahrungen speichern soll.</span><span class="sxs-lookup"><span data-stu-id="e6c73-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="e6c73-148">-YearlyRetention</span></span>
<span data-ttu-id="e6c73-149">Die jährlichen Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="e6c73-149">The Yearly Retention.</span></span>
<span data-ttu-id="e6c73-150">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="e6c73-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="e6c73-151">Es gibt mindestens 7 Tage und maximal 10 Jahre.</span><span class="sxs-lookup"><span data-stu-id="e6c73-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6c73-152">-Confirm</span></span>
<span data-ttu-id="e6c73-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6c73-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6c73-154">-WhatIf</span></span>
<span data-ttu-id="e6c73-155">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6c73-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6c73-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6c73-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c73-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c73-157">CommonParameters</span></span>
<span data-ttu-id="e6c73-158">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c73-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c73-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6c73-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c73-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6c73-160">INPUTS</span></span>

### <span data-ttu-id="e6c73-161">System.String</span><span class="sxs-lookup"><span data-stu-id="e6c73-161">System.String</span></span>

### <span data-ttu-id="e6c73-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e6c73-162">System.Int32</span></span>

## <span data-ttu-id="e6c73-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6c73-163">OUTPUTS</span></span>

### <span data-ttu-id="e6c73-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e6c73-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="e6c73-165">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e6c73-165">NOTES</span></span>

## <span data-ttu-id="e6c73-166">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e6c73-166">RELATED LINKS</span></span>

[<span data-ttu-id="e6c73-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e6c73-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="e6c73-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e6c73-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e6c73-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e6c73-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e6c73-170">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="e6c73-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)