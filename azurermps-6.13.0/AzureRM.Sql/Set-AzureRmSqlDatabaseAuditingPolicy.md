---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a9f0f2e478e94b45349efe85c6de643b5003a361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479430"
---
# <span data-ttu-id="27572-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="27572-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="27572-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27572-102">SYNOPSIS</span></span>
<span data-ttu-id="27572-103">Legt die Überwachungsrichtlinie für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="27572-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27572-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27572-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27572-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27572-105">DESCRIPTION</span></span>
<span data-ttu-id="27572-106">Das Cmdlet " **Satz-AzureRmSqlDatabaseAuditingPolicy** " ändert die Überwachungsrichtlinie einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="27572-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="27572-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="27572-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="27572-108">Geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter anzugeben, um die Speicherschlüssel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="27572-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="27572-109">Sie können auch die Aufbewahrung für die Überwachungsprotokolltabelle definieren, indem Sie den Wert der *RetentionInDays* -und Table *Identifier* -Parameter festlegen, um den Zeitraum und den Startwert für die Namen der Überwachungsprotokoll Tabellen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="27572-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="27572-110">Geben Sie den *eventType* -Parameter an, um die zu überwachenden Ereignistypen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="27572-110">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="27572-111">Nachdem das Cmdlet erfolgreich ausgeführt wurde, ist die Überwachung der Datenbank aktiviert.</span><span class="sxs-lookup"><span data-stu-id="27572-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="27572-112">Wenn die Datenbank für die Tabellen Überwachung die Richtlinie Ihres Servers für die Überwachung verwendet hat, bevor Sie dieses Cmdlet ausgeführt haben, wird die Überwachung nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="27572-112">For Table Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span> <span data-ttu-id="27572-113">Wenn die Datenbank bei der BLOB-Überwachung die Richtlinie Ihres Servers für die Überwachung verwendet hat, bevor Sie dieses Cmdlet ausgeführt haben, sind beide Überwachungsrichtlinien nebeneinander vorhanden.</span><span class="sxs-lookup"><span data-stu-id="27572-113">For Blob Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, both auditing policies will exist side-by-side.</span></span>
<span data-ttu-id="27572-114">Wenn das Cmdlet erfolgreich ist und Sie den *passthru* -Parameter verwenden, gibt es zusätzlich zu den Datenbankbezeichnern ein Objekt zurück, das die aktuelle Überwachungsrichtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="27572-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="27572-115">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="27572-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="27572-116">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27572-116">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="27572-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27572-117">EXAMPLES</span></span>

### <span data-ttu-id="27572-118">Beispiel 1: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung der Tabellen Überwachung</span><span class="sxs-lookup"><span data-stu-id="27572-118">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="27572-119">Mit diesem Befehl wird die Überwachungsrichtlinie der Datenbank mit dem Namen Database01 auf Server01 festgelegt, um das Speicherkonto mit dem Namen Storage31 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="27572-119">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="27572-120">Beispiel 2: Festlegen des Speicherkonto Schlüssels einer vorhandenen Überwachungsrichtlinie einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="27572-120">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="27572-121">Mit diesem Befehl wird die Überwachungsrichtlinie der Datenbank mit dem Namen Database01 auf Server01 festgelegt, damit derselbe Speicherkonto Name verwendet wird, aber jetzt der sekundäre Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27572-121">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="27572-122">Beispiel 3: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung eines bestimmten Ereignistyps</span><span class="sxs-lookup"><span data-stu-id="27572-122">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="27572-123">Beispiel 4: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung der BLOB-Überwachung</span><span class="sxs-lookup"><span data-stu-id="27572-123">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="27572-124">Dieser Befehl legt die Überwachungsrichtlinie der Datenbank mit dem Namen Database01 auf Server01 fest.</span><span class="sxs-lookup"><span data-stu-id="27572-124">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="27572-125">Die Richtlinie protokolliert den Login_Failure-Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="27572-125">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="27572-126">Der Befehl ändert keine Speichereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="27572-126">The command does not change the storage settings.</span></span>

## <span data-ttu-id="27572-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="27572-127">PARAMETERS</span></span>

### <span data-ttu-id="27572-128">-Auditing</span><span class="sxs-lookup"><span data-stu-id="27572-128">-AuditAction</span></span>
<span data-ttu-id="27572-129">Geben Sie mindestens eine Überwachungsaktion an.</span><span class="sxs-lookup"><span data-stu-id="27572-129">Specify one or more audit actions.</span></span>
<span data-ttu-id="27572-130">Dieser Parameter gilt nur für die BLOB-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="27572-130">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="27572-131">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="27572-131">-AuditActionGroup</span></span>
<span data-ttu-id="27572-132">Geben Sie mindestens eine Überwachungs Aktionsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="27572-132">Specify one or more audit action groups.</span></span>
<span data-ttu-id="27572-133">Dieser Parameter gilt nur für die BLOB-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="27572-133">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="27572-134">-Audittype</span><span class="sxs-lookup"><span data-stu-id="27572-134">-AuditType</span></span>
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27572-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27572-135">-DatabaseName</span></span>
<span data-ttu-id="27572-136">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="27572-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="27572-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27572-137">-DefaultProfile</span></span>
<span data-ttu-id="27572-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="27572-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27572-139">-EventType</span><span class="sxs-lookup"><span data-stu-id="27572-139">-EventType</span></span>
<span data-ttu-id="27572-140">Gibt die zu überwachenden Ereignistypen an.</span><span class="sxs-lookup"><span data-stu-id="27572-140">Specifies the event types to audit.</span></span>
<span data-ttu-id="27572-141">Dieser Parameter gilt nur für die Tabellen Überwachung.</span><span class="sxs-lookup"><span data-stu-id="27572-141">This parameter is only applicable to Table auditing.</span></span>
<span data-ttu-id="27572-142">Sie können mehrere Ereignistypen angeben.</span><span class="sxs-lookup"><span data-stu-id="27572-142">You can specify several event types.</span></span>
<span data-ttu-id="27572-143">Sie können alle angeben, um alle Ereignistypen oder None zu überwachen, um anzugeben, dass keine Ereignisse überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="27572-143">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="27572-144">Wenn Sie alle oder keine gleichzeitig angeben, wird das Cmdlet nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27572-144">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27572-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27572-145">-PassThru</span></span>
<span data-ttu-id="27572-146">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="27572-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="27572-147">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="27572-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="27572-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27572-148">-ResourceGroupName</span></span>
<span data-ttu-id="27572-149">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="27572-149">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="27572-150">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="27572-150">-RetentionInDays</span></span>
<span data-ttu-id="27572-151">Gibt die Anzahl der Aufbewahrungstage für die Überwachungsprotokolltabelle an.</span><span class="sxs-lookup"><span data-stu-id="27572-151">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="27572-152">Der Wert 0 (null) bedeutet, dass die Tabelle nicht beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="27572-152">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="27572-153">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="27572-153">The default value is zero.</span></span>
<span data-ttu-id="27572-154">Wenn Sie einen Wert angeben, der größer als 0 (null) ist, müssen Sie einen Wert für den *TableIdentifer* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="27572-154">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="27572-155">-Servername</span><span class="sxs-lookup"><span data-stu-id="27572-155">-ServerName</span></span>
<span data-ttu-id="27572-156">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="27572-156">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="27572-157">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="27572-157">-StorageAccountName</span></span>
<span data-ttu-id="27572-158">Gibt den Namen des speicherkontos für die Überwachung der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="27572-158">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="27572-159">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="27572-159">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="27572-160">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="27572-160">This parameter is not required.</span></span>
<span data-ttu-id="27572-161">Wenn Sie diesen Parameter nicht angeben, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Überwachungsrichtlinie der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="27572-161">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="27572-162">Wenn Sie zum ersten Mal eine Datenbank-Überwachungsrichtlinie definieren und diesen Parameter nicht angeben, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="27572-162">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="27572-163">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="27572-163">-StorageKeyType</span></span>
<span data-ttu-id="27572-164">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="27572-164">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="27572-165">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="27572-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27572-166">Primär</span><span class="sxs-lookup"><span data-stu-id="27572-166">Primary</span></span>
- <span data-ttu-id="27572-167">Sekundär der Standardwert ist Primary.</span><span class="sxs-lookup"><span data-stu-id="27572-167">Secondary The default value is Primary.</span></span>

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

### <span data-ttu-id="27572-168">-Tabellenidentifier</span><span class="sxs-lookup"><span data-stu-id="27572-168">-TableIdentifier</span></span>
<span data-ttu-id="27572-169">Gibt den Namen der Überwachungsprotokolltabelle an.</span><span class="sxs-lookup"><span data-stu-id="27572-169">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="27572-170">Geben Sie diesen Wert an, wenn Sie für den *RetentionInDays* -Parameter einen Wert größer als 0 angeben.</span><span class="sxs-lookup"><span data-stu-id="27572-170">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="27572-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27572-171">-Confirm</span></span>
<span data-ttu-id="27572-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27572-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27572-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27572-173">-WhatIf</span></span>
<span data-ttu-id="27572-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27572-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27572-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27572-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27572-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27572-176">CommonParameters</span></span>
<span data-ttu-id="27572-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27572-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27572-178">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27572-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27572-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27572-179">INPUTS</span></span>

### <span data-ttu-id="27572-180">Microsoft. Azure. Commands. SQL. Auditing. Model. audittype</span><span class="sxs-lookup"><span data-stu-id="27572-180">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType</span></span>

### <span data-ttu-id="27572-181">Microsoft. Azure. Commands. SQL. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="27572-181">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="27572-182">System. String []</span><span class="sxs-lookup"><span data-stu-id="27572-182">System.String[]</span></span>

### <span data-ttu-id="27572-183">System. String</span><span class="sxs-lookup"><span data-stu-id="27572-183">System.String</span></span>

### <span data-ttu-id="27572-184">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="27572-184">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="27572-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27572-185">OUTPUTS</span></span>

### <span data-ttu-id="27572-186">Microsoft. Azure. Commands. SQL. Auditing. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="27572-186">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="27572-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="27572-187">NOTES</span></span>

## <span data-ttu-id="27572-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27572-188">RELATED LINKS</span></span>

[<span data-ttu-id="27572-189">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="27572-189">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="27572-190">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="27572-190">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="27572-191">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="27572-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


