---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 623f52f1de9370c679f6df09b6cf05c50f38ca6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468028"
---
# <span data-ttu-id="1d0e5-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="1d0e5-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="1d0e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="1d0e5-103">Ändert die Überwachungseinstellungen für die Microsoft-Supportvorgänge eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="1d0e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d0e5-104">SYNTAX</span></span>

### <span data-ttu-id="1d0e5-105">ServerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d0e5-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d0e5-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d0e5-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d0e5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d0e5-107">DESCRIPTION</span></span>
<span data-ttu-id="1d0e5-108">Das **Cmdlet "Set-AzSqlServerMSSupportAudit"** ändert die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="1d0e5-109">Verwenden Sie zum Verwenden des Cmdlets die Parameter *"ResourceGroupName"* und *"ServerName",* um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="1d0e5-110">Wenn blob storage ein Ziel für Überwachungsprotokolle ist, geben Sie den *Parameter StorageAccountResourceId* an, um das Speicherkonto für die Überwachungsprotokolle zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="1d0e5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d0e5-111">EXAMPLES</span></span>

### <span data-ttu-id="1d0e5-112">Beispiel 1: Aktivieren der Überwachungsrichtlinie für den Blob Storage von Microsoft für Supportvorgänge eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1d0e5-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="1d0e5-113">Beispiel 2: Deaktivieren der Überwachungsrichtlinie für den Blob Storage von Microsoft support operations eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1d0e5-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1d0e5-114">Beispiel 3: Aktivieren der Überwachungsrichtlinie für den Ereignishub der Microsoft-Supportvorgänge eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1d0e5-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="1d0e5-115">Beispiel 4: Deaktivieren der Überwachungsrichtlinie für den Ereignishub der Microsoft-Supportvorgänge eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1d0e5-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="1d0e5-116">Beispiel 5: Aktivieren der Überwachungsprotokollanalyse der Microsoft Support Operations Auditing Policy für einen Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1d0e5-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="1d0e5-117">Beispiel 6: Deaktivieren der Überwachungsprotokollanalyserichtlinie der Microsoft Support Operations Auditing eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1d0e5-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1d0e5-118">Beispiel 7: Deaktivieren sie über die Pipeline die Überwachungsprotokollanalyserichtlinie eines Azure SQL-Servers.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1d0e5-119">Beispiel 8: Deaktivieren des Sendens von Überwachungsdatensätzen eines Azure SQL-Servers an den BLOB-Speicher und Ermöglichen des Sendens von Daten zur Protokollanalyse.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1d0e5-120">Beispiel 9: Aktivieren des Sendens von Microsoft-Supportvorgängen-Überwachungsdatensätzen eines Azure SQL-Servers an BLOB-Speicher, Ereignishub und Protokollanalysen.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="1d0e5-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d0e5-121">PARAMETERS</span></span>

### <span data-ttu-id="1d0e5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d0e5-122">-AsJob</span></span>
<span data-ttu-id="1d0e5-123">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1d0e5-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d0e5-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="1d0e5-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="1d0e5-125">Gibt an, ob BLOB-Speicher ein Ziel für Überwachungsdatensätze für Supportvorgänge von Microsoft ist.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="1d0e5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d0e5-126">-DefaultProfile</span></span>
<span data-ttu-id="1d0e5-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d0e5-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="1d0e5-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="1d0e5-129">Die Ressourcen-ID für die Ereignishubautorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="1d0e5-129">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="1d0e5-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="1d0e5-130">-EventHubName</span></span>
<span data-ttu-id="1d0e5-131">Der Name des Ereignishubs.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-131">The name of the event hub.</span></span> <span data-ttu-id="1d0e5-132">Wenn beim Bereitstellen von EventHubAuthorizationRuleResourceId keine Angabe ausgeführt wird, wird der Standardereignishub ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="1d0e5-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="1d0e5-133">-EventHubTargetState</span></span>
<span data-ttu-id="1d0e5-134">Gibt an, ob der Ereignishub ein Ziel für Überwachungsdatensätze für Supportvorgänge von Microsoft ist.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="1d0e5-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="1d0e5-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="1d0e5-136">Gibt an, ob die Protokollanalyse ein Ziel für Überwachungsdatensätze für Supportvorgänge von Microsoft ist.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="1d0e5-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d0e5-137">-PassThru</span></span>
<span data-ttu-id="1d0e5-138">Gibt an, ob die Überwachungsrichtlinie für Supportvorgänge von Microsoft am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1d0e5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d0e5-139">-ResourceGroupName</span></span>
<span data-ttu-id="1d0e5-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="1d0e5-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1d0e5-141">-ServerName</span></span>
<span data-ttu-id="1d0e5-142">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-142">SQL server name.</span></span>

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

### <span data-ttu-id="1d0e5-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="1d0e5-143">-ServerObject</span></span>
<span data-ttu-id="1d0e5-144">Das Serverobjekt zum Verwalten seiner Überwachungsrichtlinie für Supportvorgänge von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-144">The server object to manage its Microsoft support operations audit policy.</span></span>

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

### <span data-ttu-id="1d0e5-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1d0e5-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="1d0e5-146">Die Ressourcen-ID des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="1d0e5-146">The storage account resource id</span></span>

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

### <span data-ttu-id="1d0e5-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="1d0e5-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="1d0e5-148">Die Arbeitsbereichs-ID (Ressourcen-ID eines Log Analytics-Arbeitsbereichs) für einen Log Analytics-Arbeitsbereich, an den Sie Überwachungsprotokolle für Supportvorgänge von Microsoft senden möchten.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="1d0e5-149">Beispiel: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="1d0e5-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="1d0e5-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d0e5-150">-Confirm</span></span>
<span data-ttu-id="1d0e5-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d0e5-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1d0e5-152">-WhatIf</span></span>
<span data-ttu-id="1d0e5-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d0e5-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d0e5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d0e5-155">CommonParameters</span></span>
<span data-ttu-id="1d0e5-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d0e5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d0e5-157">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d0e5-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d0e5-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d0e5-158">INPUTS</span></span>

### <span data-ttu-id="1d0e5-159">System.String</span><span class="sxs-lookup"><span data-stu-id="1d0e5-159">System.String</span></span>

### <span data-ttu-id="1d0e5-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1d0e5-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="1d0e5-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1d0e5-161">System.Guid</span></span>

### <span data-ttu-id="1d0e5-162">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1d0e5-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1d0e5-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="1d0e5-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="1d0e5-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d0e5-164">OUTPUTS</span></span>

### <span data-ttu-id="1d0e5-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d0e5-165">System.Boolean</span></span>

## <span data-ttu-id="1d0e5-166">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d0e5-166">NOTES</span></span>

## <span data-ttu-id="1d0e5-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d0e5-167">RELATED LINKS</span></span>
