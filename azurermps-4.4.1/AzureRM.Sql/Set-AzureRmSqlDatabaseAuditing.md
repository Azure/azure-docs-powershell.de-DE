---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a6d09b573225efa5f8467e9ca02edb65a87ebe10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483261"
---
# <span data-ttu-id="abb39-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="abb39-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="abb39-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abb39-102">SYNOPSIS</span></span>
<span data-ttu-id="abb39-103">Ändert die Überwachungseinstellungen für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="abb39-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb39-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abb39-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abb39-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abb39-105">DESCRIPTION</span></span>
<span data-ttu-id="abb39-106">Das Cmdlet " **Satz-AzureRmSqlDatabaseAuditing** " ändert die Überwachungseinstellungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="abb39-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="abb39-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="abb39-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="abb39-108">Geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter anzugeben, um die Speicherschlüssel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="abb39-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="abb39-109">Verwenden Sie den *State* -Parameter, um die Richtlinie zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="abb39-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="abb39-110">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="abb39-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="abb39-111">Nachdem das Cmdlet erfolgreich ausgeführt wurde, ist die Überwachung der Datenbank aktiviert.</span><span class="sxs-lookup"><span data-stu-id="abb39-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="abb39-112">Wenn das Cmdlet erfolgreich ist und Sie den *passthru* -Parameter verwenden, wird zusätzlich zu den Datenbankbezeichnern ein Objekt zurückgegeben, das die aktuelle BLOB-Überwachungsrichtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="abb39-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="abb39-113">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="abb39-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="abb39-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abb39-114">EXAMPLES</span></span>

### <span data-ttu-id="abb39-115">Beispiel 1: Aktivieren der Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="abb39-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="abb39-116">Beispiel 2: Deaktivieren der BLOB-Überwachungsrichtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="abb39-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="abb39-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="abb39-117">PARAMETERS</span></span>

### <span data-ttu-id="abb39-118">-Auditing</span><span class="sxs-lookup"><span data-stu-id="abb39-118">-AuditAction</span></span>
<span data-ttu-id="abb39-119">Die Gruppe der Überwachungsaktionen</span><span class="sxs-lookup"><span data-stu-id="abb39-119">The set of the audit actions</span></span>

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

### <span data-ttu-id="abb39-120">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="abb39-120">-AuditActionGroup</span></span>
<span data-ttu-id="abb39-121">Die Gruppe der Überwachungs Aktionsgruppen</span><span class="sxs-lookup"><span data-stu-id="abb39-121">The set of the audit action groups</span></span>

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

### <span data-ttu-id="abb39-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="abb39-122">-DatabaseName</span></span>
<span data-ttu-id="abb39-123">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="abb39-123">SQL Database name.</span></span>

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

### <span data-ttu-id="abb39-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abb39-124">-PassThru</span></span>
<span data-ttu-id="abb39-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="abb39-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="abb39-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb39-126">-ResourceGroupName</span></span>
<span data-ttu-id="abb39-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="abb39-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="abb39-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="abb39-128">-RetentionInDays</span></span>
<span data-ttu-id="abb39-129">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="abb39-129">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="abb39-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="abb39-130">-ServerName</span></span>
<span data-ttu-id="abb39-131">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="abb39-131">SQL Database server name.</span></span>

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

### <span data-ttu-id="abb39-132">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="abb39-132">-State</span></span>
<span data-ttu-id="abb39-133">Der Status der Überwachungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="abb39-133">The state of the auditing policy</span></span>

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

### <span data-ttu-id="abb39-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="abb39-134">-StorageAccountName</span></span>
<span data-ttu-id="abb39-135">Der Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="abb39-135">The name of the storage account</span></span>

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

### <span data-ttu-id="abb39-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="abb39-136">-StorageKeyType</span></span>
<span data-ttu-id="abb39-137">Der Typ des Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="abb39-137">The type of the storage key</span></span>

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

### <span data-ttu-id="abb39-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="abb39-138">-Confirm</span></span>
<span data-ttu-id="abb39-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abb39-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abb39-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb39-140">-WhatIf</span></span>
<span data-ttu-id="abb39-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abb39-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abb39-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abb39-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abb39-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb39-143">-DefaultProfile</span></span>
<span data-ttu-id="abb39-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="abb39-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abb39-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb39-145">CommonParameters</span></span>
<span data-ttu-id="abb39-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb39-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb39-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb39-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb39-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abb39-148">INPUTS</span></span>

## <span data-ttu-id="abb39-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abb39-149">OUTPUTS</span></span>

### <span data-ttu-id="abb39-150">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="abb39-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="abb39-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="abb39-151">NOTES</span></span>

## <span data-ttu-id="abb39-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abb39-152">RELATED LINKS</span></span>

