---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173140"
---
# <span data-ttu-id="c57aa-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c57aa-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="c57aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c57aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c57aa-103">Erstellt eine im Arbeitsspeicher PSObject, die zum Erstellen oder Ändern eines Peerings verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c57aa-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="c57aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c57aa-104">SYNTAX</span></span>

### <span data-ttu-id="c57aa-105">IPv4Address (Standard)</span><span class="sxs-lookup"><span data-stu-id="c57aa-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c57aa-106">IPv6</span><span class="sxs-lookup"><span data-stu-id="c57aa-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c57aa-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="c57aa-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c57aa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c57aa-108">DESCRIPTION</span></span>
<span data-ttu-id="c57aa-109">Erstellt eine im Speicher PSObject</span><span class="sxs-lookup"><span data-stu-id="c57aa-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="c57aa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c57aa-110">EXAMPLES</span></span>

### <span data-ttu-id="c57aa-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c57aa-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="c57aa-112">Lokales Verbindungsobjekt</span><span class="sxs-lookup"><span data-stu-id="c57aa-112">Local connection object</span></span>

## <span data-ttu-id="c57aa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c57aa-113">PARAMETERS</span></span>

### <span data-ttu-id="c57aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57aa-114">-DefaultProfile</span></span>
<span data-ttu-id="c57aa-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c57aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c57aa-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="c57aa-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="c57aa-117">Das maximal angekündigte IPv4</span><span class="sxs-lookup"><span data-stu-id="c57aa-117">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="c57aa-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="c57aa-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="c57aa-119">Das maximal angekündigte IPv6</span><span class="sxs-lookup"><span data-stu-id="c57aa-119">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="c57aa-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="c57aa-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="c57aa-121">Der MD5-Authentifizierungsschlüssel für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c57aa-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="c57aa-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="c57aa-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="c57aa-123">Die ID der Peering-Einrichtung, die auf gefunden wurde https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="c57aa-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="c57aa-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="c57aa-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="c57aa-125">Die IPv4-Adresse der Peer Sitzung</span><span class="sxs-lookup"><span data-stu-id="c57aa-125">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="c57aa-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="c57aa-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="c57aa-127">Die IPv6-Adresse der Peer Sitzung</span><span class="sxs-lookup"><span data-stu-id="c57aa-127">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="c57aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57aa-128">CommonParameters</span></span>
<span data-ttu-id="c57aa-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c57aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57aa-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c57aa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57aa-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c57aa-131">INPUTS</span></span>

### <span data-ttu-id="c57aa-132">Keine</span><span class="sxs-lookup"><span data-stu-id="c57aa-132">None</span></span>

## <span data-ttu-id="c57aa-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c57aa-133">OUTPUTS</span></span>

### <span data-ttu-id="c57aa-134">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="c57aa-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="c57aa-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c57aa-135">NOTES</span></span>

## <span data-ttu-id="c57aa-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c57aa-136">RELATED LINKS</span></span>
