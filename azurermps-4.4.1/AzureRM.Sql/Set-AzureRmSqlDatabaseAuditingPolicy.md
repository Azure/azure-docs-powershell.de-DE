---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 99fb9bf57f056a869310de2fe27d00a72ce5d8c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478849"
---
# <span data-ttu-id="d5bd2-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d5bd2-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="d5bd2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="d5bd2-103">Legt die Überwachungsrichtlinie für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5bd2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5bd2-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5bd2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="d5bd2-106">Das Cmdlet " **Satz-AzureRmSqlDatabaseAuditingPolicy** " ändert die Überwachungsrichtlinie einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="d5bd2-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d5bd2-108">Geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter anzugeben, um die Speicherschlüssel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="d5bd2-109">Sie können auch die Aufbewahrung für die Überwachungsprotokolltabelle definieren, indem Sie den Wert der *RetentionInDays* -und Table *Identifier* -Parameter festlegen, um den Zeitraum und den Startwert für die Namen der Überwachungsprotokoll Tabellen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="d5bd2-110">Geben Sie den *eventType* -Parameter an, um die zu überwachenden Ereignistypen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="d5bd2-111">Nachdem das Cmdlet erfolgreich ausgeführt wurde, ist die Überwachung der Datenbank aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="d5bd2-112">Wenn die Datenbank die Richtlinie Ihres Servers für die Überwachung verwendet hat, bevor Sie dieses Cmdlet ausgeführt haben, beendet die Überwachung die Verwendung dieser Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-112">If the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span>
<span data-ttu-id="d5bd2-113">Wenn das Cmdlet erfolgreich ist und Sie den *passthru* -Parameter verwenden, gibt es zusätzlich zu den Datenbankbezeichnern ein Objekt zurück, das die aktuelle Überwachungsrichtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-113">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="d5bd2-114">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-114">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="d5bd2-115">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-115">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d5bd2-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5bd2-116">EXAMPLES</span></span>

### <span data-ttu-id="d5bd2-117">Beispiel 1: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung der Tabellen Überwachung</span><span class="sxs-lookup"><span data-stu-id="d5bd2-117">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="d5bd2-118">Mit diesem Befehl wird die Überwachungsrichtlinie der Datenbank mit dem Namen Database01 auf Server01 festgelegt, um das Speicherkonto mit dem Namen Storage31 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-118">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="d5bd2-119">Beispiel 2: Festlegen des Speicherkonto Schlüssels einer vorhandenen Überwachungsrichtlinie einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="d5bd2-119">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="d5bd2-120">Mit diesem Befehl wird die Überwachungsrichtlinie der Datenbank mit dem Namen Database01 auf Server01 festgelegt, damit derselbe Speicherkonto Name verwendet wird, aber jetzt der sekundäre Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-120">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="d5bd2-121">Beispiel 3: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung eines bestimmten Ereignistyps</span><span class="sxs-lookup"><span data-stu-id="d5bd2-121">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="d5bd2-122">Beispiel 4: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung der BLOB-Überwachung</span><span class="sxs-lookup"><span data-stu-id="d5bd2-122">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="d5bd2-123">Dieser Befehl legt die Überwachungsrichtlinie der Datenbank mit dem Namen Database01 auf Server01 fest.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-123">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="d5bd2-124">Die Richtlinie protokolliert den Login_Failure-Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-124">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="d5bd2-125">Der Befehl ändert keine Speichereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-125">The command does not change the storage settings.</span></span>

## <span data-ttu-id="d5bd2-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5bd2-126">PARAMETERS</span></span>

### <span data-ttu-id="d5bd2-127">-Auditing</span><span class="sxs-lookup"><span data-stu-id="d5bd2-127">-AuditAction</span></span>
<span data-ttu-id="d5bd2-128">Geben Sie mindestens eine Überwachungsaktion an.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-128">Specify one or more audit actions.</span></span>
<span data-ttu-id="d5bd2-129">Dieser Parameter gilt nur für die BLOB-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-129">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="d5bd2-130">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d5bd2-130">-AuditActionGroup</span></span>
<span data-ttu-id="d5bd2-131">Geben Sie mindestens eine Überwachungs Aktionsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-131">Specify one or more audit action groups.</span></span>
<span data-ttu-id="d5bd2-132">Dieser Parameter gilt nur für die BLOB-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-132">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="d5bd2-133">-Audittype</span><span class="sxs-lookup"><span data-stu-id="d5bd2-133">-AuditType</span></span>
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

### <span data-ttu-id="d5bd2-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5bd2-134">-DatabaseName</span></span>
<span data-ttu-id="d5bd2-135">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-135">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="d5bd2-136">-EventType</span><span class="sxs-lookup"><span data-stu-id="d5bd2-136">-EventType</span></span>
<span data-ttu-id="d5bd2-137">Gibt die zu überwachenden Ereignistypen an.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-137">Specifies the event types to audit.</span></span>
<span data-ttu-id="d5bd2-138">Dieser Parameter gilt nur für die Tabellen Überwachung.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-138">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="d5bd2-139">Sie können mehrere Ereignistypen angeben.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-139">You can specify several event types.</span></span>
<span data-ttu-id="d5bd2-140">Sie können alle angeben, um alle Ereignistypen oder None zu überwachen, um anzugeben, dass keine Ereignisse überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-140">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="d5bd2-141">Wenn Sie alle oder keine gleichzeitig angeben, wird das Cmdlet nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-141">If you specify All or None at the same time, the cmdlet does not run.</span></span>

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

### <span data-ttu-id="d5bd2-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5bd2-142">-PassThru</span></span>
<span data-ttu-id="d5bd2-143">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d5bd2-144">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d5bd2-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5bd2-145">-ResourceGroupName</span></span>
<span data-ttu-id="d5bd2-146">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-146">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d5bd2-147">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d5bd2-147">-RetentionInDays</span></span>
<span data-ttu-id="d5bd2-148">Gibt die Anzahl der Aufbewahrungstage für die Überwachungsprotokolltabelle an.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-148">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="d5bd2-149">Der Wert 0 (null) bedeutet, dass die Tabelle nicht beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-149">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="d5bd2-150">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d5bd2-150">The default value is zero.</span></span>
<span data-ttu-id="d5bd2-151">Wenn Sie einen Wert angeben, der größer als 0 (null) ist, müssen Sie einen Wert für den *TableIdentifer* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-151">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="d5bd2-152">-Servername</span><span class="sxs-lookup"><span data-stu-id="d5bd2-152">-ServerName</span></span>
<span data-ttu-id="d5bd2-153">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-153">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d5bd2-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d5bd2-154">-StorageAccountName</span></span>
<span data-ttu-id="d5bd2-155">Gibt den Namen des speicherkontos für die Überwachung der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-155">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="d5bd2-156">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-156">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="d5bd2-157">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-157">This parameter is not required.</span></span>
<span data-ttu-id="d5bd2-158">Wenn Sie diesen Parameter nicht angeben, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Überwachungsrichtlinie der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-158">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="d5bd2-159">Wenn Sie zum ersten Mal eine Datenbank-Überwachungsrichtlinie definieren und diesen Parameter nicht angeben, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-159">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="d5bd2-160">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d5bd2-160">-StorageKeyType</span></span>
<span data-ttu-id="d5bd2-161">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-161">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="d5bd2-162">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d5bd2-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5bd2-163">Primär</span><span class="sxs-lookup"><span data-stu-id="d5bd2-163">Primary</span></span>
- <span data-ttu-id="d5bd2-164">Sekundär</span><span class="sxs-lookup"><span data-stu-id="d5bd2-164">Secondary</span></span>

<span data-ttu-id="d5bd2-165">Der Standardwert ist Primary.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-165">The default value is Primary.</span></span>

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

### <span data-ttu-id="d5bd2-166">-Tabellenidentifier</span><span class="sxs-lookup"><span data-stu-id="d5bd2-166">-TableIdentifier</span></span>
<span data-ttu-id="d5bd2-167">Gibt den Namen der Überwachungsprotokolltabelle an.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-167">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="d5bd2-168">Geben Sie diesen Wert an, wenn Sie für den *RetentionInDays* -Parameter einen Wert größer als 0 angeben.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-168">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="d5bd2-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5bd2-169">-Confirm</span></span>
<span data-ttu-id="d5bd2-170">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5bd2-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5bd2-171">-WhatIf</span></span>
<span data-ttu-id="d5bd2-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5bd2-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5bd2-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5bd2-174">-DefaultProfile</span></span>
<span data-ttu-id="d5bd2-175">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5bd2-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5bd2-176">CommonParameters</span></span>
<span data-ttu-id="d5bd2-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5bd2-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5bd2-178">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5bd2-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5bd2-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5bd2-179">INPUTS</span></span>

## <span data-ttu-id="d5bd2-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5bd2-180">OUTPUTS</span></span>

### <span data-ttu-id="d5bd2-181">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d5bd2-181">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="d5bd2-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5bd2-182">NOTES</span></span>

## <span data-ttu-id="d5bd2-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5bd2-183">RELATED LINKS</span></span>

[<span data-ttu-id="d5bd2-184">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d5bd2-184">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d5bd2-185">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d5bd2-185">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="d5bd2-186">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d5bd2-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


