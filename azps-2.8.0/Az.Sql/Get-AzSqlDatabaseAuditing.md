---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 641ab27f75950a2c15035a7787346250a41f9ab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825696"
---
# <span data-ttu-id="d1cc9-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d1cc9-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="d1cc9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="d1cc9-103">**Wichtig: Dieses Cmdlet ist veraltet, wenn Sie von [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) ersetzt werden.**</span><span class="sxs-lookup"><span data-stu-id="d1cc9-103">**Important: This cmdlet is deprecated, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="d1cc9-104">Ruft die Überwachungseinstellungen einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-104">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="d1cc9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1cc9-105">SYNTAX</span></span>

### <span data-ttu-id="d1cc9-106">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1cc9-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1cc9-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="d1cc9-107">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1cc9-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="d1cc9-108">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1cc9-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="d1cc9-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1cc9-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="d1cc9-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1cc9-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="d1cc9-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1cc9-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1cc9-112">DESCRIPTION</span></span>
<span data-ttu-id="d1cc9-113">Das Cmdlet " **Get-AzSqlDatabaseAuditing** " Ruft die Überwachungseinstellungen einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-113">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="d1cc9-114">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-114">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d1cc9-115">Das Ziel der Überwachungsprotokolle wird bestimmt, indem Sie einen der folgenden Switch-Parameter angeben: BlobStorage, LogAnalytics oder EventHub (wenn keine angegeben ist, ist der Standardwert BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="d1cc9-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="d1cc9-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1cc9-116">EXAMPLES</span></span>

### <span data-ttu-id="d1cc9-117">Beispiel 1: Abrufen der BLOB-Speicher Überwachungseinstellungen einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="d1cc9-117">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="d1cc9-118">Beispiel 2: Abrufen der BLOB-Speicher Überwachungseinstellungen einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="d1cc9-118">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="d1cc9-119">Beispiel 3: Abrufen, durch Pipeline, die Einstellungen für die BLOB-Speicherüberwachung einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="d1cc9-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="d1cc9-120">Beispiel 4: Abrufen der Ereignis-Hub-Überwachungseinstellungen einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="d1cc9-120">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="d1cc9-121">Beispiel 5: Abrufen, durch Pipeline, die Ereignis-Hub-Überwachungseinstellungen einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="d1cc9-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="d1cc9-122">Beispiel 6: Abrufen der Überwachungseinstellungen für die Protokollanalyse einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="d1cc9-122">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="d1cc9-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1cc9-123">PARAMETERS</span></span>

### <span data-ttu-id="d1cc9-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="d1cc9-124">-BlobStorage</span></span>
<span data-ttu-id="d1cc9-125">Gibt an, dass das Überwachungsprotokoll Ziel BLOB-Speicher ist</span><span class="sxs-lookup"><span data-stu-id="d1cc9-125">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cc9-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1cc9-126">-DatabaseName</span></span>
<span data-ttu-id="d1cc9-127">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="d1cc9-127">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cc9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1cc9-128">-DefaultProfile</span></span>
<span data-ttu-id="d1cc9-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1cc9-130">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d1cc9-130">-EventHub</span></span>
<span data-ttu-id="d1cc9-131">Gibt an, dass das Überwachungsprotokoll Zielereignis-Hub ist</span><span class="sxs-lookup"><span data-stu-id="d1cc9-131">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="d1cc9-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1cc9-132">-InputObject</span></span>
<span data-ttu-id="d1cc9-133">Das Datenbankobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-133">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cc9-134">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="d1cc9-134">-LogAnalytics</span></span>
<span data-ttu-id="d1cc9-135">Gibt an, dass die Überwachungsprotokolle Zielprotokoll Analyse sind.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-135">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="d1cc9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1cc9-136">-ResourceGroupName</span></span>
<span data-ttu-id="d1cc9-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cc9-138">-Servername</span><span class="sxs-lookup"><span data-stu-id="d1cc9-138">-ServerName</span></span>
<span data-ttu-id="d1cc9-139">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-139">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cc9-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1cc9-140">-Confirm</span></span>
<span data-ttu-id="d1cc9-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1cc9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1cc9-142">-WhatIf</span></span>
<span data-ttu-id="d1cc9-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1cc9-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1cc9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1cc9-145">CommonParameters</span></span>
<span data-ttu-id="d1cc9-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1cc9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1cc9-147">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1cc9-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1cc9-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1cc9-148">INPUTS</span></span>

### <span data-ttu-id="d1cc9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d1cc9-149">System.String</span></span>

### <span data-ttu-id="d1cc9-150">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d1cc9-150">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="d1cc9-151">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d1cc9-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1cc9-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1cc9-152">OUTPUTS</span></span>

### <span data-ttu-id="d1cc9-153">Microsoft. Azure. Commands. SQL. Auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="d1cc9-153">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="d1cc9-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1cc9-154">NOTES</span></span>

## <span data-ttu-id="d1cc9-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1cc9-155">RELATED LINKS</span></span>
