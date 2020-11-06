---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499118"
---
# <span data-ttu-id="bdc90-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="bdc90-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="bdc90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdc90-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc90-103">Ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bdc90-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdc90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdc90-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdc90-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdc90-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc90-106">Das Cmdlet " **Satz-AzureRmSqlServerAuditing** " ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bdc90-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="bdc90-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* und Server *Name* , um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bdc90-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="bdc90-108">Geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter anzugeben, um die Speicherschlüssel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="bdc90-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="bdc90-109">Verwenden Sie den *State* -Parameter, um die Richtlinie zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bdc90-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="bdc90-110">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="bdc90-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="bdc90-111">Nachdem das Cmdlet erfolgreich ausgeführt wurde, ist die Überwachung der Azure SQL-Datenbanken, die im angegebenen Azure SQL Server definiert sind, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bdc90-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="bdc90-112">Wenn das Cmdlet erfolgreich ist und Sie den *passthru* -Parameter verwenden, gibt es zusätzlich zu den Server-IDs ein Objekt zurück, das die aktuelle BLOB-Überwachungsrichtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="bdc90-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="bdc90-113">Server-IDs beinhalten, sind aber nicht auf **ResourceGroupName** und Server **Name** limitiert.</span><span class="sxs-lookup"><span data-stu-id="bdc90-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="bdc90-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdc90-114">EXAMPLES</span></span>

### <span data-ttu-id="bdc90-115">Beispiel 1: Aktivieren der Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="bdc90-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="bdc90-116">Beispiel 2: Deaktivieren der Überwachungsrichtlinie eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="bdc90-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="bdc90-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdc90-117">PARAMETERS</span></span>

### <span data-ttu-id="bdc90-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="bdc90-118">-AuditActionGroup</span></span>
<span data-ttu-id="bdc90-119">Die Gruppe der Überwachungs Aktionsgruppen</span><span class="sxs-lookup"><span data-stu-id="bdc90-119">The set of the audit action groups</span></span>

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

### <span data-ttu-id="bdc90-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdc90-120">-PassThru</span></span>
<span data-ttu-id="bdc90-121">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="bdc90-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bdc90-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc90-122">-ResourceGroupName</span></span>
<span data-ttu-id="bdc90-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bdc90-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="bdc90-124">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bdc90-124">-RetentionInDays</span></span>
<span data-ttu-id="bdc90-125">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="bdc90-125">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="bdc90-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="bdc90-126">-ServerName</span></span>
<span data-ttu-id="bdc90-127">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="bdc90-127">SQL server name.</span></span>

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

### <span data-ttu-id="bdc90-128">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="bdc90-128">-State</span></span>
<span data-ttu-id="bdc90-129">Der Status der Überwachungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="bdc90-129">The state of the auditing policy</span></span>

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

### <span data-ttu-id="bdc90-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bdc90-130">-StorageAccountName</span></span>
<span data-ttu-id="bdc90-131">Der Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="bdc90-131">The name of the storage account</span></span>

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

### <span data-ttu-id="bdc90-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="bdc90-132">-StorageKeyType</span></span>
<span data-ttu-id="bdc90-133">Der Typ des Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="bdc90-133">The type of the storage key</span></span>

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

### <span data-ttu-id="bdc90-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bdc90-134">-Confirm</span></span>
<span data-ttu-id="bdc90-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdc90-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc90-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc90-136">-WhatIf</span></span>
<span data-ttu-id="bdc90-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdc90-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdc90-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdc90-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc90-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc90-139">-DefaultProfile</span></span>
<span data-ttu-id="bdc90-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdc90-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdc90-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc90-141">CommonParameters</span></span>
<span data-ttu-id="bdc90-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc90-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc90-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc90-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc90-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdc90-144">INPUTS</span></span>

## <span data-ttu-id="bdc90-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdc90-145">OUTPUTS</span></span>

### <span data-ttu-id="bdc90-146">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="bdc90-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="bdc90-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdc90-147">NOTES</span></span>

## <span data-ttu-id="bdc90-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdc90-148">RELATED LINKS</span></span>

