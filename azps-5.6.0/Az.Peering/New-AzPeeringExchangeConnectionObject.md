---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c4e57d3d7945f4ae06fc2461e660945bf7edfd6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937651"
---
# <span data-ttu-id="14582-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="14582-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="14582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14582-102">SYNOPSIS</span></span>
<span data-ttu-id="14582-103">Erstellt ein im Arbeitsspeicher vorhandenes PSObject, das zum Erstellen oder Ändern eines Peerings verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14582-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="14582-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14582-104">SYNTAX</span></span>

### <span data-ttu-id="14582-105">IPv4Address (Standard)</span><span class="sxs-lookup"><span data-stu-id="14582-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14582-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="14582-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14582-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="14582-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14582-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14582-108">DESCRIPTION</span></span>
<span data-ttu-id="14582-109">Erstellt ein im Arbeitsspeicher gespeichertes PSObject</span><span class="sxs-lookup"><span data-stu-id="14582-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="14582-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14582-110">EXAMPLES</span></span>

### <span data-ttu-id="14582-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14582-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="14582-112">Lokales Verbindungsobjekt</span><span class="sxs-lookup"><span data-stu-id="14582-112">Local connection object</span></span>

## <span data-ttu-id="14582-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="14582-113">PARAMETERS</span></span>

### <span data-ttu-id="14582-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14582-114">-DefaultProfile</span></span>
<span data-ttu-id="14582-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14582-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14582-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="14582-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="14582-117">Das maximal angekündigte IPv4</span><span class="sxs-lookup"><span data-stu-id="14582-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14582-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="14582-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="14582-119">Die maximal angekündigte IPv6</span><span class="sxs-lookup"><span data-stu-id="14582-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14582-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="14582-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="14582-121">Der MD5-Authentifizierungsschlüssel für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="14582-121">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14582-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="14582-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="14582-123">Die Id der Peeringeinrichtung, die auf https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="14582-123">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14582-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="14582-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="14582-125">Die IPv4-Adresse der Peersitzung</span><span class="sxs-lookup"><span data-stu-id="14582-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14582-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="14582-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="14582-127">Die IPv6-Adresse der Peersitzung</span><span class="sxs-lookup"><span data-stu-id="14582-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14582-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14582-128">CommonParameters</span></span>
<span data-ttu-id="14582-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14582-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14582-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14582-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14582-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14582-131">INPUTS</span></span>

### <span data-ttu-id="14582-132">Keine</span><span class="sxs-lookup"><span data-stu-id="14582-132">None</span></span>

## <span data-ttu-id="14582-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14582-133">OUTPUTS</span></span>

### <span data-ttu-id="14582-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="14582-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="14582-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="14582-135">NOTES</span></span>

## <span data-ttu-id="14582-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="14582-136">RELATED LINKS</span></span>
