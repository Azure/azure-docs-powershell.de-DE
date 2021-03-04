---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 6e3c5c935f6703f5c4f29b2a4ae793fc48e9b16f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940880"
---
# <span data-ttu-id="be13d-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="be13d-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="be13d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be13d-102">SYNOPSIS</span></span>
<span data-ttu-id="be13d-103">Ändert die Überwachungseinstellungen für eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="be13d-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="be13d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be13d-104">SYNTAX</span></span>

### <span data-ttu-id="be13d-105">DatabaseParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="be13d-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be13d-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be13d-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be13d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be13d-107">DESCRIPTION</span></span>
<span data-ttu-id="be13d-108">Das **Cmdlet Set-AzSqlDatabaseAudit** ändert die Überwachungseinstellungen einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="be13d-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="be13d-109">Um das Cmdlet zu verwenden, verwenden Sie die *Parameter ResourceGroupName,* *ServerName* und *DatabaseName,* um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="be13d-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="be13d-110">Wenn blob storage ein Ziel für Überwachungsprotokolle ist, geben Sie den *Parameter StorageAccountResourceId* an, um das Speicherkonto für die Überwachungsprotokolle und den *Parameter StorageKeyType* zum Definieren der Speicherschlüssel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="be13d-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="be13d-111">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *Parameters RetentionInDays* festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="be13d-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="be13d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be13d-112">EXAMPLES</span></span>

### <span data-ttu-id="be13d-113">Beispiel 1: Aktivieren der Blobspeicherüberwachungsrichtlinie einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="be13d-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="be13d-114">Beispiel 2: Deaktivieren der Blobspeicherüberwachungsrichtlinie einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="be13d-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="be13d-115">Beispiel 3: Aktivieren der Blobspeicherüberwachungsrichtlinie einer Azure SQL-Datenbank mit Filtern mithilfe eines T-SQL Prädikats</span><span class="sxs-lookup"><span data-stu-id="be13d-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "schema_name <> 'sys''" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="be13d-116">Beispiel 4: Entfernen der Filterung aus der Überwachungsrichtlinie einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="be13d-116">Example 4: Remove the filtering from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="be13d-117">Beispiel 5: Aktivieren der Ereignishubüberwachungsrichtlinie einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="be13d-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="be13d-118">Beispiel 6: Deaktivieren der Ereignishubüberwachungsrichtlinie einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="be13d-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="be13d-119">Beispiel 7: Aktivieren der Protokollanalyseüberwachungsrichtlinie einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="be13d-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="be13d-120">Beispiel 8: Deaktivieren der Protokollanalyseüberwachungsrichtlinie einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="be13d-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="be13d-121">Beispiel 9: Deaktivieren der Protokollanalyseüberwachungsrichtlinie einer Azure SQL Pipeline</span><span class="sxs-lookup"><span data-stu-id="be13d-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="be13d-122">Beispiel 10: Deaktivieren sie das Senden von Überwachungsdatensätzen einer Azure SQL-Datenbank an den Blobspeicher, und aktivieren Sie das Senden zum Protokollieren von Analysen.</span><span class="sxs-lookup"><span data-stu-id="be13d-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="be13d-123">Beispiel 11: Aktivieren des Sendens von Überwachungsdatensätzen einer Azure SQL-Datenbank an blob storage, event hub und log analytics.</span><span class="sxs-lookup"><span data-stu-id="be13d-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="be13d-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="be13d-124">PARAMETERS</span></span>

### <span data-ttu-id="be13d-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="be13d-125">-AuditAction</span></span>
<span data-ttu-id="be13d-126">Die Gruppe der Überwachungsaktionen.</span><span class="sxs-lookup"><span data-stu-id="be13d-126">The set of audit actions.</span></span>  
<span data-ttu-id="be13d-127">Die unterstützten Aktionen zur Überwachung sind:</span><span class="sxs-lookup"><span data-stu-id="be13d-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="be13d-128">SELECT</span><span class="sxs-lookup"><span data-stu-id="be13d-128">SELECT</span></span>  
<span data-ttu-id="be13d-129">UPDATE</span><span class="sxs-lookup"><span data-stu-id="be13d-129">UPDATE</span></span>  
<span data-ttu-id="be13d-130">EINFÜGEN</span><span class="sxs-lookup"><span data-stu-id="be13d-130">INSERT</span></span>  
<span data-ttu-id="be13d-131">LÖSCHEN</span><span class="sxs-lookup"><span data-stu-id="be13d-131">DELETE</span></span>  
<span data-ttu-id="be13d-132">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="be13d-132">EXECUTE</span></span>  
<span data-ttu-id="be13d-133">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="be13d-133">RECEIVE</span></span>  
<span data-ttu-id="be13d-134">VERWEISE</span><span class="sxs-lookup"><span data-stu-id="be13d-134">REFERENCES</span></span>  
<span data-ttu-id="be13d-135">Das allgemeine Formular zum Definieren einer zu überwachenden Aktion ist: [Aktion] EIN [Objekt] BY [Prinzipal] Beachten Sie, dass [Objekt] im oben angegebenen Format auf ein Objekt wie eine Tabelle, Ansicht oder gespeicherte Prozedur oder eine gesamte Datenbank oder ein gesamtes Schema verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="be13d-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="be13d-136">In letzteren Fällen werden die Formulare DATABASE::[dbname] und SCHEMA::[Schemaname] verwendet.</span><span class="sxs-lookup"><span data-stu-id="be13d-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="be13d-137">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="be13d-137">For example:</span></span>  
<span data-ttu-id="be13d-138">SELECT on dbo.myTable by public</span><span class="sxs-lookup"><span data-stu-id="be13d-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="be13d-139">SELECT on DATABASE::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="be13d-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="be13d-140">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="be13d-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="be13d-141">Weitere Informationen finden Sie unter https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="be13d-141">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="be13d-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="be13d-142">-AuditActionGroup</span></span>
<span data-ttu-id="be13d-143">Die empfohlene Gruppe von Aktionsgruppen ist die folgende Kombination: Dadurch werden alle Abfragen und gespeicherten Prozeduren überwacht, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="be13d-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="be13d-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="be13d-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="be13d-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="be13d-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="be13d-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="be13d-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="be13d-147">Diese obige Kombination ist auch der Satz, der standardmäßig konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="be13d-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="be13d-148">Diese Gruppen decken alle SQL und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Kombination mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="be13d-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="be13d-149">Weitere Informationen finden Sie unter https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="be13d-149">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="be13d-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="be13d-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="be13d-151">Gibt an, ob blob storage ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="be13d-151">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="be13d-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="be13d-152">-DatabaseName</span></span>
<span data-ttu-id="be13d-153">SQL Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="be13d-153">SQL Database name.</span></span>

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

### <span data-ttu-id="be13d-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="be13d-154">-DatabaseObject</span></span>
<span data-ttu-id="be13d-155">Das Datenbankobjekt zum Verwalten seiner Überwachungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="be13d-155">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="be13d-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be13d-156">-DefaultProfile</span></span>
<span data-ttu-id="be13d-157">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be13d-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be13d-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="be13d-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="be13d-159">Die Ressourcen-ID für die Ereignishubautorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="be13d-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="be13d-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="be13d-160">-EventHubName</span></span>
<span data-ttu-id="be13d-161">Der Name des Ereignishubs.</span><span class="sxs-lookup"><span data-stu-id="be13d-161">The name of the event hub.</span></span> <span data-ttu-id="be13d-162">Wenn beim Bereitstellen von EventHubAuthorizationRuleResourceId keine angegeben wird, wird der Standardereignishub ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="be13d-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="be13d-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="be13d-163">-EventHubTargetState</span></span>
<span data-ttu-id="be13d-164">Gibt an, ob der Ereignishub ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="be13d-164">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="be13d-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="be13d-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="be13d-166">Gibt an, ob die Protokollanalyse ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="be13d-166">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="be13d-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be13d-167">-PassThru</span></span>
<span data-ttu-id="be13d-168">Gibt an, ob die Überwachungsrichtlinie am Ende der Cmdletausführung ausgegeben werden soll</span><span class="sxs-lookup"><span data-stu-id="be13d-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="be13d-169">-PrädikateExpression</span><span class="sxs-lookup"><span data-stu-id="be13d-169">-PredicateExpression</span></span>
<span data-ttu-id="be13d-170">Das T-SQL -Prädikat (WHERE-Klausel), das zum Filtern von Überwachungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be13d-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="be13d-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be13d-171">-ResourceGroupName</span></span>
<span data-ttu-id="be13d-172">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="be13d-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="be13d-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="be13d-173">-RetentionInDays</span></span>
<span data-ttu-id="be13d-174">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="be13d-174">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="be13d-175">-Servername</span><span class="sxs-lookup"><span data-stu-id="be13d-175">-ServerName</span></span>
<span data-ttu-id="be13d-176">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="be13d-176">SQL server name.</span></span>

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

### <span data-ttu-id="be13d-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="be13d-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="be13d-178">Ressourcen-ID des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="be13d-178">The storage account resource id</span></span>

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

### <span data-ttu-id="be13d-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="be13d-179">-StorageKeyType</span></span>
<span data-ttu-id="be13d-180">Gibt an, welcher der Speicherzugriffsschlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="be13d-180">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="be13d-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="be13d-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="be13d-182">Die Arbeitsbereichs-ID (Ressourcen-ID eines Log Analytics-Arbeitsbereichs) für einen Log Analytics-Arbeitsbereich, an den Sie Überwachungsprotokolle senden möchten.</span><span class="sxs-lookup"><span data-stu-id="be13d-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="be13d-183">Beispiel: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="be13d-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="be13d-184">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be13d-184">-Confirm</span></span>
<span data-ttu-id="be13d-185">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be13d-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be13d-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be13d-186">-WhatIf</span></span>
<span data-ttu-id="be13d-187">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be13d-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be13d-188">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be13d-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be13d-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be13d-189">CommonParameters</span></span>
<span data-ttu-id="be13d-190">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be13d-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be13d-191">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be13d-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be13d-192">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be13d-192">INPUTS</span></span>

### <span data-ttu-id="be13d-193">System.String</span><span class="sxs-lookup"><span data-stu-id="be13d-193">System.String</span></span>

### <span data-ttu-id="be13d-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="be13d-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="be13d-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="be13d-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="be13d-196">System.String[]</span><span class="sxs-lookup"><span data-stu-id="be13d-196">System.String[]</span></span>

### <span data-ttu-id="be13d-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="be13d-197">System.Guid</span></span>

### <span data-ttu-id="be13d-198">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="be13d-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="be13d-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="be13d-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="be13d-200">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be13d-200">OUTPUTS</span></span>

### <span data-ttu-id="be13d-201">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be13d-201">System.Boolean</span></span>

## <span data-ttu-id="be13d-202">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="be13d-202">NOTES</span></span>

## <span data-ttu-id="be13d-203">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="be13d-203">RELATED LINKS</span></span>
