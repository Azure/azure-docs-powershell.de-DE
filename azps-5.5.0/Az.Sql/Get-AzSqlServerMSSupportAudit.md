---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: c4f3687b2e520783c4b0392e1711dcea976e0c05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168721"
---
# <span data-ttu-id="3eb40-101">Get-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="3eb40-101">Get-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="3eb40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb40-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb40-103">Ruft die Überwachungseinstellungen für die Microsoft-Supportvorgänge eines Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="3eb40-103">Gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="3eb40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3eb40-104">SYNTAX</span></span>

### <span data-ttu-id="3eb40-105">ServerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3eb40-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eb40-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eb40-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3eb40-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3eb40-107">DESCRIPTION</span></span>
<span data-ttu-id="3eb40-108">Das **Cmdlet "Get-AzSqlServerMSSupportAudit"** ruft die Überwachungseinstellungen eines Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="3eb40-108">The **Get-AzSqlServerMSSupportAudit** cmdlet gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="3eb40-109">Geben Sie die *Parameter "ResourceGroupName"* und *"ServerName"* an, um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3eb40-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="3eb40-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3eb40-110">EXAMPLES</span></span>

### <span data-ttu-id="3eb40-111">Beispiel 1: Erhalten der Überwachungseinstellungen eines Azure SQL Supportvorgängen</span><span class="sxs-lookup"><span data-stu-id="3eb40-111">Example 1: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="3eb40-112">Beispiel 2: Erhalten der Überwachungseinstellungen eines Azure SQL Über die Pipeline</span><span class="sxs-lookup"><span data-stu-id="3eb40-112">Example 2: Get, through pipeline, the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerMSSupportAudit
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="3eb40-113">Beispiel 3: Erhalten der Überwachungseinstellungen eines Azure SQL Supportvorgängen</span><span class="sxs-lookup"><span data-stu-id="3eb40-113">Example 3: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="3eb40-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eb40-114">PARAMETERS</span></span>

### <span data-ttu-id="3eb40-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eb40-115">-AsJob</span></span>
<span data-ttu-id="3eb40-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3eb40-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3eb40-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb40-117">-DefaultProfile</span></span>
<span data-ttu-id="3eb40-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3eb40-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb40-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb40-119">-ResourceGroupName</span></span>
<span data-ttu-id="3eb40-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3eb40-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb40-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3eb40-121">-ServerName</span></span>
<span data-ttu-id="3eb40-122">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="3eb40-122">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb40-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="3eb40-123">-ServerObject</span></span>
<span data-ttu-id="3eb40-124">Das Serverobjekt zum Verwalten seiner Überwachungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="3eb40-124">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb40-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb40-125">CommonParameters</span></span>
<span data-ttu-id="3eb40-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb40-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb40-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3eb40-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb40-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3eb40-128">INPUTS</span></span>

### <span data-ttu-id="3eb40-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3eb40-129">System.String</span></span>

### <span data-ttu-id="3eb40-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="3eb40-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="3eb40-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3eb40-131">OUTPUTS</span></span>

### <span data-ttu-id="3eb40-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="3eb40-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="3eb40-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3eb40-133">NOTES</span></span>

## <span data-ttu-id="3eb40-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3eb40-134">RELATED LINKS</span></span>
