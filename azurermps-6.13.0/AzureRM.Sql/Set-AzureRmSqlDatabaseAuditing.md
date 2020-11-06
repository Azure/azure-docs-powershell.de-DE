---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479434"
---
# <span data-ttu-id="688a0-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="688a0-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="688a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="688a0-102">SYNOPSIS</span></span>
<span data-ttu-id="688a0-103">Ändert die Überwachungseinstellungen für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="688a0-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="688a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="688a0-104">SYNTAX</span></span>

### <span data-ttu-id="688a0-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="688a0-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="688a0-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="688a0-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="688a0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="688a0-107">DESCRIPTION</span></span>
<span data-ttu-id="688a0-108">Das Cmdlet " **Satz-AzureRmSqlDatabaseAuditing** " ändert die Überwachungseinstellungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="688a0-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="688a0-109">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="688a0-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="688a0-110">Geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter anzugeben, um die Speicherschlüssel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="688a0-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="688a0-111">Verwenden Sie den *State* -Parameter, um die Richtlinie zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="688a0-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="688a0-112">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="688a0-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="688a0-113">Nachdem das Cmdlet erfolgreich ausgeführt wurde, ist die Überwachung der Datenbank aktiviert.</span><span class="sxs-lookup"><span data-stu-id="688a0-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="688a0-114">Wenn das Cmdlet erfolgreich ist und Sie den *passthru* -Parameter verwenden, wird zusätzlich zu den Datenbankbezeichnern ein Objekt zurückgegeben, das die aktuelle BLOB-Überwachungsrichtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="688a0-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="688a0-115">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="688a0-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="688a0-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="688a0-116">EXAMPLES</span></span>

### <span data-ttu-id="688a0-117">Beispiel 1: Aktivieren der Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="688a0-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="688a0-118">Beispiel 2: Deaktivieren der BLOB-Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="688a0-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="688a0-119">Beispiel 3: Aktivieren der Überwachungsrichtlinie einer Azure SQL-Datenbank unter Verwendung eines speicherkontos aus einem anderen Abonnement</span><span class="sxs-lookup"><span data-stu-id="688a0-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="688a0-120">Beispiel 4: Aktivieren der erweiterten Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="688a0-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="688a0-121">Beispiel 5: Entfernen Sie die erweiterte Überwachungsrichtlinie einer Azure SQL-Datenbank, und richten Sie stattdessen eine Überwachungsrichtlinie ein.</span><span class="sxs-lookup"><span data-stu-id="688a0-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="688a0-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="688a0-122">PARAMETERS</span></span>

### <span data-ttu-id="688a0-123">-Auditing</span><span class="sxs-lookup"><span data-stu-id="688a0-123">-AuditAction</span></span>
<span data-ttu-id="688a0-124">Die Gruppe von Überwachungsaktionen.</span><span class="sxs-lookup"><span data-stu-id="688a0-124">The set of audit actions.</span></span>
<span data-ttu-id="688a0-125">Die unterstützten Aktionen, die überwacht werden sollen, sind: Wählen Sie Update Einfügen Löschen ausführen von Receive-verweisen das allgemeine Formular zum Definieren einer zu überwachenden Aktion lautet: [Aktion] auf [Objekt] nach [Principal] Beachten Sie, dass [Objekt] im obigen Format auf ein Objekt wie eine Tabelle, eine Ansicht oder eine gespeicherte Prozedur oder eine gesamte Datenbank oder ein ganzes Schema verweisen kann</span><span class="sxs-lookup"><span data-stu-id="688a0-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="688a0-126">In den letzten Fällen werden die Formulare Database:: [DBName] und Schema:: [SchemaName] verwendet.</span><span class="sxs-lookup"><span data-stu-id="688a0-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="688a0-127">Beispiel: Wählen Sie unter dbo. MyTable durch Public Select on Database:: MyDatabase by Public Select on Schema:: MySchema by Public (Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="688a0-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="688a0-128">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="688a0-128">-AuditActionGroup</span></span>
<span data-ttu-id="688a0-129">Die empfohlene Gruppe der zu verwendenden Aktionsgruppen ist die folgende Kombination, die alle Abfragen und gespeicherten Prozeduren überprüft, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" Diese obige Kombination ist auch die standardmäßig konfigurierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="688a0-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="688a0-130">Diese Gruppen decken alle SQL-Anweisungen und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Verbindung mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="688a0-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="688a0-131">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="688a0-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688a0-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="688a0-132">-DatabaseName</span></span>
<span data-ttu-id="688a0-133">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="688a0-133">SQL Database name.</span></span>

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

### <span data-ttu-id="688a0-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="688a0-134">-DefaultProfile</span></span>
<span data-ttu-id="688a0-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="688a0-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="688a0-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="688a0-136">-PassThru</span></span>
<span data-ttu-id="688a0-137">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="688a0-137">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="688a0-138">-Prädikat</span><span class="sxs-lookup"><span data-stu-id="688a0-138">-PredicateExpression</span></span>
<span data-ttu-id="688a0-139">Die Anweisung der WHERE-Klausel, die zum Filtern von Überwachungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="688a0-139">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="688a0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="688a0-140">-ResourceGroupName</span></span>
<span data-ttu-id="688a0-141">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="688a0-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="688a0-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="688a0-142">-RetentionInDays</span></span>
<span data-ttu-id="688a0-143">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="688a0-143">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688a0-144">-Servername</span><span class="sxs-lookup"><span data-stu-id="688a0-144">-ServerName</span></span>
<span data-ttu-id="688a0-145">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="688a0-145">SQL Database server name.</span></span>

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

### <span data-ttu-id="688a0-146">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="688a0-146">-State</span></span>
<span data-ttu-id="688a0-147">Der Zustand der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="688a0-147">The state of the policy.</span></span>

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

### <span data-ttu-id="688a0-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="688a0-148">-StorageAccountName</span></span>
<span data-ttu-id="688a0-149">Der Name des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="688a0-149">The name of the storage account.</span></span> <span data-ttu-id="688a0-150">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="688a0-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="688a0-151">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="688a0-151">This parameter is not required.</span></span>
<span data-ttu-id="688a0-152">Wenn Sie diesen Parameter nicht angeben, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Überwachungsrichtlinie definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="688a0-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="688a0-153">Wenn Sie zum ersten Mal eine Überwachungsrichtlinie definieren und diesen Parameter nicht angeben, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="688a0-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688a0-154">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="688a0-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="688a0-155">Gibt die Abonnement-ID des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="688a0-155">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688a0-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="688a0-156">-StorageKeyType</span></span>
<span data-ttu-id="688a0-157">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="688a0-157">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688a0-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="688a0-158">-Confirm</span></span>
<span data-ttu-id="688a0-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="688a0-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="688a0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="688a0-160">-WhatIf</span></span>
<span data-ttu-id="688a0-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="688a0-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="688a0-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="688a0-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="688a0-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="688a0-163">CommonParameters</span></span>
<span data-ttu-id="688a0-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="688a0-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="688a0-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="688a0-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="688a0-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="688a0-166">INPUTS</span></span>

## <span data-ttu-id="688a0-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="688a0-167">OUTPUTS</span></span>

## <span data-ttu-id="688a0-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="688a0-168">NOTES</span></span>

## <span data-ttu-id="688a0-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="688a0-169">RELATED LINKS</span></span>
