---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: e9d3e7ca009a756526bc0cb150ebdb6c124df032
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825827"
---
# <span data-ttu-id="9011d-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="9011d-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="9011d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9011d-102">SYNOPSIS</span></span>
<span data-ttu-id="9011d-103">**Wichtig: Dieses Cmdlet ist veraltet, wenn Sie von [AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) ersetzt werden.**</span><span class="sxs-lookup"><span data-stu-id="9011d-103">**Important: This cmdlet is deprecated, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="9011d-104">Ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9011d-104">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="9011d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9011d-105">SYNTAX</span></span>

### <span data-ttu-id="9011d-106">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9011d-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9011d-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="9011d-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9011d-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="9011d-108">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9011d-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="9011d-109">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9011d-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="9011d-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9011d-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="9011d-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9011d-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="9011d-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9011d-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="9011d-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9011d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9011d-114">DESCRIPTION</span></span>
<span data-ttu-id="9011d-115">Das Cmdlet " **Satz-AzSqlServerAuditing** " ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9011d-115">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="9011d-116">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* und Server *Name* , um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9011d-116">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="9011d-117">Das Ziel der Überwachungsprotokolle wird bestimmt, indem Sie einen der folgenden Switch-Parameter angeben: BlobStorage, LogAnalytics oder EventHub (wenn keine angegeben ist, ist der Standardwert BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="9011d-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="9011d-118">Verwenden Sie den *State* -Parameter, um die Richtlinie zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9011d-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="9011d-119">Wenn das Überwachungsprotokoll Ziel BLOB-Speicher ist, geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter zum Definieren der Speicherschlüssel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9011d-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="9011d-120">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9011d-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="9011d-121">Wenn das Cmdlet erfolgreich ist und Sie den *passthru* -Parameter verwenden, gibt es ein Objekt zurück, das die aktuellen Überwachungseinstellungen zusätzlich zu den Server-IDs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9011d-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="9011d-122">Server-IDs beinhalten, sind aber nicht auf **ResourceGroupName** und Server **Name** limitiert.</span><span class="sxs-lookup"><span data-stu-id="9011d-122">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="9011d-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9011d-123">EXAMPLES</span></span>

### <span data-ttu-id="9011d-124">Beispiel 1: Aktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9011d-124">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="9011d-125">Beispiel 2: Deaktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9011d-125">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="9011d-126">Beispiel 3: Aktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL-Servers unter Verwendung eines speicherkontos aus einem anderen Abonnement</span><span class="sxs-lookup"><span data-stu-id="9011d-126">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="9011d-127">Beispiel 4: Aktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL Server mit erweiterter Filterung mithilfe eines T-SQL-Prädikats</span><span class="sxs-lookup"><span data-stu-id="9011d-127">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="9011d-128">Beispiel 5: Entfernen der erweiterten Filtereinstellung aus der BLOB-Überwachungsspeicher Richtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9011d-128">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="9011d-129">Beispiel 6: Aktivieren der Ereignis-Hub-Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9011d-129">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
$EventHubAuthorizationRule = Get-AzEventHubAuthorizationRule `
    -ResourceGroupName "ResourceGroup01" `
    -Namespace "EventHubName" `
    -Name "SharedAccessPoliceName" 

Set-AzSqlServerAuditing `
    -State Enabled `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -EventHub `
    -EventHubName "EventHubName" `
    -EventHubAuthorizationRuleResourceId $EventHubAuthorizationRule.Id
```

### <span data-ttu-id="9011d-130">Beispiel 7: Deaktivieren der Ereignis-Hub-Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9011d-130">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="9011d-131">Beispiel 8: Aktivieren der Überwachungsrichtlinie für die Protokollanalyse eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9011d-131">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="9011d-132">Beispiel 9: Deaktivieren der Überwachungsrichtlinie für die Protokollanalyse eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9011d-132">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="9011d-133">Beispiel 10: Deaktivieren Sie die Protokollanalyse-Überwachungsrichtlinie eines Azure SQL Server durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9011d-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="9011d-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="9011d-134">PARAMETERS</span></span>

### <span data-ttu-id="9011d-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9011d-135">-AsJob</span></span>
<span data-ttu-id="9011d-136">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9011d-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9011d-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="9011d-137">-AuditActionGroup</span></span>
<span data-ttu-id="9011d-138">Die empfohlene Gruppe der zu verwendenden Aktionsgruppen ist die folgende Kombination, die alle Abfragen und gespeicherten Prozeduren überprüft, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="9011d-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="9011d-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="9011d-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="9011d-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="9011d-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="9011d-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="9011d-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="9011d-142">Diese obige Kombination ist auch die standardmäßig konfigurierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9011d-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="9011d-143">Diese Gruppen decken alle SQL-Anweisungen und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Verbindung mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="9011d-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="9011d-144">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="9011d-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="9011d-145">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="9011d-145">-BlobStorage</span></span>
<span data-ttu-id="9011d-146">Gibt an, dass das Überwachungsprotokoll Ziel BLOB-Speicher ist</span><span class="sxs-lookup"><span data-stu-id="9011d-146">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="9011d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9011d-147">-DefaultProfile</span></span>
<span data-ttu-id="9011d-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9011d-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9011d-149">-EventHub</span><span class="sxs-lookup"><span data-stu-id="9011d-149">-EventHub</span></span>
<span data-ttu-id="9011d-150">Gibt an, dass das Überwachungsprotokoll Zielereignis-Hub ist</span><span class="sxs-lookup"><span data-stu-id="9011d-150">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="9011d-151">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="9011d-151">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="9011d-152">Die Ressourcen-ID für die Ereignis-Hub-Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="9011d-152">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="9011d-153">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="9011d-153">-EventHubName</span></span>
<span data-ttu-id="9011d-154">Der Name des Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="9011d-154">The name of the event hub.</span></span> <span data-ttu-id="9011d-155">Wenn beim Bereitstellen von EventHubAuthorizationRuleResourceId keine angegeben wird, wird der Standardereignis-Hub ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9011d-155">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="9011d-156">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9011d-156">-InputObject</span></span>
<span data-ttu-id="9011d-157">Das Serverobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9011d-157">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9011d-158">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="9011d-158">-LogAnalytics</span></span>
<span data-ttu-id="9011d-159">Gibt an, dass die Überwachungsprotokolle Zielprotokoll Analyse sind.</span><span class="sxs-lookup"><span data-stu-id="9011d-159">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="9011d-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9011d-160">-PassThru</span></span>
<span data-ttu-id="9011d-161">Gibt an, ob die Überwachungsrichtlinie am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9011d-161">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9011d-162">-Prädikat</span><span class="sxs-lookup"><span data-stu-id="9011d-162">-PredicateExpression</span></span>
<span data-ttu-id="9011d-163">Das T-SQL-Prädikat (WHERE-Klausel), das zum Filtern von Überwachungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9011d-163">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="9011d-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9011d-164">-ResourceGroupName</span></span>
<span data-ttu-id="9011d-165">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9011d-165">The name of the resource group.</span></span>

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

### <span data-ttu-id="9011d-166">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9011d-166">-RetentionInDays</span></span>
<span data-ttu-id="9011d-167">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="9011d-167">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="9011d-168">-Servername</span><span class="sxs-lookup"><span data-stu-id="9011d-168">-ServerName</span></span>
<span data-ttu-id="9011d-169">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="9011d-169">SQL server name.</span></span>

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

### <span data-ttu-id="9011d-170">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="9011d-170">-State</span></span>
<span data-ttu-id="9011d-171">Der Zustand der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9011d-171">The state of the policy.</span></span>

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

### <span data-ttu-id="9011d-172">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9011d-172">-StorageAccountName</span></span>
<span data-ttu-id="9011d-173">Der Name des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="9011d-173">The name of the storage account.</span></span>

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

### <span data-ttu-id="9011d-174">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9011d-174">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="9011d-175">Die Abonnement-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="9011d-175">The storage account subscription id</span></span>

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

### <span data-ttu-id="9011d-176">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="9011d-176">-StorageKeyType</span></span>
<span data-ttu-id="9011d-177">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9011d-177">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="9011d-178">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="9011d-178">-WorkspaceResourceId</span></span>
<span data-ttu-id="9011d-179">Die Arbeitsbereichs-ID (Ressourcen-ID eines Protokollanalyse Arbeitsbereichs) für einen Protokollanalyse Arbeitsbereich, an den Sie Überwachungsprotokolle senden möchten.</span><span class="sxs-lookup"><span data-stu-id="9011d-179">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="9011d-180">Beispiel:/Subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/Insights-Integration/Providers/Microsoft.OperationalInsights/Workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="9011d-180">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="9011d-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9011d-181">-Confirm</span></span>
<span data-ttu-id="9011d-182">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9011d-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9011d-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9011d-183">-WhatIf</span></span>
<span data-ttu-id="9011d-184">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9011d-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9011d-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9011d-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9011d-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9011d-186">CommonParameters</span></span>
<span data-ttu-id="9011d-187">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9011d-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9011d-188">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9011d-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9011d-189">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9011d-189">INPUTS</span></span>

### <span data-ttu-id="9011d-190">System. String</span><span class="sxs-lookup"><span data-stu-id="9011d-190">System.String</span></span>

### <span data-ttu-id="9011d-191">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="9011d-191">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="9011d-192">Microsoft. Azure. Commands. SQL. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="9011d-192">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="9011d-193">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="9011d-193">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9011d-194">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9011d-194">System.Guid</span></span>

### <span data-ttu-id="9011d-195">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9011d-195">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9011d-196">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9011d-196">OUTPUTS</span></span>

### <span data-ttu-id="9011d-197">Microsoft. Azure. Commands. SQL. Auditing. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="9011d-197">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="9011d-198">Notizen</span><span class="sxs-lookup"><span data-stu-id="9011d-198">NOTES</span></span>

## <span data-ttu-id="9011d-199">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9011d-199">RELATED LINKS</span></span>
