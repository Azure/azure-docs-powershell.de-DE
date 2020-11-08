---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: ec88d8ff9f5a514a3b1b5dcd9ecb917ee348b900
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174067"
---
# <span data-ttu-id="1b1b3-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1b1b3-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="1b1b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1b3-103">Ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="1b1b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b1b3-104">SYNTAX</span></span>

### <span data-ttu-id="1b1b3-105">ServerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b1b3-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b1b3-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b1b3-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b1b3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b1b3-107">DESCRIPTION</span></span>
<span data-ttu-id="1b1b3-108">Das Cmdlet " **Satz-AzSqlServerAudit** " ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="1b1b3-109">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* und Server *Name* , um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="1b1b3-110">Wenn der BLOB-Speicher ein Ziel für Überwachungsprotokolle ist, geben Sie den *StorageAccountResourceId* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter zum Definieren der Speicherschlüssel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="1b1b3-111">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="1b1b3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b1b3-112">EXAMPLES</span></span>

### <span data-ttu-id="1b1b3-113">Beispiel 1: Aktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1b1b3-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="1b1b3-114">Beispiel 2: Deaktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1b1b3-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1b1b3-115">Beispiel 3: Aktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL Server mit erweiterter Filterung mithilfe eines T-SQL-Prädikats</span><span class="sxs-lookup"><span data-stu-id="1b1b3-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="1b1b3-116">Beispiel 4: Entfernen der erweiterten Filtereinstellung aus der Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1b1b3-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="1b1b3-117">Beispiel 5: Aktivieren der Ereignis-Hub-Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1b1b3-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="1b1b3-118">Beispiel 6: Deaktivieren der Ereignis-Hub-Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1b1b3-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="1b1b3-119">Beispiel 7: Aktivieren der Überwachungsrichtlinie für die Protokollanalyse eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1b1b3-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="1b1b3-120">Beispiel 8: Deaktivieren der Überwachungsrichtlinie für die Protokollanalyse eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1b1b3-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1b1b3-121">Beispiel 9: Deaktivieren der Protokollanalyse-Überwachungsrichtlinie für eine Azure SQL Server-Pipeline</span><span class="sxs-lookup"><span data-stu-id="1b1b3-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1b1b3-122">Beispiel 10: Deaktivieren Sie das Senden von Überwachungseinträgen eines Azure SQL Server an den BLOB-Speicher, und aktivieren Sie das Senden an die Protokollanalyse.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1b1b3-123">Beispiel 11: Aktivieren des Sendens von Überwachungsdatensätzen eines Azure SQL Server an BLOB-Speicher, Ereignis-Hub und Protokollanalyse.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="1b1b3-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b1b3-124">PARAMETERS</span></span>

### <span data-ttu-id="1b1b3-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b1b3-125">-AsJob</span></span>
<span data-ttu-id="1b1b3-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1b1b3-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b1b3-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="1b1b3-127">-AuditActionGroup</span></span>
<span data-ttu-id="1b1b3-128">Die empfohlene Gruppe der zu verwendenden Aktionsgruppen ist die folgende Kombination, die alle Abfragen und gespeicherten Prozeduren überprüft, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="1b1b3-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="1b1b3-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="1b1b3-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="1b1b3-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="1b1b3-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="1b1b3-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="1b1b3-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="1b1b3-132">Diese obige Kombination ist auch die standardmäßig konfigurierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="1b1b3-133">Diese Gruppen decken alle SQL-Anweisungen und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Verbindung mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="1b1b3-134">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="1b1b3-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="1b1b3-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="1b1b3-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="1b1b3-136">Gibt an, ob der BLOB-Speicher ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="1b1b3-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1b3-137">-DefaultProfile</span></span>
<span data-ttu-id="1b1b3-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b1b3-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="1b1b3-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="1b1b3-140">Die Ressourcen-ID für die Ereignis-Hub-Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="1b1b3-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="1b1b3-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="1b1b3-141">-EventHubName</span></span>
<span data-ttu-id="1b1b3-142">Der Name des Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-142">The name of the event hub.</span></span> <span data-ttu-id="1b1b3-143">Wenn beim Bereitstellen von EventHubAuthorizationRuleResourceId keine angegeben wird, wird der Standardereignis-Hub ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="1b1b3-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="1b1b3-144">-EventHubTargetState</span></span>
<span data-ttu-id="1b1b3-145">Gibt an, ob der Ereignis-Hub ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="1b1b3-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="1b1b3-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="1b1b3-147">Gibt an, ob die Protokollanalyse ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="1b1b3-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b1b3-148">-PassThru</span></span>
<span data-ttu-id="1b1b3-149">Gibt an, ob die Überwachungsrichtlinie am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1b1b3-150">-Prädikat</span><span class="sxs-lookup"><span data-stu-id="1b1b3-150">-PredicateExpression</span></span>
<span data-ttu-id="1b1b3-151">Das T-SQL-Prädikat (WHERE-Klausel), das zum Filtern von Überwachungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="1b1b3-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1b3-152">-ResourceGroupName</span></span>
<span data-ttu-id="1b1b3-153">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1b3-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1b1b3-154">-RetentionInDays</span></span>
<span data-ttu-id="1b1b3-155">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="1b1b3-156">-Servername</span><span class="sxs-lookup"><span data-stu-id="1b1b3-156">-ServerName</span></span>
<span data-ttu-id="1b1b3-157">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1b3-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="1b1b3-158">-ServerObject</span></span>
<span data-ttu-id="1b1b3-159">Das Serverobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1b3-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1b1b3-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="1b1b3-161">Die Ressourcen-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="1b1b3-161">The storage account resource id</span></span>

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

### <span data-ttu-id="1b1b3-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="1b1b3-162">-StorageKeyType</span></span>
<span data-ttu-id="1b1b3-163">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="1b1b3-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="1b1b3-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="1b1b3-165">Die Arbeitsbereichs-ID (Ressourcen-ID eines Protokollanalyse Arbeitsbereichs) für einen Protokollanalyse Arbeitsbereich, an den Sie Überwachungsprotokolle senden möchten.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="1b1b3-166">Beispiel:/Subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/Insights-Integration/Providers/Microsoft.OperationalInsights/Workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="1b1b3-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="1b1b3-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b1b3-167">-Confirm</span></span>
<span data-ttu-id="1b1b3-168">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b1b3-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b1b3-169">-WhatIf</span></span>
<span data-ttu-id="1b1b3-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b1b3-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b1b3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1b3-172">CommonParameters</span></span>
<span data-ttu-id="1b1b3-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1b3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1b3-174">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b1b3-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1b3-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b1b3-175">INPUTS</span></span>

### <span data-ttu-id="1b1b3-176">System. String</span><span class="sxs-lookup"><span data-stu-id="1b1b3-176">System.String</span></span>

### <span data-ttu-id="1b1b3-177">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1b1b3-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="1b1b3-178">Microsoft. Azure. Commands. SQL. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="1b1b3-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="1b1b3-179">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1b1b3-179">System.Guid</span></span>

### <span data-ttu-id="1b1b3-180">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b1b3-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1b1b3-181">Microsoft. Azure. Commands. SQL. Auditing. Model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="1b1b3-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="1b1b3-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b1b3-182">OUTPUTS</span></span>

### <span data-ttu-id="1b1b3-183">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b1b3-183">System.Boolean</span></span>

## <span data-ttu-id="1b1b3-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b1b3-184">NOTES</span></span>

## <span data-ttu-id="1b1b3-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b1b3-185">RELATED LINKS</span></span>
