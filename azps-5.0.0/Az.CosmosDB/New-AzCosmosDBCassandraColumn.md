---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299385"
---
# <span data-ttu-id="38bd8-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="38bd8-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="38bd8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="38bd8-103">Erstellt eine neue CosmosDB Cassandra-Spalte.</span><span class="sxs-lookup"><span data-stu-id="38bd8-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="38bd8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38bd8-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38bd8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="38bd8-106">Das **New-AzCosmosDBCassandraColumn** erstellt eine neue CosmosDB Cassandra-Spalte.</span><span class="sxs-lookup"><span data-stu-id="38bd8-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="38bd8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38bd8-107">EXAMPLES</span></span>

### <span data-ttu-id="38bd8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38bd8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="38bd8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="38bd8-109">PARAMETERS</span></span>

### <span data-ttu-id="38bd8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bd8-110">-DefaultProfile</span></span>
<span data-ttu-id="38bd8-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38bd8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38bd8-112">-Name</span><span class="sxs-lookup"><span data-stu-id="38bd8-112">-Name</span></span>
<span data-ttu-id="38bd8-113">Der Name der Cassandra-Spalte.</span><span class="sxs-lookup"><span data-stu-id="38bd8-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="38bd8-114">-Typ</span><span class="sxs-lookup"><span data-stu-id="38bd8-114">-Type</span></span>
<span data-ttu-id="38bd8-115">Der Typ der Cassandra-Spalte.</span><span class="sxs-lookup"><span data-stu-id="38bd8-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="38bd8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bd8-116">CommonParameters</span></span>
<span data-ttu-id="38bd8-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38bd8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bd8-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38bd8-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bd8-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38bd8-119">INPUTS</span></span>

### <span data-ttu-id="38bd8-120">Keine</span><span class="sxs-lookup"><span data-stu-id="38bd8-120">None</span></span>

## <span data-ttu-id="38bd8-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38bd8-121">OUTPUTS</span></span>

### <span data-ttu-id="38bd8-122">Microsoft. Azure. Commands. CosmosDB. Models. PSColumn</span><span class="sxs-lookup"><span data-stu-id="38bd8-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="38bd8-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="38bd8-123">NOTES</span></span>

## <span data-ttu-id="38bd8-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38bd8-124">RELATED LINKS</span></span>
