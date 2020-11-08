---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008583"
---
# <span data-ttu-id="e6861-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="e6861-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="e6861-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6861-102">SYNOPSIS</span></span>
<span data-ttu-id="e6861-103">Erstellen Sie ein neues CosmosDB Location-Objekt (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="e6861-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="e6861-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6861-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6861-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6861-105">DESCRIPTION</span></span>
<span data-ttu-id="e6861-106">Erstellen Sie ein neues CosmosDB Location-Objekt (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="e6861-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="e6861-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6861-107">EXAMPLES</span></span>

### <span data-ttu-id="e6861-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6861-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="e6861-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6861-109">PARAMETERS</span></span>

### <span data-ttu-id="e6861-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6861-110">-DefaultProfile</span></span>
<span data-ttu-id="e6861-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e6861-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6861-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="e6861-112">-FailoverPriority</span></span>
<span data-ttu-id="e6861-113">Failover-Priorität des Standorts.</span><span class="sxs-lookup"><span data-stu-id="e6861-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="e6861-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e6861-114">-IsZoneRedundant</span></span>
<span data-ttu-id="e6861-115">Boolescher Wert, der angibt, ob es sich bei diesem Bereich um eine AvailabilityZone handelt.</span><span class="sxs-lookup"><span data-stu-id="e6861-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="e6861-116">-Standortname</span><span class="sxs-lookup"><span data-stu-id="e6861-116">-LocationName</span></span>
<span data-ttu-id="e6861-117">Der Name der Position in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e6861-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="e6861-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6861-118">CommonParameters</span></span>
<span data-ttu-id="e6861-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6861-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6861-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6861-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6861-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6861-121">INPUTS</span></span>

### <span data-ttu-id="e6861-122">Keine</span><span class="sxs-lookup"><span data-stu-id="e6861-122">None</span></span>

## <span data-ttu-id="e6861-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6861-123">OUTPUTS</span></span>

### <span data-ttu-id="e6861-124">Microsoft. Azure. Commands. CosmosDB. Models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="e6861-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="e6861-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6861-125">NOTES</span></span>

## <span data-ttu-id="e6861-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6861-126">RELATED LINKS</span></span>
