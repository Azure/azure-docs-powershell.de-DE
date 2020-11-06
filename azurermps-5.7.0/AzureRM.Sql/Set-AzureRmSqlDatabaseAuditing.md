---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480794"
---
# <span data-ttu-id="47040-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="47040-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="47040-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47040-102">SYNOPSIS</span></span>
<span data-ttu-id="47040-103">Ändert die Überwachungseinstellungen für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="47040-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47040-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47040-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47040-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47040-105">DESCRIPTION</span></span>
<span data-ttu-id="47040-106">Das Cmdlet " **Satz-AzureRmSqlDatabaseAuditing** " ändert die Überwachungseinstellungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="47040-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="47040-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="47040-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="47040-108">Geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter anzugeben, um die Speicherschlüssel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="47040-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="47040-109">Verwenden Sie den *State* -Parameter, um die Richtlinie zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="47040-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="47040-110">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="47040-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="47040-111">Nachdem das Cmdlet erfolgreich ausgeführt wurde, ist die Überwachung der Datenbank aktiviert.</span><span class="sxs-lookup"><span data-stu-id="47040-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="47040-112">Wenn das Cmdlet erfolgreich ist und Sie den *passthru* -Parameter verwenden, wird zusätzlich zu den Datenbankbezeichnern ein Objekt zurückgegeben, das die aktuelle BLOB-Überwachungsrichtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="47040-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="47040-113">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="47040-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="47040-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47040-114">EXAMPLES</span></span>

### <span data-ttu-id="47040-115">Beispiel 1: Aktivieren der Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="47040-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="47040-116">Beispiel 2: Deaktivieren der BLOB-Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="47040-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="47040-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="47040-117">PARAMETERS</span></span>

### <span data-ttu-id="47040-118">-Auditing</span><span class="sxs-lookup"><span data-stu-id="47040-118">-AuditAction</span></span>
<span data-ttu-id="47040-119">Die Gruppe von Überwachungsaktionen.</span><span class="sxs-lookup"><span data-stu-id="47040-119">The set of audit actions.</span></span>  
<span data-ttu-id="47040-120">Die unterstützten zu überwachenden Aktionen sind:</span><span class="sxs-lookup"><span data-stu-id="47040-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="47040-121">Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="47040-121">SELECT</span></span>  
<span data-ttu-id="47040-122">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="47040-122">UPDATE</span></span>  
<span data-ttu-id="47040-123">Einfügen</span><span class="sxs-lookup"><span data-stu-id="47040-123">INSERT</span></span>  
<span data-ttu-id="47040-124">Löschen</span><span class="sxs-lookup"><span data-stu-id="47040-124">DELETE</span></span>  
<span data-ttu-id="47040-125">Ausführen</span><span class="sxs-lookup"><span data-stu-id="47040-125">EXECUTE</span></span>  
<span data-ttu-id="47040-126">Erhalten</span><span class="sxs-lookup"><span data-stu-id="47040-126">RECEIVE</span></span>  
<span data-ttu-id="47040-127">Referenzen</span><span class="sxs-lookup"><span data-stu-id="47040-127">REFERENCES</span></span>  

<span data-ttu-id="47040-128">Das allgemeine Formular zum Definieren einer zu überwachenden Aktion lautet:</span><span class="sxs-lookup"><span data-stu-id="47040-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="47040-129">Aktion Auf [Objekt] nach [Principal]</span><span class="sxs-lookup"><span data-stu-id="47040-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="47040-130">Beachten Sie, dass [Objekt] im obigen Format auf ein Objekt wie eine Tabelle, eine Sicht oder eine gespeicherte Prozedur oder auf eine gesamte Datenbank oder ein ganzes Schema verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="47040-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="47040-131">In den letzten Fällen werden die Formulare Database:: [DBName] und Schema:: [SchemaName] verwendet.</span><span class="sxs-lookup"><span data-stu-id="47040-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="47040-132">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="47040-132">For example:</span></span>  
<span data-ttu-id="47040-133">Auswählen von "dbo. MyTable" nach öffentlichem</span><span class="sxs-lookup"><span data-stu-id="47040-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="47040-134">Wählen Sie in Database:: MyDatabase by Public aus.</span><span class="sxs-lookup"><span data-stu-id="47040-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="47040-135">Wählen Sie auf Schema:: MySchema nach öffentlichen</span><span class="sxs-lookup"><span data-stu-id="47040-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="47040-136">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="47040-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47040-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="47040-137">-AuditActionGroup</span></span>
<span data-ttu-id="47040-138">Die empfohlene Gruppe der zu verwendenden Aktionsgruppen ist die folgende Kombination, die alle Abfragen und gespeicherten Prozeduren überprüft, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="47040-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="47040-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="47040-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="47040-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="47040-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="47040-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="47040-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="47040-142">Diese obige Kombination ist auch die standardmäßig konfigurierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="47040-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="47040-143">Diese Gruppen decken alle SQL-Anweisungen und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Verbindung mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="47040-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="47040-144">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="47040-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47040-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47040-145">-DatabaseName</span></span>
<span data-ttu-id="47040-146">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="47040-146">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47040-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47040-147">-DefaultProfile</span></span>
<span data-ttu-id="47040-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47040-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47040-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47040-149">-PassThru</span></span>
<span data-ttu-id="47040-150">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="47040-150">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47040-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47040-151">-ResourceGroupName</span></span>
<span data-ttu-id="47040-152">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="47040-152">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47040-153">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="47040-153">-RetentionInDays</span></span>
<span data-ttu-id="47040-154">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="47040-154">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47040-155">-Servername</span><span class="sxs-lookup"><span data-stu-id="47040-155">-ServerName</span></span>
<span data-ttu-id="47040-156">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="47040-156">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47040-157">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="47040-157">-State</span></span>
<span data-ttu-id="47040-158">Der Zustand der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="47040-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47040-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="47040-159">-StorageAccountName</span></span>
<span data-ttu-id="47040-160">Der Name des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="47040-160">The name of the storage account.</span></span> <span data-ttu-id="47040-161">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="47040-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="47040-162">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47040-162">This parameter is not required.</span></span>  
<span data-ttu-id="47040-163">Wenn Sie diesen Parameter nicht angeben, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Überwachungsrichtlinie definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="47040-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="47040-164">Wenn Sie zum ersten Mal eine Überwachungsrichtlinie definieren und diesen Parameter nicht angeben, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="47040-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47040-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="47040-165">-StorageKeyType</span></span>
<span data-ttu-id="47040-166">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47040-166">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47040-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47040-167">-Confirm</span></span>
<span data-ttu-id="47040-168">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47040-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47040-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47040-169">-WhatIf</span></span>
<span data-ttu-id="47040-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47040-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47040-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47040-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47040-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47040-172">CommonParameters</span></span>
<span data-ttu-id="47040-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47040-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47040-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47040-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47040-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47040-175">INPUTS</span></span>

### <span data-ttu-id="47040-176">Keine</span><span class="sxs-lookup"><span data-stu-id="47040-176">None</span></span>
<span data-ttu-id="47040-177">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="47040-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47040-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47040-178">OUTPUTS</span></span>

### <span data-ttu-id="47040-179">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="47040-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="47040-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="47040-180">NOTES</span></span>

## <span data-ttu-id="47040-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47040-181">RELATED LINKS</span></span>
