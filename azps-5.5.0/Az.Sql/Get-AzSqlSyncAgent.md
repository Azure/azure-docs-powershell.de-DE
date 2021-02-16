---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150529"
---
# <span data-ttu-id="69210-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="69210-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="69210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69210-102">SYNOPSIS</span></span>
<span data-ttu-id="69210-103">Gibt Informationen zu Azure SQL Sync Agents zurück.</span><span class="sxs-lookup"><span data-stu-id="69210-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="69210-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69210-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69210-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69210-105">DESCRIPTION</span></span>
<span data-ttu-id="69210-106">Das **Cmdlet "Get-AzSqlSyncAgent"** gibt Informationen zu einem oder mehreren Azure SQL Sync Agents zurück.</span><span class="sxs-lookup"><span data-stu-id="69210-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="69210-107">Geben Sie den Namen eines Synchronisierungs-Agents an, um nur Informationen zu diesem Synchronisierungs-Agent zu sehen.</span><span class="sxs-lookup"><span data-stu-id="69210-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="69210-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69210-108">EXAMPLES</span></span>

### <span data-ttu-id="69210-109">Beispiel 1: Erhalten aller Instanzen von Azure SQL-Synchronisierungs-Agent, die einem Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="69210-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="69210-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Synchronisierungs-Agents ab, die einem Azure-SQL Server.</span><span class="sxs-lookup"><span data-stu-id="69210-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="69210-111">Beispiel 2: Informationen zu einem Azure SQL-Synchronisierungs-Agent</span><span class="sxs-lookup"><span data-stu-id="69210-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="69210-112">Dieser Befehl ruft Informationen zum Azure SQL-Datenbanksynchronisierungs-Agent mit dem Namen "SyncAgent01" ab.</span><span class="sxs-lookup"><span data-stu-id="69210-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="69210-113">Beispiel 3: Erhalten aller Instanzen von Azure SQL-Synchronisierungs-Agent, der einem Azure SQL Server mithilfe der Filterung zugewiesen wurde</span><span class="sxs-lookup"><span data-stu-id="69210-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="69210-114">Dieser Befehl ruft Informationen zu allen Azure SQL-Synchronisierungs-Agents ab, die einem Azure SQL Server, die mit "SyncAgent" beginnen.</span><span class="sxs-lookup"><span data-stu-id="69210-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="69210-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69210-115">PARAMETERS</span></span>

### <span data-ttu-id="69210-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69210-116">-DefaultProfile</span></span>
<span data-ttu-id="69210-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="69210-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69210-118">-Name</span><span class="sxs-lookup"><span data-stu-id="69210-118">-Name</span></span>
<span data-ttu-id="69210-119">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="69210-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69210-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69210-120">-ResourceGroupName</span></span>
<span data-ttu-id="69210-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69210-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="69210-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69210-122">-ServerName</span></span>
<span data-ttu-id="69210-123">Der Name des Azure-SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="69210-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="69210-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69210-124">CommonParameters</span></span>
<span data-ttu-id="69210-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69210-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69210-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69210-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69210-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69210-127">INPUTS</span></span>

### <span data-ttu-id="69210-128">System.String</span><span class="sxs-lookup"><span data-stu-id="69210-128">System.String</span></span>

## <span data-ttu-id="69210-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69210-129">OUTPUTS</span></span>

### <span data-ttu-id="69210-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="69210-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="69210-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69210-131">NOTES</span></span>

## <span data-ttu-id="69210-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69210-132">RELATED LINKS</span></span>

[<span data-ttu-id="69210-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="69210-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="69210-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="69210-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

