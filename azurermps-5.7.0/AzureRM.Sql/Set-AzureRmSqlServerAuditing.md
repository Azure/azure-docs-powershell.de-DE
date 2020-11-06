---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 2a81030cdf985ae338692e59d86da30cee50694f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482674"
---
# <span data-ttu-id="43f76-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="43f76-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="43f76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43f76-102">SYNOPSIS</span></span>
<span data-ttu-id="43f76-103">Ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43f76-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43f76-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43f76-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43f76-105">DESCRIPTION</span></span>
<span data-ttu-id="43f76-106">Das Cmdlet " **Satz-AzureRmSqlServerAuditing** " ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43f76-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="43f76-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* und Server *Name* , um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="43f76-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="43f76-108">Geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter anzugeben, um die Speicherschlüssel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="43f76-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="43f76-109">Verwenden Sie den *State* -Parameter, um die Richtlinie zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="43f76-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="43f76-110">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="43f76-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="43f76-111">Nachdem das Cmdlet erfolgreich ausgeführt wurde, ist die Überwachung der Azure SQL-Datenbanken, die im angegebenen Azure SQL Server definiert sind, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="43f76-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="43f76-112">Wenn das Cmdlet erfolgreich ist und Sie den *passthru* -Parameter verwenden, gibt es zusätzlich zu den Server-IDs ein Objekt zurück, das die aktuelle BLOB-Überwachungsrichtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="43f76-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="43f76-113">Server-IDs beinhalten, sind aber nicht auf **ResourceGroupName** und Server **Name** limitiert.</span><span class="sxs-lookup"><span data-stu-id="43f76-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="43f76-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43f76-114">EXAMPLES</span></span>

### <span data-ttu-id="43f76-115">Beispiel 1: Aktivieren der Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="43f76-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="43f76-116">Beispiel 2: Deaktivieren der Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="43f76-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="43f76-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="43f76-117">PARAMETERS</span></span>

### <span data-ttu-id="43f76-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="43f76-118">-AuditActionGroup</span></span>
<span data-ttu-id="43f76-119">Die empfohlene Gruppe der zu verwendenden Aktionsgruppen ist die folgende Kombination, die alle Abfragen und gespeicherten Prozeduren überprüft, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="43f76-119">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="43f76-120">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="43f76-120">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="43f76-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="43f76-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="43f76-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="43f76-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="43f76-123">Diese obige Kombination ist auch die standardmäßig konfigurierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="43f76-123">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="43f76-124">Diese Gruppen decken alle SQL-Anweisungen und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Verbindung mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="43f76-124">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="43f76-125">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="43f76-125">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="43f76-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f76-126">-DefaultProfile</span></span>
<span data-ttu-id="43f76-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43f76-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43f76-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43f76-128">-PassThru</span></span>
<span data-ttu-id="43f76-129">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="43f76-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="43f76-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43f76-130">-ResourceGroupName</span></span>
<span data-ttu-id="43f76-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43f76-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="43f76-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="43f76-132">-RetentionInDays</span></span>
<span data-ttu-id="43f76-133">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="43f76-133">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="43f76-134">-Servername</span><span class="sxs-lookup"><span data-stu-id="43f76-134">-ServerName</span></span>
<span data-ttu-id="43f76-135">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="43f76-135">SQL server name.</span></span>

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

### <span data-ttu-id="43f76-136">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="43f76-136">-State</span></span>
<span data-ttu-id="43f76-137">Der Zustand der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="43f76-137">The state of the policy.</span></span>

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

### <span data-ttu-id="43f76-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="43f76-138">-StorageAccountName</span></span>
<span data-ttu-id="43f76-139">Der Name des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="43f76-139">The name of the storage account.</span></span> <span data-ttu-id="43f76-140">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="43f76-140">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="43f76-141">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="43f76-141">This parameter is not required.</span></span>  
<span data-ttu-id="43f76-142">Wenn Sie diesen Parameter nicht angeben, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Überwachungsrichtlinie definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="43f76-142">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="43f76-143">Wenn Sie zum ersten Mal eine Überwachungsrichtlinie definieren und diesen Parameter nicht angeben, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="43f76-143">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="43f76-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="43f76-144">-StorageKeyType</span></span>
<span data-ttu-id="43f76-145">Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43f76-145">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="43f76-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43f76-146">-Confirm</span></span>
<span data-ttu-id="43f76-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43f76-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f76-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f76-148">-WhatIf</span></span>
<span data-ttu-id="43f76-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43f76-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43f76-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43f76-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f76-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f76-151">CommonParameters</span></span>
<span data-ttu-id="43f76-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f76-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f76-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f76-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f76-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43f76-154">INPUTS</span></span>

### <span data-ttu-id="43f76-155">Keine</span><span class="sxs-lookup"><span data-stu-id="43f76-155">None</span></span>
<span data-ttu-id="43f76-156">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="43f76-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43f76-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43f76-157">OUTPUTS</span></span>

### <span data-ttu-id="43f76-158">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="43f76-158">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="43f76-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="43f76-159">NOTES</span></span>

## <span data-ttu-id="43f76-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43f76-160">RELATED LINKS</span></span>
