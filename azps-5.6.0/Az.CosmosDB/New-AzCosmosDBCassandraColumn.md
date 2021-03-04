---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 634a6a8e1e6b921703603ee7f2bfd345aa64608c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948000"
---
# <span data-ttu-id="43466-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="43466-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="43466-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43466-102">SYNOPSIS</span></span>
<span data-ttu-id="43466-103">Erstellt eine neue Spalte "CosmosDB-Kassandra".</span><span class="sxs-lookup"><span data-stu-id="43466-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="43466-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43466-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43466-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43466-105">DESCRIPTION</span></span>
<span data-ttu-id="43466-106">Die **New-AzCosmosDBCassandraColumn** erstellt eine neue Spalte "CosmosDB-Kassandra".</span><span class="sxs-lookup"><span data-stu-id="43466-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="43466-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43466-107">EXAMPLES</span></span>

### <span data-ttu-id="43466-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43466-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="43466-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43466-109">PARAMETERS</span></span>

### <span data-ttu-id="43466-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43466-110">-DefaultProfile</span></span>
<span data-ttu-id="43466-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43466-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43466-112">-Name</span><span class="sxs-lookup"><span data-stu-id="43466-112">-Name</span></span>
<span data-ttu-id="43466-113">Name der Spalte "Kassandra".</span><span class="sxs-lookup"><span data-stu-id="43466-113">Name of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43466-114">-Type</span><span class="sxs-lookup"><span data-stu-id="43466-114">-Type</span></span>
<span data-ttu-id="43466-115">Typ der Spalte "Kassandra".</span><span class="sxs-lookup"><span data-stu-id="43466-115">Type of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43466-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43466-116">CommonParameters</span></span>
<span data-ttu-id="43466-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43466-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43466-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43466-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43466-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43466-119">INPUTS</span></span>

### <span data-ttu-id="43466-120">Keine</span><span class="sxs-lookup"><span data-stu-id="43466-120">None</span></span>

## <span data-ttu-id="43466-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43466-121">OUTPUTS</span></span>

### <span data-ttu-id="43466-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="43466-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="43466-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="43466-123">NOTES</span></span>

## <span data-ttu-id="43466-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="43466-124">RELATED LINKS</span></span>
