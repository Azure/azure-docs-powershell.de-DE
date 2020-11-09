---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299386"
---
# <span data-ttu-id="c8002-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="c8002-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="c8002-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8002-102">SYNOPSIS</span></span>
<span data-ttu-id="c8002-103">Erstellt einen neuen CosmosDB Cassandra-Cluster Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c8002-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="c8002-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8002-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8002-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8002-105">DESCRIPTION</span></span>
<span data-ttu-id="c8002-106">Der **New-AzCosmosDBCassandraClusterKey** erstellt einen neuen CosmosDB Cassandra-Cluster Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c8002-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="c8002-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8002-107">EXAMPLES</span></span>

### <span data-ttu-id="c8002-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c8002-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="c8002-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8002-109">PARAMETERS</span></span>

### <span data-ttu-id="c8002-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8002-110">-DefaultProfile</span></span>
<span data-ttu-id="c8002-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8002-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8002-112">-Name</span><span class="sxs-lookup"><span data-stu-id="c8002-112">-Name</span></span>
<span data-ttu-id="c8002-113">Name des Cassandra-Cluster Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c8002-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="c8002-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c8002-114">-OrderBy</span></span>
<span data-ttu-id="c8002-115">Bestellung des Cassandra-Cluster Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c8002-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="c8002-116">Mögliche Werte sind: "ASC"; "DESC"</span><span class="sxs-lookup"><span data-stu-id="c8002-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="c8002-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8002-117">CommonParameters</span></span>
<span data-ttu-id="c8002-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8002-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8002-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8002-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8002-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8002-120">INPUTS</span></span>

### <span data-ttu-id="c8002-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c8002-121">None</span></span>

## <span data-ttu-id="c8002-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8002-122">OUTPUTS</span></span>

### <span data-ttu-id="c8002-123">Microsoft. Azure. Commands. CosmosDB. Models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="c8002-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="c8002-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8002-124">NOTES</span></span>

## <span data-ttu-id="c8002-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8002-125">RELATED LINKS</span></span>
