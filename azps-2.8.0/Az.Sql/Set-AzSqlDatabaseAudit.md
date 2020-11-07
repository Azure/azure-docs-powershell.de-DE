---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 0a9122f4869c1d1d68fe5fc0fcdc5f4151b47e66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825767"
---
# <span data-ttu-id="802ef-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="802ef-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="802ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="802ef-102">SYNOPSIS</span></span>
<span data-ttu-id="802ef-103">Ändert die Überwachungseinstellungen für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="802ef-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="802ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="802ef-104">SYNTAX</span></span>

### <span data-ttu-id="802ef-105">DatabaseParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="802ef-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="802ef-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="802ef-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="802ef-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="802ef-107">DESCRIPTION</span></span>
<span data-ttu-id="802ef-108">Das Cmdlet " **Satz-AzSqlDatabaseAudit** " ändert die Überwachungseinstellungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="802ef-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="802ef-109">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="802ef-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="802ef-110">Wenn der BLOB-Speicher ein Ziel für Überwachungsprotokolle ist, geben Sie den *StorageAccountResourceId* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter zum Definieren der Speicherschlüssel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="802ef-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="802ef-111">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="802ef-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="802ef-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="802ef-112">EXAMPLES</span></span>

### <span data-ttu-id="802ef-113">Beispiel 1: Aktivieren der BLOB-Speicher Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="802ef-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="802ef-114">Beispiel 2: Deaktivieren der BLOB-Speicher Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="802ef-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="802ef-115">Beispiel 3,1: Aktivieren der BLOB-Speicher Überwachungsrichtlinie einer Azure SQL-Datenbank mit erweiterter Filterung mithilfe eines T-SQL-Prädikats</span><span class="sxs-lookup"><span data-stu-id="802ef-115">Example 3.1: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="802ef-116">Beispiel 3,2: Entfernen der erweiterten Filtereinstellung aus der Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="802ef-116">Example 3.2: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="802ef-117">Beispiel 4: Aktivieren der Ereignis-Hub-Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="802ef-117">Example 4: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="802ef-118">Beispiel 5: Deaktivieren der Ereignis-Hub-Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="802ef-118">Example 5: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="802ef-119">Beispiel 6: Aktivieren der Überwachungsrichtlinie für die Protokollanalyse einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="802ef-119">Example 6: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="802ef-120">Beispiel 7: Deaktivieren der Überwachungsrichtlinie für die Protokollanalyse einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="802ef-120">Example 7: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="802ef-121">Beispiel 8: Deaktivieren Sie die Protokollanalyse-Überwachungsrichtlinie einer Azure SQL-Datenbank durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="802ef-121">Example 8: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="802ef-122">Beispiel 9: Deaktivieren Sie das Senden von Überwachungsdatensätzen einer Azure SQL-Datenbank an den BLOB-Speicher, und aktivieren Sie das Senden an die Protokollanalyse.</span><span class="sxs-lookup"><span data-stu-id="802ef-122">Example 9: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="802ef-123">Beispiel 10: Aktivieren Sie das Senden von Überwachungsdatensätzen einer Azure SQL-Datenbank an BLOB-Speicher, Ereignis-Hub und Protokollanalyse.</span><span class="sxs-lookup"><span data-stu-id="802ef-123">Example 10: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="802ef-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="802ef-124">PARAMETERS</span></span>

### <span data-ttu-id="802ef-125">-Auditing</span><span class="sxs-lookup"><span data-stu-id="802ef-125">-AuditAction</span></span>
<span data-ttu-id="802ef-126">Die Gruppe von Überwachungsaktionen.</span><span class="sxs-lookup"><span data-stu-id="802ef-126">The set of audit actions.</span></span>  
<span data-ttu-id="802ef-127">Die unterstützten zu überwachenden Aktionen sind:</span><span class="sxs-lookup"><span data-stu-id="802ef-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="802ef-128">Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="802ef-128">SELECT</span></span>  
<span data-ttu-id="802ef-129">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="802ef-129">UPDATE</span></span>  
<span data-ttu-id="802ef-130">Einfügen</span><span class="sxs-lookup"><span data-stu-id="802ef-130">INSERT</span></span>  
<span data-ttu-id="802ef-131">Löschen</span><span class="sxs-lookup"><span data-stu-id="802ef-131">DELETE</span></span>  
<span data-ttu-id="802ef-132">Ausführen</span><span class="sxs-lookup"><span data-stu-id="802ef-132">EXECUTE</span></span>  
<span data-ttu-id="802ef-133">Erhalten</span><span class="sxs-lookup"><span data-stu-id="802ef-133">RECEIVE</span></span>  
<span data-ttu-id="802ef-134">Referenzen</span><span class="sxs-lookup"><span data-stu-id="802ef-134">REFERENCES</span></span>  
<span data-ttu-id="802ef-135">Die allgemeine Form zum Definieren einer zu überwachenden Aktion lautet: [Aktion] auf [Objekt] nach [Principal] Beachten Sie, dass [Objekt] im obigen Format auf ein Objekt wie eine Tabelle, eine Sicht oder eine gespeicherte Prozedur oder auf eine gesamte Datenbank oder ein ganzes Schema verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="802ef-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="802ef-136">In den letzten Fällen werden die Formulare Database:: [DBName] und Schema:: [SchemaName] verwendet.</span><span class="sxs-lookup"><span data-stu-id="802ef-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="802ef-137">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="802ef-137">For example:</span></span>  
<span data-ttu-id="802ef-138">Auswählen von "dbo. MyTable" nach öffentlichem</span><span class="sxs-lookup"><span data-stu-id="802ef-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="802ef-139">Wählen Sie in Database:: MyDatabase by Public aus.</span><span class="sxs-lookup"><span data-stu-id="802ef-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="802ef-140">Wählen Sie auf Schema:: MySchema nach öffentlichen</span><span class="sxs-lookup"><span data-stu-id="802ef-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="802ef-141">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="802ef-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="802ef-142">-AuditActionGroup</span></span>
<span data-ttu-id="802ef-143">Die empfohlene Gruppe der zu verwendenden Aktionsgruppen ist die folgende Kombination, die alle Abfragen und gespeicherten Prozeduren überprüft, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="802ef-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="802ef-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="802ef-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="802ef-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="802ef-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="802ef-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="802ef-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="802ef-147">Diese obige Kombination ist auch die standardmäßig konfigurierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="802ef-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="802ef-148">Diese Gruppen decken alle SQL-Anweisungen und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Verbindung mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="802ef-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="802ef-149">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="802ef-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="802ef-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="802ef-151">Gibt an, ob der BLOB-Speicher ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="802ef-151">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="802ef-152">-DatabaseName</span></span>
<span data-ttu-id="802ef-153">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="802ef-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="802ef-154">-DatabaseObject</span></span>
<span data-ttu-id="802ef-155">Das Datenbankobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="802ef-155">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802ef-156">-DefaultProfile</span></span>
<span data-ttu-id="802ef-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="802ef-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="802ef-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="802ef-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="802ef-159">Die Ressourcen-ID für die Ereignis-Hub-Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="802ef-159">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="802ef-160">-EventHubName</span></span>
<span data-ttu-id="802ef-161">Der Name des Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="802ef-161">The name of the event hub.</span></span> <span data-ttu-id="802ef-162">Wenn beim Bereitstellen von EventHubAuthorizationRuleResourceId keine angegeben wird, wird der Standardereignis-Hub ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="802ef-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="802ef-163">-EventHubTargetState</span></span>
<span data-ttu-id="802ef-164">Gibt an, ob der Ereignis-Hub ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="802ef-164">Indicates whether event hub is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="802ef-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="802ef-166">Gibt an, ob die Protokollanalyse ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="802ef-166">Indicates whether log analytics is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="802ef-167">-PassThru</span></span>
<span data-ttu-id="802ef-168">Gibt an, ob die Überwachungsrichtlinie am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="802ef-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="802ef-169">-Prädikat</span><span class="sxs-lookup"><span data-stu-id="802ef-169">-PredicateExpression</span></span>
<span data-ttu-id="802ef-170">Das T-SQL-Prädikat (WHERE-Klausel), das zum Filtern von Überwachungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="802ef-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="802ef-171">-ResourceGroupName</span></span>
<span data-ttu-id="802ef-172">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="802ef-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="802ef-173">-RetentionInDays</span></span>
<span data-ttu-id="802ef-174">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="802ef-174">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-175">-Servername</span><span class="sxs-lookup"><span data-stu-id="802ef-175">-ServerName</span></span>
<span data-ttu-id="802ef-176">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="802ef-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="802ef-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="802ef-178">Die Ressourcen-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="802ef-178">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="802ef-179">-StorageKeyType</span></span>
<span data-ttu-id="802ef-180">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="802ef-180">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="802ef-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="802ef-182">Die Arbeitsbereichs-ID (Ressourcen-ID eines Protokollanalyse Arbeitsbereichs) für einen Protokollanalyse Arbeitsbereich, an den Sie Überwachungsprotokolle senden möchten.</span><span class="sxs-lookup"><span data-stu-id="802ef-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="802ef-183">Beispiel:/Subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/Insights-Integration/Providers/Microsoft.OperationalInsights/Workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="802ef-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802ef-184">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="802ef-184">-Confirm</span></span>
<span data-ttu-id="802ef-185">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="802ef-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="802ef-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="802ef-186">-WhatIf</span></span>
<span data-ttu-id="802ef-187">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="802ef-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="802ef-188">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="802ef-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="802ef-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802ef-189">CommonParameters</span></span>
<span data-ttu-id="802ef-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="802ef-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802ef-191">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="802ef-191">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802ef-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="802ef-192">INPUTS</span></span>

### <span data-ttu-id="802ef-193">System. String</span><span class="sxs-lookup"><span data-stu-id="802ef-193">System.String</span></span>

### <span data-ttu-id="802ef-194">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="802ef-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="802ef-195">Microsoft. Azure. Commands. SQL. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="802ef-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="802ef-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="802ef-196">System.String[]</span></span>

### <span data-ttu-id="802ef-197">System. GUID</span><span class="sxs-lookup"><span data-stu-id="802ef-197">System.Guid</span></span>

### <span data-ttu-id="802ef-198">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="802ef-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="802ef-199">Microsoft. Azure. Commands. SQL. Auditing. Model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="802ef-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="802ef-200">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="802ef-200">OUTPUTS</span></span>

### <span data-ttu-id="802ef-201">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="802ef-201">System.Boolean</span></span>

## <span data-ttu-id="802ef-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="802ef-202">NOTES</span></span>

## <span data-ttu-id="802ef-203">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="802ef-203">RELATED LINKS</span></span>
