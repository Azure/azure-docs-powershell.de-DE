---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: f8a31171309a9c869d29078ff09ce8903288e8bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825348"
---
# <span data-ttu-id="8cb23-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="8cb23-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="8cb23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cb23-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb23-103">**Wichtig: Dieses Cmdlet ist veraltet, wenn Sie von [AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) ersetzt werden.**</span><span class="sxs-lookup"><span data-stu-id="8cb23-103">**Important: This cmdlet is deprecated, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="8cb23-104">Ändert die Überwachungseinstellungen für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8cb23-104">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="8cb23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cb23-105">SYNTAX</span></span>

### <span data-ttu-id="8cb23-106">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8cb23-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb23-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="8cb23-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb23-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="8cb23-108">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb23-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="8cb23-109">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb23-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8cb23-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb23-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8cb23-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cb23-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8cb23-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb23-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8cb23-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cb23-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb23-114">DESCRIPTION</span></span>
<span data-ttu-id="8cb23-115">Das Cmdlet " **Satz-AzSqlDatabaseAuditing** " ändert die Überwachungseinstellungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8cb23-115">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="8cb23-116">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8cb23-116">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="8cb23-117">Das Ziel der Überwachungsprotokolle wird bestimmt, indem Sie einen der folgenden Switch-Parameter angeben: BlobStorage, LogAnalytics oder EventHub (wenn keine angegeben ist, ist der Standardwert BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="8cb23-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="8cb23-118">Verwenden Sie den *State* -Parameter, um die Richtlinie zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8cb23-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="8cb23-119">Wenn das Überwachungsprotokoll Ziel BLOB-Speicher ist, geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter zum Definieren der Speicherschlüssel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="8cb23-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="8cb23-120">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8cb23-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="8cb23-121">Wenn das Cmdlet erfolgreich ausgeführt wird und Sie den *passthru* -Parameter verwenden, wird zusätzlich zu den Datenbankbezeichnern ein Objekt zurückgegeben, das die aktuellen Überwachungseinstellungen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8cb23-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="8cb23-122">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="8cb23-122">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="8cb23-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cb23-123">EXAMPLES</span></span>

### <span data-ttu-id="8cb23-124">Beispiel 1: Aktivieren der BLOB-Speicher Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8cb23-124">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="8cb23-125">Beispiel 2: Deaktivieren der BLOB-Speicher Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8cb23-125">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="8cb23-126">Beispiel 3: Aktivieren der BLOB-Speicher Überwachungsrichtlinie einer Azure SQL-Datenbank unter Verwendung eines speicherkontos aus einem anderen Abonnement</span><span class="sxs-lookup"><span data-stu-id="8cb23-126">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="8cb23-127">Beispiel 4: Aktivieren der BLOB-Speicher Überwachungsrichtlinie einer Azure SQL-Datenbank mit erweiterter Filterung mithilfe eines T-SQL-Prädikats</span><span class="sxs-lookup"><span data-stu-id="8cb23-127">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="8cb23-128">Beispiel 5: Entfernen der erweiterten Filtereinstellung aus der BLOB-Speicher Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8cb23-128">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="8cb23-129">Beispiel 6: Aktivieren der Ereignis-Hub-Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8cb23-129">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="8cb23-130">Beispiel 7: Deaktivieren der Ereignis-Hub-Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8cb23-130">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="8cb23-131">Beispiel 8: Aktivieren der Überwachungsrichtlinie für die Protokollanalyse einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8cb23-131">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="8cb23-132">Beispiel 9: Deaktivieren der Überwachungsrichtlinie für die Protokollanalyse einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8cb23-132">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="8cb23-133">Beispiel 10: Deaktivieren Sie die Protokollanalyse-Überwachungsrichtlinie einer Azure SQL-Datenbank durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8cb23-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="8cb23-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb23-134">PARAMETERS</span></span>

### <span data-ttu-id="8cb23-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cb23-135">-AsJob</span></span>
<span data-ttu-id="8cb23-136">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8cb23-136">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-137">-Auditing</span><span class="sxs-lookup"><span data-stu-id="8cb23-137">-AuditAction</span></span>
<span data-ttu-id="8cb23-138">Die Gruppe von Überwachungsaktionen.</span><span class="sxs-lookup"><span data-stu-id="8cb23-138">The set of audit actions.</span></span>  
<span data-ttu-id="8cb23-139">Die unterstützten zu überwachenden Aktionen sind:</span><span class="sxs-lookup"><span data-stu-id="8cb23-139">The supported actions to audit are:</span></span>  
<span data-ttu-id="8cb23-140">Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="8cb23-140">SELECT</span></span>  
<span data-ttu-id="8cb23-141">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8cb23-141">UPDATE</span></span>  
<span data-ttu-id="8cb23-142">Einfügen</span><span class="sxs-lookup"><span data-stu-id="8cb23-142">INSERT</span></span>  
<span data-ttu-id="8cb23-143">Löschen</span><span class="sxs-lookup"><span data-stu-id="8cb23-143">DELETE</span></span>  
<span data-ttu-id="8cb23-144">Ausführen</span><span class="sxs-lookup"><span data-stu-id="8cb23-144">EXECUTE</span></span>  
<span data-ttu-id="8cb23-145">Erhalten</span><span class="sxs-lookup"><span data-stu-id="8cb23-145">RECEIVE</span></span>  
<span data-ttu-id="8cb23-146">Verweist auf das allgemeine Formular zum Definieren einer zu überwachenden Aktion lautet: [Aktion] auf [Objekt] nach [Prinzipal] Beachten Sie, dass [Objekt] im obigen Format auf ein Objekt wie eine Tabelle, eine Sicht oder eine gespeicherte Prozedur oder auf eine gesamte Datenbank oder ein ganzes Schema verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="8cb23-146">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="8cb23-147">In den letzten Fällen werden die Formulare Database:: [DBName] und Schema:: [SchemaName] verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cb23-147">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="8cb23-148">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8cb23-148">For example:</span></span>  
<span data-ttu-id="8cb23-149">Auswählen von "dbo. MyTable" nach öffentlichem</span><span class="sxs-lookup"><span data-stu-id="8cb23-149">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="8cb23-150">Wählen Sie in Database:: MyDatabase by Public aus.</span><span class="sxs-lookup"><span data-stu-id="8cb23-150">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="8cb23-151">Wählen Sie auf Schema:: MySchema nach öffentlichen</span><span class="sxs-lookup"><span data-stu-id="8cb23-151">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="8cb23-152">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="8cb23-152">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-153">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="8cb23-153">-AuditActionGroup</span></span>
<span data-ttu-id="8cb23-154">Die empfohlene Gruppe der zu verwendenden Aktionsgruppen ist die folgende Kombination, die alle Abfragen und gespeicherten Prozeduren überprüft, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="8cb23-154">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="8cb23-155">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8cb23-155">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="8cb23-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8cb23-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="8cb23-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="8cb23-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="8cb23-158">Diese obige Kombination ist auch die standardmäßig konfigurierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8cb23-158">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="8cb23-159">Diese Gruppen decken alle SQL-Anweisungen und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Verbindung mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="8cb23-159">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="8cb23-160">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="8cb23-160">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-161">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="8cb23-161">-BlobStorage</span></span>
<span data-ttu-id="8cb23-162">Gibt an, dass das Überwachungsprotokoll Ziel BLOB-Speicher ist</span><span class="sxs-lookup"><span data-stu-id="8cb23-162">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-163">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8cb23-163">-DatabaseName</span></span>
<span data-ttu-id="8cb23-164">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="8cb23-164">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb23-165">-DefaultProfile</span></span>
<span data-ttu-id="8cb23-166">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cb23-166">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cb23-167">-EventHub</span><span class="sxs-lookup"><span data-stu-id="8cb23-167">-EventHub</span></span>
<span data-ttu-id="8cb23-168">Gibt an, dass das Überwachungsprotokoll Zielereignis-Hub ist</span><span class="sxs-lookup"><span data-stu-id="8cb23-168">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-169">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="8cb23-169">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="8cb23-170">Die Ressourcen-ID für die Ereignis-Hub-Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="8cb23-170">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-171">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="8cb23-171">-EventHubName</span></span>
<span data-ttu-id="8cb23-172">Der Name des Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="8cb23-172">The name of the event hub.</span></span> <span data-ttu-id="8cb23-173">Wenn beim Bereitstellen von EventHubAuthorizationRuleResourceId keine angegeben wird, wird der Standardereignis-Hub ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8cb23-173">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-174">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8cb23-174">-InputObject</span></span>
<span data-ttu-id="8cb23-175">Das Datenbankobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cb23-175">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-176">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="8cb23-176">-LogAnalytics</span></span>
<span data-ttu-id="8cb23-177">Gibt an, dass die Überwachungsprotokolle Zielprotokoll Analyse sind.</span><span class="sxs-lookup"><span data-stu-id="8cb23-177">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-178">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cb23-178">-PassThru</span></span>
<span data-ttu-id="8cb23-179">Gibt an, ob die Überwachungsrichtlinie am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cb23-179">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-180">-Prädikat</span><span class="sxs-lookup"><span data-stu-id="8cb23-180">-PredicateExpression</span></span>
<span data-ttu-id="8cb23-181">Das T-SQL-Prädikat (WHERE-Klausel), das zum Filtern von Überwachungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cb23-181">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb23-182">-ResourceGroupName</span></span>
<span data-ttu-id="8cb23-183">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8cb23-183">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-184">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8cb23-184">-RetentionInDays</span></span>
<span data-ttu-id="8cb23-185">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="8cb23-185">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-186">-Servername</span><span class="sxs-lookup"><span data-stu-id="8cb23-186">-ServerName</span></span>
<span data-ttu-id="8cb23-187">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="8cb23-187">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-188">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="8cb23-188">-State</span></span>
<span data-ttu-id="8cb23-189">Der Zustand der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8cb23-189">The state of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-190">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8cb23-190">-StorageAccountName</span></span>
<span data-ttu-id="8cb23-191">Der Name des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="8cb23-191">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-192">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8cb23-192">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="8cb23-193">Die Abonnement-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8cb23-193">The storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-194">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="8cb23-194">-StorageKeyType</span></span>
<span data-ttu-id="8cb23-195">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cb23-195">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-196">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="8cb23-196">-WorkspaceResourceId</span></span>
<span data-ttu-id="8cb23-197">Die Arbeitsbereichs-ID (Ressourcen-ID eines Protokollanalyse Arbeitsbereichs) für einen Protokollanalyse Arbeitsbereich, an den Sie Überwachungsprotokolle senden möchten.</span><span class="sxs-lookup"><span data-stu-id="8cb23-197">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="8cb23-198">Beispiel:/Subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/Insights-Integration/Providers/Microsoft.OperationalInsights/Workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="8cb23-198">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb23-199">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8cb23-199">-Confirm</span></span>
<span data-ttu-id="8cb23-200">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cb23-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cb23-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cb23-201">-WhatIf</span></span>
<span data-ttu-id="8cb23-202">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cb23-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cb23-203">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb23-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cb23-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb23-204">CommonParameters</span></span>
<span data-ttu-id="8cb23-205">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cb23-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb23-206">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cb23-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb23-207">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cb23-207">INPUTS</span></span>

### <span data-ttu-id="8cb23-208">System. String</span><span class="sxs-lookup"><span data-stu-id="8cb23-208">System.String</span></span>

### <span data-ttu-id="8cb23-209">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8cb23-209">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="8cb23-210">Microsoft. Azure. Commands. SQL. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="8cb23-210">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="8cb23-211">System. String []</span><span class="sxs-lookup"><span data-stu-id="8cb23-211">System.String[]</span></span>

### <span data-ttu-id="8cb23-212">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="8cb23-212">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8cb23-213">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8cb23-213">System.Guid</span></span>

### <span data-ttu-id="8cb23-214">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8cb23-214">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8cb23-215">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cb23-215">OUTPUTS</span></span>

### <span data-ttu-id="8cb23-216">Microsoft. Azure. Commands. SQL. Auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="8cb23-216">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="8cb23-217">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cb23-217">NOTES</span></span>

## <span data-ttu-id="8cb23-218">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cb23-218">RELATED LINKS</span></span>
