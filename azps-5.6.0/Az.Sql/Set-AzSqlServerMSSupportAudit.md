---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 6e101beb73b68427f806fdae3fa2406082a9b47a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935488"
---
# <span data-ttu-id="3d165-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="3d165-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="3d165-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d165-102">SYNOPSIS</span></span>
<span data-ttu-id="3d165-103">Ändert die Überwachungseinstellungen für Microsoft-Supportvorgänge eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3d165-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="3d165-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d165-104">SYNTAX</span></span>

### <span data-ttu-id="3d165-105">ServerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d165-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d165-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d165-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d165-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d165-107">DESCRIPTION</span></span>
<span data-ttu-id="3d165-108">Das **Cmdlet Set-AzSqlServerMSSupportAudit** ändert die Einstellungen für die Überwachung von Microsoft-Supportvorgängen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3d165-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="3d165-109">Um das Cmdlet zu verwenden, verwenden Sie die *Parameter ResourceGroupName* und *ServerName,* um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3d165-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="3d165-110">Wenn blob storage ein Ziel für Überwachungsprotokolle ist, geben Sie den *Parameter StorageAccountResourceId* an, um das Speicherkonto für die Überwachungsprotokolle zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="3d165-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="3d165-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d165-111">EXAMPLES</span></span>

### <span data-ttu-id="3d165-112">Beispiel 1: Aktivieren der Microsoft-Supportüberwachungsrichtlinie für Den Blobspeicher eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="3d165-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="3d165-113">Beispiel 2: Deaktivieren der Überwachungsrichtlinie für Den Blobspeicher microsoft support operations eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="3d165-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="3d165-114">Beispiel 3: Aktivieren der Microsoft-Supportüberwachungsrichtlinie für Vorgänge eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="3d165-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="3d165-115">Beispiel 4: Deaktivieren der Microsoft-Supportüberwachungsrichtlinie für Vorgänge eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="3d165-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="3d165-116">Beispiel 5: Aktivieren der Überwachungsrichtlinie für Die Überwachung von Vorgängen durch Microsoft für die Protokollanalyse eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="3d165-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="3d165-117">Beispiel 6: Deaktivieren der Überwachungsrichtlinie für Die Überwachung von Vorgängen durch Microsoft für die Protokollanalyse eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="3d165-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="3d165-118">Beispiel 7: Deaktivieren der Überwachungsrichtlinie für Die Überwachung von Vorgängen durch Microsoft durch die Pipeline eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="3d165-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="3d165-119">Beispiel 8: Deaktivieren Sie das Senden von Überwachungsprotokollen für Microsoft-Supportvorgänge eines Azure SQL-Servers an den Blobspeicher, und aktivieren Sie das Senden zum Protokollieren von Analysen.</span><span class="sxs-lookup"><span data-stu-id="3d165-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="3d165-120">Beispiel 9: Aktivieren des Sendens von Überwachungsprotokollen eines Azure SQL-Servers an blob storage, event hub und log analytics.</span><span class="sxs-lookup"><span data-stu-id="3d165-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="3d165-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3d165-121">PARAMETERS</span></span>

### <span data-ttu-id="3d165-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d165-122">-AsJob</span></span>
<span data-ttu-id="3d165-123">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3d165-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d165-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="3d165-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="3d165-125">Gibt an, ob blob storage ein Ziel für Überwachungsdatensätze für Microsoft-Supportvorgänge ist.</span><span class="sxs-lookup"><span data-stu-id="3d165-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d165-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d165-126">-DefaultProfile</span></span>
<span data-ttu-id="3d165-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d165-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d165-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="3d165-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="3d165-129">Die Ressourcen-ID für die Ereignishubautorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="3d165-129">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d165-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="3d165-130">-EventHubName</span></span>
<span data-ttu-id="3d165-131">Der Name des Ereignishubs.</span><span class="sxs-lookup"><span data-stu-id="3d165-131">The name of the event hub.</span></span> <span data-ttu-id="3d165-132">Wenn beim Bereitstellen von EventHubAuthorizationRuleResourceId keine angegeben wird, wird der Standardereignishub ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3d165-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d165-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="3d165-133">-EventHubTargetState</span></span>
<span data-ttu-id="3d165-134">Gibt an, ob der Ereignishub ein Ziel für Überwachungsprotokolle für Microsoft-Supportvorgänge ist.</span><span class="sxs-lookup"><span data-stu-id="3d165-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d165-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="3d165-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="3d165-136">Gibt an, ob die Protokollanalyse ein Ziel für Überwachungsprotokolle für Microsoft-Supportvorgänge ist.</span><span class="sxs-lookup"><span data-stu-id="3d165-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d165-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d165-137">-PassThru</span></span>
<span data-ttu-id="3d165-138">Gibt an, ob die Überwachungsrichtlinie für Microsoft-Supportvorgänge am Ende der Cmdletausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d165-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="3d165-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d165-139">-ResourceGroupName</span></span>
<span data-ttu-id="3d165-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d165-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="3d165-141">-Servername</span><span class="sxs-lookup"><span data-stu-id="3d165-141">-ServerName</span></span>
<span data-ttu-id="3d165-142">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="3d165-142">SQL server name.</span></span>

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

### <span data-ttu-id="3d165-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="3d165-143">-ServerObject</span></span>
<span data-ttu-id="3d165-144">Das Serverobjekt zum Verwalten seiner Überwachungsrichtlinie für Microsoft-Supportvorgänge.</span><span class="sxs-lookup"><span data-stu-id="3d165-144">The server object to manage its Microsoft support operations audit policy.</span></span>

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

### <span data-ttu-id="3d165-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3d165-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="3d165-146">Ressourcen-ID des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3d165-146">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d165-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="3d165-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="3d165-148">Die Arbeitsbereichs-ID (Ressourcen-ID eines Log Analytics-Arbeitsbereichs) für einen Log Analytics-Arbeitsbereich, an den Sie Überwachungsprotokolle für Microsoft-Supportvorgänge senden möchten.</span><span class="sxs-lookup"><span data-stu-id="3d165-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="3d165-149">Beispiel: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="3d165-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d165-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d165-150">-Confirm</span></span>
<span data-ttu-id="3d165-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d165-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d165-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d165-152">-WhatIf</span></span>
<span data-ttu-id="3d165-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d165-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d165-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d165-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d165-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d165-155">CommonParameters</span></span>
<span data-ttu-id="3d165-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d165-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d165-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d165-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d165-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d165-158">INPUTS</span></span>

### <span data-ttu-id="3d165-159">System.String</span><span class="sxs-lookup"><span data-stu-id="3d165-159">System.String</span></span>

### <span data-ttu-id="3d165-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="3d165-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="3d165-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3d165-161">System.Guid</span></span>

### <span data-ttu-id="3d165-162">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3d165-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3d165-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="3d165-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="3d165-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d165-164">OUTPUTS</span></span>

### <span data-ttu-id="3d165-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d165-165">System.Boolean</span></span>

## <span data-ttu-id="3d165-166">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3d165-166">NOTES</span></span>

## <span data-ttu-id="3d165-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3d165-167">RELATED LINKS</span></span>
