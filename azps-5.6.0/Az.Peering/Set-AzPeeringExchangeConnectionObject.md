---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d935f980b776ad6f61fe705a14e0da2a375d1e1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937568"
---
# <span data-ttu-id="a8da0-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="a8da0-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="a8da0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8da0-102">SYNOPSIS</span></span>
<span data-ttu-id="a8da0-103">Legt die Exchange-Verbindungsinformationen fest oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="a8da0-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="a8da0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8da0-104">SYNTAX</span></span>

### <span data-ttu-id="a8da0-105">IPv4Address (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8da0-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8da0-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="a8da0-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8da0-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="a8da0-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8da0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8da0-108">DESCRIPTION</span></span>
<span data-ttu-id="a8da0-109">In Verbindung mit Update-AzPeering verwendet, handelt es sich um einen Speichervorgang, der nur mit beibehalten `Update-AzPeering` wird.</span><span class="sxs-lookup"><span data-stu-id="a8da0-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="a8da0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a8da0-110">EXAMPLES</span></span>

### <span data-ttu-id="a8da0-111">Aktualisieren des Md5-Hashs</span><span class="sxs-lookup"><span data-stu-id="a8da0-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="a8da0-112">Aktualisiert den Md5-Hash für die erste Verbindung im Peeringobjekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a8da0-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="a8da0-113">Aktualisieren der Bgp-Sitzungsadresse</span><span class="sxs-lookup"><span data-stu-id="a8da0-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="a8da0-114">Aktualisiert die Peeringadresse für die erste Verbindung im Peeringobjekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a8da0-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="a8da0-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a8da0-115">PARAMETERS</span></span>

### <span data-ttu-id="a8da0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8da0-116">-DefaultProfile</span></span>
<span data-ttu-id="a8da0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8da0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8da0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8da0-118">-InputObject</span></span>
<span data-ttu-id="a8da0-119">Das Exchange-Verbindungsobjekt</span><span class="sxs-lookup"><span data-stu-id="a8da0-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8da0-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="a8da0-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="a8da0-121">Das maximal angekündigte IPv4</span><span class="sxs-lookup"><span data-stu-id="a8da0-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8da0-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="a8da0-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="a8da0-123">Die maximal angekündigte IPv6</span><span class="sxs-lookup"><span data-stu-id="a8da0-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8da0-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="a8da0-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="a8da0-125">Der MD5-Authentifizierungsschlüssel für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a8da0-125">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8da0-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="a8da0-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="a8da0-127">Die IPv4-Adresse der Peersitzung</span><span class="sxs-lookup"><span data-stu-id="a8da0-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8da0-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="a8da0-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="a8da0-129">Die IPv6-Adresse der Peersitzung</span><span class="sxs-lookup"><span data-stu-id="a8da0-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8da0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8da0-130">CommonParameters</span></span>
<span data-ttu-id="a8da0-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8da0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8da0-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8da0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8da0-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a8da0-133">INPUTS</span></span>

### <span data-ttu-id="a8da0-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="a8da0-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="a8da0-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a8da0-135">OUTPUTS</span></span>

### <span data-ttu-id="a8da0-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="a8da0-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="a8da0-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a8da0-137">NOTES</span></span>

## <span data-ttu-id="a8da0-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a8da0-138">RELATED LINKS</span></span>
