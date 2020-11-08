---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003839"
---
# <span data-ttu-id="db117-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="db117-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="db117-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db117-102">SYNOPSIS</span></span>
<span data-ttu-id="db117-103">Erstellt ein neues CosmosDB SQL-UniqueKey-Objekt.</span><span class="sxs-lookup"><span data-stu-id="db117-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="db117-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db117-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db117-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db117-105">DESCRIPTION</span></span>
<span data-ttu-id="db117-106">Das Cmdlet **New-AzCosmosDBSqlUniqueKey** erstellt ein neues Objekt vom Typ PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="db117-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="db117-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db117-107">EXAMPLES</span></span>

### <span data-ttu-id="db117-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="db117-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="db117-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db117-109">PARAMETERS</span></span>

### <span data-ttu-id="db117-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db117-110">-DefaultProfile</span></span>
<span data-ttu-id="db117-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db117-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db117-112">-Path</span><span class="sxs-lookup"><span data-stu-id="db117-112">-Path</span></span>
<span data-ttu-id="db117-113">Array mit einer Zeichenfolge von Path-Werten</span><span class="sxs-lookup"><span data-stu-id="db117-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db117-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db117-114">CommonParameters</span></span>
<span data-ttu-id="db117-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db117-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db117-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db117-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db117-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db117-117">INPUTS</span></span>

### <span data-ttu-id="db117-118">Keine</span><span class="sxs-lookup"><span data-stu-id="db117-118">None</span></span>

## <span data-ttu-id="db117-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db117-119">OUTPUTS</span></span>

### <span data-ttu-id="db117-120">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="db117-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="db117-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="db117-121">NOTES</span></span>

## <span data-ttu-id="db117-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db117-122">RELATED LINKS</span></span>
