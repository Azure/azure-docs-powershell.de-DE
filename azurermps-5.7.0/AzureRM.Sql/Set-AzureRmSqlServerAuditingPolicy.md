---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: ee54928b1f32c726bc2847eace77e6ccbe48c4d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482673"
---
# <span data-ttu-id="f84cd-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f84cd-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="f84cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f84cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f84cd-103">Ändert die Überwachungsrichtlinie eines SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="f84cd-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f84cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f84cd-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f84cd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f84cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f84cd-106">Das Cmdlet " **Satz-AzureRmSqlServerAuditingPolicy** " ändert die Überwachungsrichtlinie eines Azure SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="f84cd-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="f84cd-107">Geben Sie die Parameter *ResourceGroupName* und *Servername* an, um den Server zu identifizieren, den *StorageAccountName* -Parameter, um das Speicherkonto für die Überwachungsprotokolle anzugeben, und den *StorageKeyType* -Parameter, um die zu verwendenden Speicherschlüssel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f84cd-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>

<span data-ttu-id="f84cd-108">Sie können auch die Aufbewahrung für die Überwachungsprotokolltabelle definieren, indem Sie den Wert der *RetentionInDays* -und Table *Identifier* -Parameter festlegen, um den Zeitraum und den Startwert für die Namen der Überwachungsprotokoll Tabellen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f84cd-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="f84cd-109">Geben Sie den *eventType* -Parameter an, um die zu überwachenden Ereignistypen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f84cd-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="f84cd-110">Nachdem Sie dieses Cmdlet ausgeführt haben, ist die Überwachung der Datenbanken, die die Richtlinie dieses Servers verwenden, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f84cd-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="f84cd-111">Wenn das Cmdlet erfolgreich ausgeführt wird und Sie den *passthru* -Parameter angeben, gibt das Cmdlet ein Objekt zurück, das die aktuelle Überwachungsrichtlinie beschreibt, und die Server-IDs.</span><span class="sxs-lookup"><span data-stu-id="f84cd-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="f84cd-112">Server-IDs sind **ResourceGroupName** und Server **Name**.</span><span class="sxs-lookup"><span data-stu-id="f84cd-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="f84cd-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f84cd-113">EXAMPLES</span></span>

### <span data-ttu-id="f84cd-114">Beispiel 1: Festlegen der Überwachungsrichtlinie einer Azure SQL Server-Tabellen Überwachung verwenden</span><span class="sxs-lookup"><span data-stu-id="f84cd-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="f84cd-115">Mit diesem Befehl wird die Überwachungsrichtlinie des Servers mit dem Namen Server01 für die Verwendung eines speicherkontos mit dem Namen Storage22 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f84cd-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="f84cd-116">Beispiel 2: Festlegen des Speicherkonto Schlüssels einer vorhandenen Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f84cd-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="f84cd-117">Mit diesem Befehl wird die Überwachungsrichtlinie des Servers mit dem Namen Server01 so festgelegt, dass der sekundäre Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f84cd-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="f84cd-118">Der Befehl ändert den Namen des speicherkontos nicht.</span><span class="sxs-lookup"><span data-stu-id="f84cd-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="f84cd-119">Beispiel 3: Festlegen der Überwachungsrichtlinie eines Azure SQL Server für die Verwendung eines bestimmten Ereignistyps</span><span class="sxs-lookup"><span data-stu-id="f84cd-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="f84cd-120">Beispiel 4: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung der BLOB-Überwachung</span><span class="sxs-lookup"><span data-stu-id="f84cd-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="f84cd-121">Mit diesem Befehl wird die Überwachungsrichtlinie des Servers mit dem Namen Server01 für die Verwendung des Login_Failure-Ereignistyps festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f84cd-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="f84cd-122">Mit diesem Befehl werden keine anderen Einstellungen geändert.</span><span class="sxs-lookup"><span data-stu-id="f84cd-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="f84cd-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="f84cd-123">PARAMETERS</span></span>

### <span data-ttu-id="f84cd-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f84cd-124">-AuditActionGroup</span></span>
<span data-ttu-id="f84cd-125">Geben Sie mindestens eine Überwachungs Aktionsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="f84cd-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="f84cd-126">Dieser Parameter gilt nur für die BLOB-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="f84cd-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="f84cd-127">-Audittype</span><span class="sxs-lookup"><span data-stu-id="f84cd-127">-AuditType</span></span>
<span data-ttu-id="f84cd-128">Geben Sie den Überwachungstyp an.</span><span class="sxs-lookup"><span data-stu-id="f84cd-128">Specify the audit type.</span></span> <span data-ttu-id="f84cd-129">Überwachungsprotokolle können in den Tabellenspeicher oder BLOB-Speicher geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f84cd-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="f84cd-130">Die BLOB-Überwachung bietet eine höhere Leistung und unterstützt die Überwachung auf Objektebene.</span><span class="sxs-lookup"><span data-stu-id="f84cd-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

```yaml
Type: AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84cd-131">-DefaultProfile</span></span>
<span data-ttu-id="f84cd-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f84cd-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f84cd-133">-EventType</span><span class="sxs-lookup"><span data-stu-id="f84cd-133">-EventType</span></span>
<span data-ttu-id="f84cd-134">Gibt die zu überwachenden Ereignistypen an.</span><span class="sxs-lookup"><span data-stu-id="f84cd-134">Specifies the event types to audit.</span></span>
<span data-ttu-id="f84cd-135">Dieser Parameter gilt nur für die Tabellen Überwachung.</span><span class="sxs-lookup"><span data-stu-id="f84cd-135">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="f84cd-136">Sie können mehrere Ereignistypen angeben.</span><span class="sxs-lookup"><span data-stu-id="f84cd-136">You can specify several event types.</span></span>
<span data-ttu-id="f84cd-137">Sie können alle angeben, um alle Ereignistypen oder None zu überwachen, um anzugeben, dass keine Ereignisse überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="f84cd-137">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="f84cd-138">Wenn Sie alle oder keine gleichzeitig angeben, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="f84cd-138">If you specify All or None at the same time, the command fails.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f84cd-139">-PassThru</span></span>
<span data-ttu-id="f84cd-140">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f84cd-140">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f84cd-141">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f84cd-141">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f84cd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84cd-142">-ResourceGroupName</span></span>
<span data-ttu-id="f84cd-143">Gibt den Namen der Ressourcengruppe an, die die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="f84cd-143">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="f84cd-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f84cd-144">-RetentionInDays</span></span>
<span data-ttu-id="f84cd-145">Gibt die Anzahl der Aufbewahrungstage für die Überwachungsprotokolltabelle an.</span><span class="sxs-lookup"><span data-stu-id="f84cd-145">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="f84cd-146">Der Wert 0 (null) bedeutet, dass die Tabelle nicht beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="f84cd-146">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="f84cd-147">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="f84cd-147">this is the default.</span></span>
<span data-ttu-id="f84cd-148">Wenn Sie einen Wert angeben, der größer als 0 (null) ist, müssen Sie auch einen Wert für den *TableIdentifer* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f84cd-148">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="f84cd-149">-Servername</span><span class="sxs-lookup"><span data-stu-id="f84cd-149">-ServerName</span></span>
<span data-ttu-id="f84cd-150">Gibt den Namen des Servers an, der die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="f84cd-150">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f84cd-151">-StorageAccountName</span></span>
<span data-ttu-id="f84cd-152">Gibt den Namen des speicherkontos für die Überwachung der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="f84cd-152">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="f84cd-153">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="f84cd-153">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="f84cd-154">Wenn Sie diesen Parameter nicht angeben, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Überwachungsrichtlinie der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f84cd-154">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="f84cd-155">Wenn dies das erste Mal ist, dass eine Datenbank-Überwachungsrichtlinie definiert ist und Sie diesen Parameter nicht angeben, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="f84cd-155">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="f84cd-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f84cd-156">-StorageKeyType</span></span>
<span data-ttu-id="f84cd-157">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f84cd-157">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="f84cd-158">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f84cd-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f84cd-159">Primär</span><span class="sxs-lookup"><span data-stu-id="f84cd-159">Primary</span></span>
- <span data-ttu-id="f84cd-160">Sekundär</span><span class="sxs-lookup"><span data-stu-id="f84cd-160">Secondary</span></span>

<span data-ttu-id="f84cd-161">Der Standardwert ist Primary.</span><span class="sxs-lookup"><span data-stu-id="f84cd-161">The default value is Primary.</span></span>

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

### <span data-ttu-id="f84cd-162">-Tabellenidentifier</span><span class="sxs-lookup"><span data-stu-id="f84cd-162">-TableIdentifier</span></span>
<span data-ttu-id="f84cd-163">Gibt den Namen der Überwachungsprotokolltabelle an.</span><span class="sxs-lookup"><span data-stu-id="f84cd-163">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="f84cd-164">Geben Sie diesen Wert an, wenn Sie für den *RetentionInDays* -Parameter einen Wert größer als 0 angeben.</span><span class="sxs-lookup"><span data-stu-id="f84cd-164">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="f84cd-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f84cd-165">-Confirm</span></span>
<span data-ttu-id="f84cd-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f84cd-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f84cd-167">-WhatIf</span></span>
<span data-ttu-id="f84cd-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f84cd-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f84cd-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f84cd-169">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84cd-170">CommonParameters</span></span>
<span data-ttu-id="f84cd-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84cd-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84cd-172">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f84cd-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84cd-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f84cd-173">INPUTS</span></span>

### <span data-ttu-id="f84cd-174">Keine</span><span class="sxs-lookup"><span data-stu-id="f84cd-174">None</span></span>
<span data-ttu-id="f84cd-175">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f84cd-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f84cd-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f84cd-176">OUTPUTS</span></span>

### <span data-ttu-id="f84cd-177">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f84cd-177">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="f84cd-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="f84cd-178">NOTES</span></span>

## <span data-ttu-id="f84cd-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f84cd-179">RELATED LINKS</span></span>

[<span data-ttu-id="f84cd-180">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f84cd-180">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="f84cd-181">Verwenden von-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f84cd-181">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="f84cd-182">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f84cd-182">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


