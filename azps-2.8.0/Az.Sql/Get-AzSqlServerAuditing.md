---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: cf9bea67027e7a2c5e3928755f6d88b1dc124489
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826083"
---
# <span data-ttu-id="e6187-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="e6187-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="e6187-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6187-102">SYNOPSIS</span></span>
<span data-ttu-id="e6187-103">**Wichtig: Dieses Cmdlet ist veraltet, wenn Sie von [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) ersetzt werden.**</span><span class="sxs-lookup"><span data-stu-id="e6187-103">**Important: This cmdlet is deprecated, [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="e6187-104">Ruft die Überwachungseinstellungen eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="e6187-104">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="e6187-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6187-105">SYNTAX</span></span>

### <span data-ttu-id="e6187-106">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6187-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6187-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="e6187-107">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6187-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="e6187-108">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6187-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="e6187-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6187-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="e6187-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6187-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="e6187-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6187-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6187-112">DESCRIPTION</span></span>
<span data-ttu-id="e6187-113">Das Cmdlet " **Get-AzSqlServerAuditing** " Ruft die Überwachungseinstellungen eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="e6187-113">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="e6187-114">Geben Sie die Parameter *ResourceGroupName* und Server *Name* an, um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e6187-114">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="e6187-115">Das Ziel der Überwachungsprotokolle wird bestimmt, indem Sie einen der folgenden Switch-Parameter angeben: BlobStorage, LogAnalytics oder EventHub (wenn keine angegeben ist, ist der Standardwert BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="e6187-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="e6187-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6187-116">EXAMPLES</span></span>

### <span data-ttu-id="e6187-117">Beispiel 1: Abrufen der BLOB-Speicher Überwachungseinstellungen eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="e6187-117">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="e6187-118">Beispiel 2: Abrufen der Speicher Überwachungseinstellungen für BLOB-Speicher eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="e6187-118">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
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

### <span data-ttu-id="e6187-119">Beispiel 3: Abrufen, durch Pipeline, die Speicher Überwachungseinstellungen für BLOB-Speicher eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="e6187-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
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

### <span data-ttu-id="e6187-120">Beispiel 4: Abrufen der Ereignis-Hub-Überwachungseinstellungen eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="e6187-120">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="e6187-121">Beispiel 5: Abrufen, durch Pipeline, die Ereignis-Hub-Überwachungseinstellungen eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="e6187-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="e6187-122">Beispiel 6: Abrufen der Überwachungseinstellungen für die Protokollanalyse eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="e6187-122">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="e6187-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6187-123">PARAMETERS</span></span>

### <span data-ttu-id="e6187-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="e6187-124">-BlobStorage</span></span>
<span data-ttu-id="e6187-125">Gibt an, dass das Überwachungsprotokoll Ziel BLOB-Speicher ist</span><span class="sxs-lookup"><span data-stu-id="e6187-125">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="e6187-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6187-126">-DefaultProfile</span></span>
<span data-ttu-id="e6187-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e6187-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6187-128">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e6187-128">-EventHub</span></span>
<span data-ttu-id="e6187-129">Gibt an, dass das Überwachungsprotokoll Zielereignis-Hub ist</span><span class="sxs-lookup"><span data-stu-id="e6187-129">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="e6187-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e6187-130">-InputObject</span></span>
<span data-ttu-id="e6187-131">Das Serverobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6187-131">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6187-132">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="e6187-132">-LogAnalytics</span></span>
<span data-ttu-id="e6187-133">Gibt an, dass die Überwachungsprotokolle Zielprotokoll Analyse sind.</span><span class="sxs-lookup"><span data-stu-id="e6187-133">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="e6187-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6187-134">-ResourceGroupName</span></span>
<span data-ttu-id="e6187-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e6187-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6187-136">-Servername</span><span class="sxs-lookup"><span data-stu-id="e6187-136">-ServerName</span></span>
<span data-ttu-id="e6187-137">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="e6187-137">SQL server name.</span></span>

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

### <span data-ttu-id="e6187-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6187-138">-Confirm</span></span>
<span data-ttu-id="e6187-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6187-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6187-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6187-140">-WhatIf</span></span>
<span data-ttu-id="e6187-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6187-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6187-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6187-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6187-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6187-143">CommonParameters</span></span>
<span data-ttu-id="e6187-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6187-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6187-145">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6187-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6187-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6187-146">INPUTS</span></span>

### <span data-ttu-id="e6187-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e6187-147">System.String</span></span>

### <span data-ttu-id="e6187-148">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="e6187-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="e6187-149">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="e6187-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6187-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6187-150">OUTPUTS</span></span>

### <span data-ttu-id="e6187-151">Microsoft. Azure. Commands. SQL. Auditing. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="e6187-151">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="e6187-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6187-152">NOTES</span></span>

## <span data-ttu-id="e6187-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6187-153">RELATED LINKS</span></span>
