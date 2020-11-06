---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 3041d7a25ad87e6e2b9242043645a66219ac7e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498745"
---
# <span data-ttu-id="a8730-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a8730-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="a8730-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8730-102">SYNOPSIS</span></span>
<span data-ttu-id="a8730-103">Gibt Informationen zu Azure SQL-Synchronisierungs-Agents zurück.</span><span class="sxs-lookup"><span data-stu-id="a8730-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8730-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8730-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8730-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8730-105">DESCRIPTION</span></span>
<span data-ttu-id="a8730-106">Das Cmdlet " **Get-AzureRmSqlSyncAgent** " gibt Informationen zu einem oder mehreren Azure SQL-Synchronisierungs-Agents zurück.</span><span class="sxs-lookup"><span data-stu-id="a8730-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="a8730-107">Geben Sie den Namen eines Synchronisierungs-Agents an, um Informationen nur für diesen Synchronisierungs-Agent anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a8730-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="a8730-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8730-108">EXAMPLES</span></span>

### <span data-ttu-id="a8730-109">Beispiel 1: Abrufen aller Instanzen des Azure SQL-Synchronisierungs-Agents, die einem Azure SQL Server zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="a8730-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="a8730-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Synchronisierungs-Agents ab, die einem Azure SQL Server zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="a8730-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="a8730-111">Beispiel 2: Abrufen von Informationen zu einem Azure SQL-Synchronisierungs-Agent</span><span class="sxs-lookup"><span data-stu-id="a8730-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="a8730-112">Dieser Befehl ruft Informationen zum Azure SQL-Daten Bank Synchronisierungs-Agent mit dem Namen "SyncAgent01" ab.</span><span class="sxs-lookup"><span data-stu-id="a8730-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="a8730-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8730-113">PARAMETERS</span></span>

### <span data-ttu-id="a8730-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8730-114">-DefaultProfile</span></span>
<span data-ttu-id="a8730-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a8730-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8730-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a8730-116">-Name</span></span>
<span data-ttu-id="a8730-117">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="a8730-117">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8730-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8730-118">-ResourceGroupName</span></span>
<span data-ttu-id="a8730-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8730-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8730-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="a8730-120">-ServerName</span></span>
<span data-ttu-id="a8730-121">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="a8730-121">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8730-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8730-122">CommonParameters</span></span>
<span data-ttu-id="a8730-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8730-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8730-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8730-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8730-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8730-125">INPUTS</span></span>

### <span data-ttu-id="a8730-126">Keine</span><span class="sxs-lookup"><span data-stu-id="a8730-126">None</span></span>
<span data-ttu-id="a8730-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a8730-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8730-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8730-128">OUTPUTS</span></span>

### <span data-ttu-id="a8730-129">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="a8730-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="a8730-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8730-130">NOTES</span></span>

## <span data-ttu-id="a8730-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8730-131">RELATED LINKS</span></span>

[<span data-ttu-id="a8730-132">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a8730-132">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="a8730-133">Neu – AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a8730-133">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

