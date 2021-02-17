---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156169"
---
# <span data-ttu-id="32d5e-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="32d5e-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="32d5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="32d5e-103">Gibt Informationen zu SQL Server Datenbanken zurück, die von einem Synchronisierungs-Agent verknüpft wurden.</span><span class="sxs-lookup"><span data-stu-id="32d5e-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="32d5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32d5e-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32d5e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32d5e-105">DESCRIPTION</span></span>
<span data-ttu-id="32d5e-106">Das **Cmdlet "Get-AzSqlSyncAgentLinkedDatabase"** gibt Informationen zu SQL Server, die von einem Synchronisierungs-Agent verknüpft wurden.</span><span class="sxs-lookup"><span data-stu-id="32d5e-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="32d5e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32d5e-107">EXAMPLES</span></span>

### <span data-ttu-id="32d5e-108">Beispiel 1: Die verknüpften SQL Server für einen Azure SQL-Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="32d5e-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="32d5e-109">Im folgenden Beispiel werden die verknüpften SQL Server zurückgegeben, die von einem Azure SQL-Agent verknüpft wurden.</span><span class="sxs-lookup"><span data-stu-id="32d5e-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="32d5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32d5e-110">PARAMETERS</span></span>

### <span data-ttu-id="32d5e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d5e-111">-DefaultProfile</span></span>
<span data-ttu-id="32d5e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="32d5e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32d5e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d5e-113">-ResourceGroupName</span></span>
<span data-ttu-id="32d5e-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="32d5e-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="32d5e-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32d5e-115">-ServerName</span></span>
<span data-ttu-id="32d5e-116">Der Name des Azure-SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="32d5e-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="32d5e-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="32d5e-117">-SyncAgentName</span></span>
<span data-ttu-id="32d5e-118">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="32d5e-118">The sync agent name.</span></span>

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

### <span data-ttu-id="32d5e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d5e-119">CommonParameters</span></span>
<span data-ttu-id="32d5e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d5e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d5e-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32d5e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d5e-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32d5e-122">INPUTS</span></span>

### <span data-ttu-id="32d5e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="32d5e-123">System.String</span></span>

## <span data-ttu-id="32d5e-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32d5e-124">OUTPUTS</span></span>

### <span data-ttu-id="32d5e-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="32d5e-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="32d5e-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="32d5e-126">NOTES</span></span>

## <span data-ttu-id="32d5e-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="32d5e-127">RELATED LINKS</span></span>
