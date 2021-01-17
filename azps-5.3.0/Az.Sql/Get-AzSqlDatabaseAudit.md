---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: b6b6ca6bea6dd980b429ee17e69fb86556dd6ce0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375107"
---
# <span data-ttu-id="d98c2-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d98c2-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="d98c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d98c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d98c2-103">Ruft die Überwachungseinstellungen einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="d98c2-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="d98c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d98c2-104">SYNTAX</span></span>

### <span data-ttu-id="d98c2-105">DatabaseParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d98c2-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d98c2-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d98c2-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d98c2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d98c2-107">DESCRIPTION</span></span>
<span data-ttu-id="d98c2-108">Das **Cmdlet "Get-AzSqlDatabaseAudit"** ruft die Überwachungseinstellungen einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="d98c2-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="d98c2-109">Verwenden Sie zum Verwenden des Cmdlets die Parameter *"ResourceGroupName",* *"ServerName"* und *"DatabaseName",* um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d98c2-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="d98c2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d98c2-110">EXAMPLES</span></span>

### <span data-ttu-id="d98c2-111">Beispiel 1: Erhalten der Überwachungseinstellungen einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="d98c2-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="d98c2-112">Beispiel 2: Erhalten der Überwachungseinstellungen einer Azure SQL Pipeline</span><span class="sxs-lookup"><span data-stu-id="d98c2-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="d98c2-113">Beispiel 3: Erhalten der Überwachungseinstellungen einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="d98c2-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="d98c2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d98c2-114">PARAMETERS</span></span>

### <span data-ttu-id="d98c2-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d98c2-115">-DatabaseName</span></span>
<span data-ttu-id="d98c2-116">SQL Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="d98c2-116">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98c2-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d98c2-117">-DatabaseObject</span></span>
<span data-ttu-id="d98c2-118">Das Datenbankobjekt zum Verwalten seiner Überwachungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d98c2-118">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d98c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98c2-119">-DefaultProfile</span></span>
<span data-ttu-id="d98c2-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d98c2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d98c2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d98c2-121">-ResourceGroupName</span></span>
<span data-ttu-id="d98c2-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d98c2-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98c2-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d98c2-123">-ServerName</span></span>
<span data-ttu-id="d98c2-124">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="d98c2-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98c2-125">CommonParameters</span></span>
<span data-ttu-id="d98c2-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d98c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98c2-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d98c2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98c2-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d98c2-128">INPUTS</span></span>

### <span data-ttu-id="d98c2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d98c2-129">System.String</span></span>

### <span data-ttu-id="d98c2-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d98c2-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d98c2-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d98c2-131">OUTPUTS</span></span>

### <span data-ttu-id="d98c2-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="d98c2-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="d98c2-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d98c2-133">NOTES</span></span>

## <span data-ttu-id="d98c2-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d98c2-134">RELATED LINKS</span></span>
