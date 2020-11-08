---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003852"
---
# <span data-ttu-id="44253-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="44253-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="44253-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44253-102">SYNOPSIS</span></span>
<span data-ttu-id="44253-103">Erstellen Sie ein neues CosmosDB Location-Objekt (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="44253-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="44253-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44253-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44253-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44253-105">DESCRIPTION</span></span>
<span data-ttu-id="44253-106">Erstellen Sie ein neues CosmosDB Location-Objekt (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="44253-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="44253-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44253-107">EXAMPLES</span></span>

### <span data-ttu-id="44253-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44253-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="44253-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="44253-109">PARAMETERS</span></span>

### <span data-ttu-id="44253-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44253-110">-DefaultProfile</span></span>
<span data-ttu-id="44253-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44253-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44253-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="44253-112">-FailoverPriority</span></span>
<span data-ttu-id="44253-113">Failover-Priorität des Standorts.</span><span class="sxs-lookup"><span data-stu-id="44253-113">Failover priority of the location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44253-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="44253-114">-IsZoneRedundant</span></span>
<span data-ttu-id="44253-115">Boolescher Wert, der angibt, ob es sich bei diesem Bereich um eine AvailabilityZone handelt.</span><span class="sxs-lookup"><span data-stu-id="44253-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44253-116">-Standortname</span><span class="sxs-lookup"><span data-stu-id="44253-116">-LocationName</span></span>
<span data-ttu-id="44253-117">Der Name der Position in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="44253-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="44253-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44253-118">CommonParameters</span></span>
<span data-ttu-id="44253-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44253-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44253-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44253-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44253-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44253-121">INPUTS</span></span>

### <span data-ttu-id="44253-122">Keine</span><span class="sxs-lookup"><span data-stu-id="44253-122">None</span></span>

## <span data-ttu-id="44253-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44253-123">OUTPUTS</span></span>

### <span data-ttu-id="44253-124">Microsoft. Azure. Commands. CosmosDB. Models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="44253-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="44253-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="44253-125">NOTES</span></span>

## <span data-ttu-id="44253-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44253-126">RELATED LINKS</span></span>
