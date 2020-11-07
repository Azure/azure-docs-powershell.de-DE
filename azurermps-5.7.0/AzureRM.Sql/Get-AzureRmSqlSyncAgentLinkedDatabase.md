---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 8fceaa92f14c6218d723b7fa7153970f118855a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664152"
---
# <span data-ttu-id="cee8a-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="cee8a-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="cee8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cee8a-102">SYNOPSIS</span></span>
<span data-ttu-id="cee8a-103">Gibt Informationen zu SQL Server-Datenbanken zurück, die von einem Synchronisierungs-Agent verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cee8a-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cee8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cee8a-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cee8a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cee8a-105">DESCRIPTION</span></span>
<span data-ttu-id="cee8a-106">Das Cmdlet " **Get-AzureRmSqlSyncAgentLinkedDatabases** " gibt Informationen zu SQL Server-Datenbanken zurück, die von einem Synchronisierungs-Agent verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cee8a-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="cee8a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cee8a-107">EXAMPLES</span></span>

### <span data-ttu-id="cee8a-108">Beispiel 1: Abrufen der verknüpften SQL Server-Datenbanken für einen Azure SQL-Synchronisierungs-Agent</span><span class="sxs-lookup"><span data-stu-id="cee8a-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="cee8a-109">Dieser Befehl gibt die verknüpften SQL Server-Datenbanken zurück, die mit einem Azure SQL-Synchronisierungs-Agent verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cee8a-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="cee8a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cee8a-110">PARAMETERS</span></span>

### <span data-ttu-id="cee8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee8a-111">-DefaultProfile</span></span>
<span data-ttu-id="cee8a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cee8a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cee8a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee8a-113">-ResourceGroupName</span></span>
<span data-ttu-id="cee8a-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cee8a-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="cee8a-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="cee8a-115">-ServerName</span></span>
<span data-ttu-id="cee8a-116">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="cee8a-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="cee8a-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="cee8a-117">-SyncAgentName</span></span>
<span data-ttu-id="cee8a-118">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="cee8a-118">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cee8a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee8a-119">CommonParameters</span></span>
<span data-ttu-id="cee8a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee8a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee8a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cee8a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee8a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cee8a-122">INPUTS</span></span>

### <span data-ttu-id="cee8a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="cee8a-123">None</span></span>
<span data-ttu-id="cee8a-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="cee8a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cee8a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cee8a-125">OUTPUTS</span></span>

### <span data-ttu-id="cee8a-126">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cee8a-126">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="cee8a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="cee8a-127">NOTES</span></span>

## <span data-ttu-id="cee8a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cee8a-128">RELATED LINKS</span></span>
