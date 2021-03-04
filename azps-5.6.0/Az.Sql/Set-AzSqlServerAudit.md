---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 8b0312ddcdce5c538b80f0245470496c534bf07f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939859"
---
# <span data-ttu-id="09ffa-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="09ffa-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="09ffa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="09ffa-103">Ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="09ffa-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="09ffa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09ffa-104">SYNTAX</span></span>

### <span data-ttu-id="09ffa-105">ServerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="09ffa-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09ffa-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ffa-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09ffa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09ffa-107">DESCRIPTION</span></span>
<span data-ttu-id="09ffa-108">Das **Cmdlet Set-AzSqlServerAudit** ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="09ffa-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="09ffa-109">Um das Cmdlet zu verwenden, verwenden Sie die *Parameter ResourceGroupName* und *ServerName,* um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="09ffa-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="09ffa-110">Wenn blob storage ein Ziel für Überwachungsprotokolle ist, geben Sie den *Parameter StorageAccountResourceId* an, um das Speicherkonto für die Überwachungsprotokolle und den *Parameter StorageKeyType* zum Definieren der Speicherschlüssel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="09ffa-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="09ffa-111">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *Parameters RetentionInDays* festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="09ffa-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="09ffa-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09ffa-112">EXAMPLES</span></span>

### <span data-ttu-id="09ffa-113">Beispiel 1: Aktivieren der Blobspeicherüberwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="09ffa-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="09ffa-114">Beispiel 2: Deaktivieren der Blobspeicherüberwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="09ffa-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="09ffa-115">Beispiel 3: Aktivieren der Blobspeicherüberwachungsrichtlinie eines Azure SQL-Servers mit erweiterter Filterung mithilfe eines T-SQL Prädikats</span><span class="sxs-lookup"><span data-stu-id="09ffa-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="09ffa-116">Beispiel 4: Entfernen der Einstellung für erweiterte Filter aus der Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="09ffa-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="09ffa-117">Beispiel 5: Aktivieren der Ereignishubüberwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="09ffa-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="09ffa-118">Beispiel 6: Deaktivieren der Ereignishubüberwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="09ffa-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="09ffa-119">Beispiel 7: Aktivieren der Protokollanalyseüberwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="09ffa-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="09ffa-120">Beispiel 8: Deaktivieren der Protokollanalyseüberwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="09ffa-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="09ffa-121">Beispiel 9: Deaktivieren der Überwachungsrichtlinie für die Protokollanalyse eines Azure SQL Pipeline</span><span class="sxs-lookup"><span data-stu-id="09ffa-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="09ffa-122">Beispiel 10: Deaktivieren Sie das Senden von Überwachungsdatensätzen eines Azure SQL-Servers an den Blobspeicher, und aktivieren Sie das Senden zum Protokollieren von Analysen.</span><span class="sxs-lookup"><span data-stu-id="09ffa-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="09ffa-123">Beispiel 11: Aktivieren des Sendens von Überwachungsdatensätzen eines Azure SQL an blob storage, event hub und log analytics.</span><span class="sxs-lookup"><span data-stu-id="09ffa-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="09ffa-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="09ffa-124">PARAMETERS</span></span>

### <span data-ttu-id="09ffa-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09ffa-125">-AsJob</span></span>
<span data-ttu-id="09ffa-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="09ffa-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09ffa-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="09ffa-127">-AuditActionGroup</span></span>
<span data-ttu-id="09ffa-128">Die empfohlene Gruppe von Aktionsgruppen ist die folgende Kombination: Dadurch werden alle Abfragen und gespeicherten Prozeduren überwacht, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="09ffa-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="09ffa-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="09ffa-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="09ffa-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="09ffa-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="09ffa-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="09ffa-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="09ffa-132">Diese obige Kombination ist auch der Satz, der standardmäßig konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="09ffa-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="09ffa-133">Diese Gruppen decken alle SQL und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Kombination mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="09ffa-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="09ffa-134">Weitere Informationen finden Sie unter https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="09ffa-134">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="09ffa-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="09ffa-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="09ffa-136">Gibt an, ob blob storage ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="09ffa-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="09ffa-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ffa-137">-DefaultProfile</span></span>
<span data-ttu-id="09ffa-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09ffa-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09ffa-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="09ffa-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="09ffa-140">Die Ressourcen-ID für die Ereignishubautorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="09ffa-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="09ffa-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="09ffa-141">-EventHubName</span></span>
<span data-ttu-id="09ffa-142">Der Name des Ereignishubs.</span><span class="sxs-lookup"><span data-stu-id="09ffa-142">The name of the event hub.</span></span> <span data-ttu-id="09ffa-143">Wenn beim Bereitstellen von EventHubAuthorizationRuleResourceId keine angegeben wird, wird der Standardereignishub ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="09ffa-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="09ffa-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="09ffa-144">-EventHubTargetState</span></span>
<span data-ttu-id="09ffa-145">Gibt an, ob der Ereignishub ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="09ffa-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="09ffa-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="09ffa-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="09ffa-147">Gibt an, ob die Protokollanalyse ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="09ffa-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="09ffa-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09ffa-148">-PassThru</span></span>
<span data-ttu-id="09ffa-149">Gibt an, ob die Überwachungsrichtlinie am Ende der Cmdletausführung ausgegeben werden soll</span><span class="sxs-lookup"><span data-stu-id="09ffa-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="09ffa-150">-PrädikateExpression</span><span class="sxs-lookup"><span data-stu-id="09ffa-150">-PredicateExpression</span></span>
<span data-ttu-id="09ffa-151">Das T-SQL -Prädikat (WHERE-Klausel), das zum Filtern von Überwachungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09ffa-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="09ffa-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ffa-152">-ResourceGroupName</span></span>
<span data-ttu-id="09ffa-153">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="09ffa-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="09ffa-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="09ffa-154">-RetentionInDays</span></span>
<span data-ttu-id="09ffa-155">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="09ffa-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="09ffa-156">-Servername</span><span class="sxs-lookup"><span data-stu-id="09ffa-156">-ServerName</span></span>
<span data-ttu-id="09ffa-157">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="09ffa-157">SQL server name.</span></span>

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

### <span data-ttu-id="09ffa-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="09ffa-158">-ServerObject</span></span>
<span data-ttu-id="09ffa-159">Das Serverobjekt zum Verwalten seiner Überwachungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="09ffa-159">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="09ffa-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="09ffa-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="09ffa-161">Ressourcen-ID des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="09ffa-161">The storage account resource id</span></span>

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

### <span data-ttu-id="09ffa-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="09ffa-162">-StorageKeyType</span></span>
<span data-ttu-id="09ffa-163">Gibt an, welcher der Speicherzugriffsschlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09ffa-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="09ffa-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="09ffa-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="09ffa-165">Die Arbeitsbereichs-ID (Ressourcen-ID eines Log Analytics-Arbeitsbereichs) für einen Log Analytics-Arbeitsbereich, an den Sie Überwachungsprotokolle senden möchten.</span><span class="sxs-lookup"><span data-stu-id="09ffa-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="09ffa-166">Beispiel: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="09ffa-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="09ffa-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09ffa-167">-Confirm</span></span>
<span data-ttu-id="09ffa-168">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09ffa-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ffa-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ffa-169">-WhatIf</span></span>
<span data-ttu-id="09ffa-170">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09ffa-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09ffa-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09ffa-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ffa-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ffa-172">CommonParameters</span></span>
<span data-ttu-id="09ffa-173">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ffa-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ffa-174">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09ffa-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ffa-175">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09ffa-175">INPUTS</span></span>

### <span data-ttu-id="09ffa-176">System.String</span><span class="sxs-lookup"><span data-stu-id="09ffa-176">System.String</span></span>

### <span data-ttu-id="09ffa-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="09ffa-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="09ffa-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="09ffa-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="09ffa-179">System.Guid</span><span class="sxs-lookup"><span data-stu-id="09ffa-179">System.Guid</span></span>

### <span data-ttu-id="09ffa-180">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09ffa-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="09ffa-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="09ffa-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="09ffa-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09ffa-182">OUTPUTS</span></span>

### <span data-ttu-id="09ffa-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="09ffa-183">System.Boolean</span></span>

## <span data-ttu-id="09ffa-184">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="09ffa-184">NOTES</span></span>

## <span data-ttu-id="09ffa-185">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="09ffa-185">RELATED LINKS</span></span>
