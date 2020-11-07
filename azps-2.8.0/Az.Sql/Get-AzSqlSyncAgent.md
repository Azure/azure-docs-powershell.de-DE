---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: f74a031079ab35e1584d8c7e5536e2605ea665ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825503"
---
# <span data-ttu-id="31ab7-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="31ab7-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="31ab7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="31ab7-103">Gibt Informationen zu Azure SQL-Synchronisierungs-Agents zurück.</span><span class="sxs-lookup"><span data-stu-id="31ab7-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="31ab7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31ab7-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31ab7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="31ab7-106">Das Cmdlet " **Get-AzSqlSyncAgent** " gibt Informationen zu einem oder mehreren Azure SQL-Synchronisierungs-Agents zurück.</span><span class="sxs-lookup"><span data-stu-id="31ab7-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="31ab7-107">Geben Sie den Namen eines Synchronisierungs-Agents an, um Informationen nur für diesen Synchronisierungs-Agent anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="31ab7-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="31ab7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31ab7-108">EXAMPLES</span></span>

### <span data-ttu-id="31ab7-109">Beispiel 1: Abrufen aller Instanzen des Azure SQL-Synchronisierungs-Agents, die einem Azure SQL Server zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="31ab7-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="31ab7-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Synchronisierungs-Agents ab, die einem Azure SQL Server zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="31ab7-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="31ab7-111">Beispiel 2: Abrufen von Informationen zu einem Azure SQL-Synchronisierungs-Agent</span><span class="sxs-lookup"><span data-stu-id="31ab7-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="31ab7-112">Dieser Befehl ruft Informationen zum Azure SQL-Daten Bank Synchronisierungs-Agent mit dem Namen "SyncAgent01" ab.</span><span class="sxs-lookup"><span data-stu-id="31ab7-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="31ab7-113">Beispiel 3: Abrufen aller Instanzen des Azure SQL-Synchronisierungs-Agents, die einem Azure SQL Server mithilfe von Filtern zugewiesen wurden</span><span class="sxs-lookup"><span data-stu-id="31ab7-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="31ab7-114">Dieser Befehl ruft Informationen zu allen Azure SQL-Synchronisierungs-Agents ab, die einem Azure SQL Server zugewiesen sind, die mit "SyncAgent" beginnen.</span><span class="sxs-lookup"><span data-stu-id="31ab7-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="31ab7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="31ab7-115">PARAMETERS</span></span>

### <span data-ttu-id="31ab7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ab7-116">-DefaultProfile</span></span>
<span data-ttu-id="31ab7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="31ab7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31ab7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="31ab7-118">-Name</span></span>
<span data-ttu-id="31ab7-119">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="31ab7-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="31ab7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ab7-120">-ResourceGroupName</span></span>
<span data-ttu-id="31ab7-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="31ab7-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="31ab7-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="31ab7-122">-ServerName</span></span>
<span data-ttu-id="31ab7-123">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="31ab7-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="31ab7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ab7-124">CommonParameters</span></span>
<span data-ttu-id="31ab7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ab7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ab7-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31ab7-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ab7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31ab7-127">INPUTS</span></span>

### <span data-ttu-id="31ab7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="31ab7-128">System.String</span></span>

## <span data-ttu-id="31ab7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31ab7-129">OUTPUTS</span></span>

### <span data-ttu-id="31ab7-130">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="31ab7-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="31ab7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="31ab7-131">NOTES</span></span>

## <span data-ttu-id="31ab7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31ab7-132">RELATED LINKS</span></span>

[<span data-ttu-id="31ab7-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="31ab7-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="31ab7-134">Neu – AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="31ab7-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

