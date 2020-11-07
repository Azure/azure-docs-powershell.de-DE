---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 11c444e92c6377e0a0df5aaa324ee162647784a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664313"
---
# <span data-ttu-id="cb11d-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="cb11d-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="cb11d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb11d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb11d-103">Gibt Informationen zu SQL Server-Datenbanken zurück, die von einem Synchronisierungs-Agent verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cb11d-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb11d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb11d-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb11d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb11d-105">DESCRIPTION</span></span>
<span data-ttu-id="cb11d-106">Das Cmdlet " **Get-AzureRmSqlSyncAgentLinkedDatabases** " gibt Informationen zu SQL Server-Datenbanken zurück, die von einem Synchronisierungs-Agent verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cb11d-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="cb11d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb11d-107">EXAMPLES</span></span>

### <span data-ttu-id="cb11d-108">Beispiel 1: Abrufen der verknüpften SQL Server-Datenbanken für einen Azure SQL-Synchronisierungs-Agent</span><span class="sxs-lookup"><span data-stu-id="cb11d-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="cb11d-109">Dieser Befehl gibt die verknüpften SQL Server-Datenbanken zurück, die mit einem Azure SQL-Synchronisierungs-Agent verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cb11d-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="cb11d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb11d-110">PARAMETERS</span></span>

### <span data-ttu-id="cb11d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb11d-111">-DefaultProfile</span></span>
<span data-ttu-id="cb11d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cb11d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb11d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb11d-113">-ResourceGroupName</span></span>
<span data-ttu-id="cb11d-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cb11d-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb11d-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="cb11d-115">-ServerName</span></span>
<span data-ttu-id="cb11d-116">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="cb11d-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="cb11d-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="cb11d-117">-SyncAgentName</span></span>
<span data-ttu-id="cb11d-118">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="cb11d-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb11d-119">CommonParameters</span></span>
<span data-ttu-id="cb11d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb11d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb11d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb11d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb11d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb11d-122">INPUTS</span></span>

### <span data-ttu-id="cb11d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cb11d-123">System.String</span></span>

## <span data-ttu-id="cb11d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb11d-124">OUTPUTS</span></span>

### <span data-ttu-id="cb11d-125">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cb11d-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="cb11d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb11d-126">NOTES</span></span>

## <span data-ttu-id="cb11d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb11d-127">RELATED LINKS</span></span>
