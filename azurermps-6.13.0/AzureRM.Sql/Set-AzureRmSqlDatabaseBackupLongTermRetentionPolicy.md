---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a9389999bdbd93b332a3186ede1003c896552d1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479433"
---
# <span data-ttu-id="56e17-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="56e17-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="56e17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56e17-102">SYNOPSIS</span></span>
<span data-ttu-id="56e17-103">Legt eine Server-langfristige Aufbewahrungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="56e17-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56e17-104">SYNTAX</span></span>

### <span data-ttu-id="56e17-105">WeeklyRetentionRequired (Standard)</span><span class="sxs-lookup"><span data-stu-id="56e17-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e17-106">Legacy</span><span class="sxs-lookup"><span data-stu-id="56e17-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e17-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="56e17-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e17-108">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="56e17-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e17-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="56e17-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56e17-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56e17-110">DESCRIPTION</span></span>
<span data-ttu-id="56e17-111">Das Cmdlet " **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** " legt die für diese Datenbank registrierte langfristige Aufbewahrungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="56e17-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="56e17-112">Bei der Richtlinie handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56e17-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="56e17-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56e17-113">EXAMPLES</span></span>

### <span data-ttu-id="56e17-114">Beispiel 1: Festlegen der wöchentlichen Aufbewahrung für die aktuelle Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="56e17-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="56e17-115">Dadurch wird die langfristige Aufbewahrungsrichtlinie von database01 so festgelegt, dass jede wöchentliche vollständige Sicherung zwei Wochen lang gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="56e17-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="56e17-116">Beispiel 2: Festlegen der monatlichen Aufbewahrungsdauer für die aktuelle Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="56e17-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="56e17-117">Damit wird die langfristige Aufbewahrungsrichtlinie von database01 festgelegt, um die erste vollständige Sicherung eines jeden Monats für 5 Jahre zu speichern.</span><span class="sxs-lookup"><span data-stu-id="56e17-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="56e17-118">Beispiel 3: Festlegen der jährlichen Aufbewahrungsdauer für die aktuelle Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="56e17-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="56e17-119">Damit wird die langfristige Aufbewahrungsrichtlinie von database01 festgelegt, um die vollständige Sicherung zu speichern, die in der 26. Woche des Jahres für 10 Jahre durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="56e17-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="56e17-120">Beispiel 4: Festlegen jeder Aufbewahrung für die aktuelle Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="56e17-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="56e17-121">Dadurch wird die langfristige Aufbewahrungsrichtlinie von database01 so festgelegt, dass jede vollständige Sicherung für 14 Tage, die erste vollständige Sicherung eines jeden Monats für 24 Wochen, und die vollständige Sicherung, die in der 26. Woche des Jahres für 10 Jahre durchgeführt wurde, gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="56e17-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="56e17-122">Beispiel 4: Entfernen der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="56e17-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="56e17-123">Entfernt die Richtlinie für database01, damit keine langfristigen Aufbewahrungs Sicherungen mehr gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="56e17-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="56e17-124">Dies wirkt sich nicht auf bereits ausgeführte Sicherungen aus.</span><span class="sxs-lookup"><span data-stu-id="56e17-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="56e17-125">Beispiel 4: Entfernen der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="56e17-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="56e17-126">Dies ist eine weitere Möglichkeit zum Entfernen der Richtlinie für database01, damit keine langfristigen Aufbewahrungs Sicherungen mehr gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="56e17-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="56e17-127">Dies wirkt sich nicht auf bereits ausgeführte Sicherungen aus.</span><span class="sxs-lookup"><span data-stu-id="56e17-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="56e17-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e17-128">PARAMETERS</span></span>

### <span data-ttu-id="56e17-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56e17-129">-DatabaseName</span></span>
<span data-ttu-id="56e17-130">Der Name der zu verwendenden Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="56e17-130">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="56e17-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e17-131">-DefaultProfile</span></span>
<span data-ttu-id="56e17-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56e17-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e17-133">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="56e17-133">-MonthlyRetention</span></span>
<span data-ttu-id="56e17-134">Die monatliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="56e17-134">The Monthly Retention.</span></span>
<span data-ttu-id="56e17-135">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="56e17-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="56e17-136">Es gibt eine Minimum von 7 Tagen und maximal 10 Jahren.</span><span class="sxs-lookup"><span data-stu-id="56e17-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="56e17-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="56e17-137">-RemovePolicy</span></span>
<span data-ttu-id="56e17-138">Falls angegeben, wird die Richtlinie für die Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="56e17-138">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="56e17-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e17-139">-ResourceGroupName</span></span>
<span data-ttu-id="56e17-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56e17-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="56e17-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="56e17-141">-ResourceId</span></span>
<span data-ttu-id="56e17-142">Die Ressourcen-ID der Sicherungsrichtlinie für langfristige Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="56e17-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56e17-143">-Servername</span><span class="sxs-lookup"><span data-stu-id="56e17-143">-ServerName</span></span>
<span data-ttu-id="56e17-144">Der Name des Azure SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="56e17-144">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="56e17-145">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="56e17-145">-State</span></span>
<span data-ttu-id="56e17-146">Der Zustand der Backup-Richtlinie für langfristige Aufbewahrung, "aktiviert" oder "deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="56e17-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e17-147">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="56e17-147">-WeeklyRetention</span></span>
<span data-ttu-id="56e17-148">Die wöchentliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="56e17-148">The Weekly Retention.</span></span>
<span data-ttu-id="56e17-149">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="56e17-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="56e17-150">Es gibt eine Minimum von 7 Tagen und maximal 10 Jahren.</span><span class="sxs-lookup"><span data-stu-id="56e17-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="56e17-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="56e17-151">-WeekOfYear</span></span>
<span data-ttu-id="56e17-152">Die Woche des Jahres, 1 bis 52, um die jährliche Aufbewahrung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="56e17-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="56e17-153">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="56e17-153">-YearlyRetention</span></span>
<span data-ttu-id="56e17-154">Die jährliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="56e17-154">The Yearly Retention.</span></span>
<span data-ttu-id="56e17-155">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="56e17-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="56e17-156">Es gibt eine Minimum von 7 Tagen und maximal 10 Jahren.</span><span class="sxs-lookup"><span data-stu-id="56e17-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="56e17-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56e17-157">-Confirm</span></span>
<span data-ttu-id="56e17-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56e17-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e17-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e17-159">-WhatIf</span></span>
<span data-ttu-id="56e17-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56e17-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e17-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56e17-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e17-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e17-162">CommonParameters</span></span>
<span data-ttu-id="56e17-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e17-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e17-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e17-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e17-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56e17-165">INPUTS</span></span>

### <span data-ttu-id="56e17-166">System. String</span><span class="sxs-lookup"><span data-stu-id="56e17-166">System.String</span></span>

### <span data-ttu-id="56e17-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="56e17-167">System.Int32</span></span>

## <span data-ttu-id="56e17-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56e17-168">OUTPUTS</span></span>

### <span data-ttu-id="56e17-169">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="56e17-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="56e17-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="56e17-170">NOTES</span></span>

## <span data-ttu-id="56e17-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56e17-171">RELATED LINKS</span></span>

[<span data-ttu-id="56e17-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="56e17-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="56e17-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="56e17-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="56e17-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="56e17-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="56e17-175">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="56e17-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
