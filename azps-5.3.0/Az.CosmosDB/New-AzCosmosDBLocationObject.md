---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470726"
---
# <span data-ttu-id="406d8-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="406d8-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="406d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="406d8-102">SYNOPSIS</span></span>
<span data-ttu-id="406d8-103">Erstellen Sie ein neues Standortobjekt (PSLocation) aus.</span><span class="sxs-lookup"><span data-stu-id="406d8-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="406d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="406d8-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="406d8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="406d8-105">DESCRIPTION</span></span>
<span data-ttu-id="406d8-106">Erstellen Sie ein neues Standortobjekt (PSLocation) aus.</span><span class="sxs-lookup"><span data-stu-id="406d8-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="406d8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="406d8-107">EXAMPLES</span></span>

### <span data-ttu-id="406d8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="406d8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="406d8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="406d8-109">PARAMETERS</span></span>

### <span data-ttu-id="406d8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406d8-110">-DefaultProfile</span></span>
<span data-ttu-id="406d8-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="406d8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="406d8-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="406d8-112">-FailoverPriority</span></span>
<span data-ttu-id="406d8-113">Failoverpriorität des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="406d8-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="406d8-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="406d8-114">-IsZoneRedundant</span></span>
<span data-ttu-id="406d8-115">Boolesch, um anzugeben, ob es sich bei dieser Region um einen AvailabilityZone-Bereich handelt.</span><span class="sxs-lookup"><span data-stu-id="406d8-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="406d8-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="406d8-116">-LocationName</span></span>
<span data-ttu-id="406d8-117">Der Name der Position in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="406d8-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="406d8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406d8-118">CommonParameters</span></span>
<span data-ttu-id="406d8-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="406d8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406d8-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="406d8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406d8-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="406d8-121">INPUTS</span></span>

### <span data-ttu-id="406d8-122">Keine</span><span class="sxs-lookup"><span data-stu-id="406d8-122">None</span></span>

## <span data-ttu-id="406d8-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="406d8-123">OUTPUTS</span></span>

### <span data-ttu-id="406d8-124">Microsoft.Azure.Commands.UmsDB.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="406d8-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="406d8-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="406d8-125">NOTES</span></span>

## <span data-ttu-id="406d8-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="406d8-126">RELATED LINKS</span></span>
