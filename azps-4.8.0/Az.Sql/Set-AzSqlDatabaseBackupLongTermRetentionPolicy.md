---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174095"
---
# <span data-ttu-id="51c3e-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="51c3e-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="51c3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="51c3e-103">Legt eine Server-langfristige Aufbewahrungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="51c3e-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="51c3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51c3e-104">SYNTAX</span></span>

### <span data-ttu-id="51c3e-105">WeeklyRetentionRequired (Standard)</span><span class="sxs-lookup"><span data-stu-id="51c3e-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51c3e-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="51c3e-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51c3e-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="51c3e-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51c3e-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="51c3e-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51c3e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51c3e-109">DESCRIPTION</span></span>
<span data-ttu-id="51c3e-110">Das Cmdlet " **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** " legt die für diese Datenbank registrierte langfristige Aufbewahrungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="51c3e-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="51c3e-111">Bei der Richtlinie handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51c3e-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="51c3e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51c3e-112">EXAMPLES</span></span>

### <span data-ttu-id="51c3e-113">Beispiel 1: Festlegen der wöchentlichen Aufbewahrung für die aktuelle Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="51c3e-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="51c3e-114">Dadurch wird die langfristige Aufbewahrungsrichtlinie von database01 so festgelegt, dass jede wöchentliche vollständige Sicherung zwei Wochen lang gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="51c3e-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="51c3e-115">Beispiel 2: Festlegen der monatlichen Aufbewahrungsdauer für die aktuelle Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="51c3e-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="51c3e-116">Damit wird die langfristige Aufbewahrungsrichtlinie von database01 festgelegt, um die erste vollständige Sicherung eines jeden Monats für 5 Jahre zu speichern.</span><span class="sxs-lookup"><span data-stu-id="51c3e-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="51c3e-117">Beispiel 3: Festlegen der jährlichen Aufbewahrungsdauer für die aktuelle Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="51c3e-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="51c3e-118">Damit wird die langfristige Aufbewahrungsrichtlinie von database01 festgelegt, um die vollständige Sicherung zu speichern, die in der 26. Woche des Jahres für 10 Jahre durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="51c3e-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="51c3e-119">Beispiel 4: Festlegen jeder Aufbewahrung für die aktuelle Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="51c3e-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="51c3e-120">Dadurch wird die langfristige Aufbewahrungsrichtlinie von database01 so festgelegt, dass jede vollständige Sicherung für 14 Tage, die erste vollständige Sicherung eines jeden Monats für 24 Wochen, und die vollständige Sicherung, die in der 26. Woche des Jahres für 10 Jahre durchgeführt wurde, gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="51c3e-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="51c3e-121">Beispiel 5: Entfernen der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="51c3e-121">Example 5: Remove the long term retention policy</span></span>
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

<span data-ttu-id="51c3e-122">Entfernt die Richtlinie für database01, damit keine langfristigen Aufbewahrungs Sicherungen mehr gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="51c3e-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="51c3e-123">Dies wirkt sich nicht auf bereits ausgeführte Sicherungen aus.</span><span class="sxs-lookup"><span data-stu-id="51c3e-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="51c3e-124">Beispiel 6: Entfernen der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="51c3e-124">Example 6: Remove the long term retention policy</span></span>
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

<span data-ttu-id="51c3e-125">Dies ist eine weitere Möglichkeit zum Entfernen der Richtlinie für database01, damit keine langfristigen Aufbewahrungs Sicherungen mehr gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="51c3e-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="51c3e-126">Dies wirkt sich nicht auf bereits ausgeführte Sicherungen aus.</span><span class="sxs-lookup"><span data-stu-id="51c3e-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="51c3e-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="51c3e-127">PARAMETERS</span></span>

### <span data-ttu-id="51c3e-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="51c3e-128">-DatabaseName</span></span>
<span data-ttu-id="51c3e-129">Der Name der zu verwendenden Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="51c3e-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="51c3e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c3e-130">-DefaultProfile</span></span>
<span data-ttu-id="51c3e-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51c3e-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51c3e-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="51c3e-132">-MonthlyRetention</span></span>
<span data-ttu-id="51c3e-133">Die monatliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="51c3e-133">The Monthly Retention.</span></span>
<span data-ttu-id="51c3e-134">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="51c3e-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="51c3e-135">Es gibt einen Mindestbetrag von 7 Tagen und maximal 10 Jahren.</span><span class="sxs-lookup"><span data-stu-id="51c3e-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="51c3e-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="51c3e-136">-RemovePolicy</span></span>
<span data-ttu-id="51c3e-137">Falls angegeben, wird die Richtlinie für die Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="51c3e-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="51c3e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51c3e-138">-ResourceGroupName</span></span>
<span data-ttu-id="51c3e-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="51c3e-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="51c3e-140">-Servername</span><span class="sxs-lookup"><span data-stu-id="51c3e-140">-ServerName</span></span>
<span data-ttu-id="51c3e-141">Der Name des Azure SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="51c3e-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="51c3e-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="51c3e-142">-WeeklyRetention</span></span>
<span data-ttu-id="51c3e-143">Die wöchentliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="51c3e-143">The Weekly Retention.</span></span>
<span data-ttu-id="51c3e-144">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="51c3e-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="51c3e-145">Es gibt einen Mindestbetrag von 7 Tagen und maximal 10 Jahren.</span><span class="sxs-lookup"><span data-stu-id="51c3e-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="51c3e-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="51c3e-146">-WeekOfYear</span></span>
<span data-ttu-id="51c3e-147">Die Woche des Jahres, 1 bis 52, um die jährliche Aufbewahrung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="51c3e-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="51c3e-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="51c3e-148">-YearlyRetention</span></span>
<span data-ttu-id="51c3e-149">Die jährliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="51c3e-149">The Yearly Retention.</span></span>
<span data-ttu-id="51c3e-150">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="51c3e-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="51c3e-151">Es gibt einen Mindestbetrag von 7 Tagen und maximal 10 Jahren.</span><span class="sxs-lookup"><span data-stu-id="51c3e-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="51c3e-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51c3e-152">-Confirm</span></span>
<span data-ttu-id="51c3e-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51c3e-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51c3e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51c3e-154">-WhatIf</span></span>
<span data-ttu-id="51c3e-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51c3e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51c3e-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51c3e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51c3e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c3e-157">CommonParameters</span></span>
<span data-ttu-id="51c3e-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c3e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c3e-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51c3e-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c3e-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51c3e-160">INPUTS</span></span>

### <span data-ttu-id="51c3e-161">System. String</span><span class="sxs-lookup"><span data-stu-id="51c3e-161">System.String</span></span>

### <span data-ttu-id="51c3e-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="51c3e-162">System.Int32</span></span>

## <span data-ttu-id="51c3e-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51c3e-163">OUTPUTS</span></span>

### <span data-ttu-id="51c3e-164">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="51c3e-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="51c3e-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="51c3e-165">NOTES</span></span>

## <span data-ttu-id="51c3e-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51c3e-166">RELATED LINKS</span></span>

[<span data-ttu-id="51c3e-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="51c3e-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="51c3e-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="51c3e-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="51c3e-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="51c3e-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="51c3e-170">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="51c3e-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)