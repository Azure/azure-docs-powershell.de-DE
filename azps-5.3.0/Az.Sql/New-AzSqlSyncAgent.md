---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: 4a4ce99eb30aaa959eabdc9c1385b567aef2b0fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460668"
---
# <span data-ttu-id="fca5c-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="fca5c-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="fca5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fca5c-102">SYNOPSIS</span></span>
<span data-ttu-id="fca5c-103">Erstellt einen Azure SQL-Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="fca5c-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="fca5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fca5c-104">SYNTAX</span></span>

### <span data-ttu-id="fca5c-105">SyncDatabaseComponent (Standard)</span><span class="sxs-lookup"><span data-stu-id="fca5c-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fca5c-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="fca5c-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fca5c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fca5c-107">DESCRIPTION</span></span>
<span data-ttu-id="fca5c-108">Das **Cmdlet "New-AzSqlSyncAgent"** erstellt einen Azure SQL-Agent.</span><span class="sxs-lookup"><span data-stu-id="fca5c-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="fca5c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fca5c-109">EXAMPLES</span></span>

### <span data-ttu-id="fca5c-110">Beispiel 1: Erstellen eines Synchronisierungs-Agents für einen Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fca5c-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="fca5c-111">Mit diesem Befehl wird ein Synchronisierungs-Agent für einen Azure SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="fca5c-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="fca5c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fca5c-112">PARAMETERS</span></span>

### <span data-ttu-id="fca5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca5c-113">-DefaultProfile</span></span>
<span data-ttu-id="fca5c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fca5c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fca5c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fca5c-115">-Name</span></span>
<span data-ttu-id="fca5c-116">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="fca5c-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fca5c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca5c-117">-ResourceGroupName</span></span>
<span data-ttu-id="fca5c-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fca5c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="fca5c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fca5c-119">-ServerName</span></span>
<span data-ttu-id="fca5c-120">Der Name des Azure-SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="fca5c-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="fca5c-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fca5c-121">-SyncDatabaseName</span></span>
<span data-ttu-id="fca5c-122">Die Datenbank, die zum Speichern von Synchronisierungsmetadaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fca5c-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca5c-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca5c-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="fca5c-124">Die Ressourcengruppe, zu der die Synchronisierungsmetadatendatenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="fca5c-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca5c-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="fca5c-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="fca5c-126">Die Ressourcen-ID der Synchronisierungsmetadatendatenbank.</span><span class="sxs-lookup"><span data-stu-id="fca5c-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca5c-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="fca5c-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="fca5c-128">Der Server, auf dem die Synchronisierungsmetadatendatenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="fca5c-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca5c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fca5c-129">-Confirm</span></span>
<span data-ttu-id="fca5c-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fca5c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca5c-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fca5c-131">-WhatIf</span></span>
<span data-ttu-id="fca5c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fca5c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca5c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fca5c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca5c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca5c-134">CommonParameters</span></span>
<span data-ttu-id="fca5c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fca5c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca5c-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fca5c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca5c-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fca5c-137">INPUTS</span></span>

### <span data-ttu-id="fca5c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fca5c-138">System.String</span></span>

## <span data-ttu-id="fca5c-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fca5c-139">OUTPUTS</span></span>

### <span data-ttu-id="fca5c-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="fca5c-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="fca5c-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fca5c-141">NOTES</span></span>

## <span data-ttu-id="fca5c-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fca5c-142">RELATED LINKS</span></span>

[<span data-ttu-id="fca5c-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="fca5c-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="fca5c-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="fca5c-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

