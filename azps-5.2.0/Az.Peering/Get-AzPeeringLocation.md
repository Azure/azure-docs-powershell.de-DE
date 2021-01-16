---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: 233cf87eed682919df8ca0ae38fefaec5964942c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301443"
---
# <span data-ttu-id="d9abc-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="d9abc-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="d9abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9abc-102">SYNOPSIS</span></span>
<span data-ttu-id="d9abc-103">Ruft die von Microsoft angebotenen Peeringstandorte ab.</span><span class="sxs-lookup"><span data-stu-id="d9abc-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="d9abc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9abc-104">SYNTAX</span></span>

### <span data-ttu-id="d9abc-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9abc-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9abc-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="d9abc-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9abc-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="d9abc-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9abc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9abc-108">DESCRIPTION</span></span>
<span data-ttu-id="d9abc-109">Ruft die Peeringeinrichtungen ab, an denen Benutzer eine Verbindung mit anderen ARM.</span><span class="sxs-lookup"><span data-stu-id="d9abc-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="d9abc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9abc-110">EXAMPLES</span></span>

### <span data-ttu-id="d9abc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9abc-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="d9abc-112">Dies ist eine lange Liste von Speicherorten.</span><span class="sxs-lookup"><span data-stu-id="d9abc-112">Its a long list of locations.</span></span> <span data-ttu-id="d9abc-113">Ruft alle direkten Peeringeinrichtungen ab.</span><span class="sxs-lookup"><span data-stu-id="d9abc-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="d9abc-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d9abc-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="d9abc-115">Ruft den Exchange-Peering-Standort für Honolulu ab.</span><span class="sxs-lookup"><span data-stu-id="d9abc-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="d9abc-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d9abc-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="d9abc-117">Ruft den Exchange-Peering-Speicherort für die Peeringeinrichtungs-ID 71 ab.</span><span class="sxs-lookup"><span data-stu-id="d9abc-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="d9abc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9abc-118">PARAMETERS</span></span>

### <span data-ttu-id="d9abc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9abc-119">-DefaultProfile</span></span>
<span data-ttu-id="d9abc-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9abc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9abc-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="d9abc-121">-DirectPeeringType</span></span>
<span data-ttu-id="d9abc-122">Wählen Sie "Edge", "CDN" und "Transit" aus.</span><span class="sxs-lookup"><span data-stu-id="d9abc-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9abc-123">-Kind</span><span class="sxs-lookup"><span data-stu-id="d9abc-123">-Kind</span></span>
<span data-ttu-id="d9abc-124">Zeigt alle Peeringressourcen nach Art an.</span><span class="sxs-lookup"><span data-stu-id="d9abc-124">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9abc-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="d9abc-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="d9abc-126">Die PeeringDB.com Einrichtungs-ID</span><span class="sxs-lookup"><span data-stu-id="d9abc-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9abc-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="d9abc-127">-PeeringLocation</span></span>
<span data-ttu-id="d9abc-128">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d9abc-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9abc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9abc-129">CommonParameters</span></span>
<span data-ttu-id="d9abc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9abc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9abc-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9abc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9abc-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9abc-132">INPUTS</span></span>

### <span data-ttu-id="d9abc-133">Keine</span><span class="sxs-lookup"><span data-stu-id="d9abc-133">None</span></span>

## <span data-ttu-id="d9abc-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9abc-134">OUTPUTS</span></span>

### <span data-ttu-id="d9abc-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="d9abc-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="d9abc-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d9abc-136">NOTES</span></span>

## <span data-ttu-id="d9abc-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d9abc-137">RELATED LINKS</span></span>
