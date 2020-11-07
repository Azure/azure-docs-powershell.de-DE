---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c09ff4ad7762eafc18d7890f9611c9b989841c95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846331"
---
# <span data-ttu-id="88679-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="88679-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="88679-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88679-102">SYNOPSIS</span></span>
<span data-ttu-id="88679-103">Legt die Exchange-Verbindungsinformationen fest oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="88679-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="88679-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88679-104">SYNTAX</span></span>

### <span data-ttu-id="88679-105">IPv6 (Standard)</span><span class="sxs-lookup"><span data-stu-id="88679-105">IPv6Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88679-106">IPv4Address</span><span class="sxs-lookup"><span data-stu-id="88679-106">IPv4Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88679-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="88679-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88679-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88679-108">DESCRIPTION</span></span>
<span data-ttu-id="88679-109">In Verbindung mit Update-AzPeering verwendet, handelt es sich um einen Arbeitsspeicher Vorgang, der nur mit beibehalten wird `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="88679-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="88679-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88679-110">EXAMPLES</span></span>

### <span data-ttu-id="88679-111">MD5-Hash aktualisieren</span><span class="sxs-lookup"><span data-stu-id="88679-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="88679-112">Aktualisiert den MD5-Hash für die erste Verbindung im Peering-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="88679-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="88679-113">Aktualisieren der BGP-Sitzungsadresse</span><span class="sxs-lookup"><span data-stu-id="88679-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="88679-114">Aktualisiert die Peering-Adresse für die erste Verbindung im Peering-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="88679-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="88679-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="88679-115">PARAMETERS</span></span>

### <span data-ttu-id="88679-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88679-116">-DefaultProfile</span></span>
<span data-ttu-id="88679-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88679-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88679-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="88679-118">-InputObject</span></span>
<span data-ttu-id="88679-119">Das Exchange-Verbindungsobjekt</span><span class="sxs-lookup"><span data-stu-id="88679-119">The exchange connection object</span></span>

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

### <span data-ttu-id="88679-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="88679-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="88679-121">Das maximal angekündigte IPv4</span><span class="sxs-lookup"><span data-stu-id="88679-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="88679-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="88679-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="88679-123">Das maximal angekündigte IPv6</span><span class="sxs-lookup"><span data-stu-id="88679-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="88679-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="88679-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="88679-125">Der MD5-Authentifizierungsschlüssel für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="88679-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="88679-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="88679-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="88679-127">Die IPv4-Adresse der Peer Sitzung</span><span class="sxs-lookup"><span data-stu-id="88679-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="88679-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="88679-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="88679-129">Die IPv6-Adresse der Peer Sitzung</span><span class="sxs-lookup"><span data-stu-id="88679-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="88679-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88679-130">CommonParameters</span></span>
<span data-ttu-id="88679-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88679-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88679-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88679-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88679-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88679-133">INPUTS</span></span>

### <span data-ttu-id="88679-134">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="88679-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="88679-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88679-135">OUTPUTS</span></span>

### <span data-ttu-id="88679-136">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="88679-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="88679-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="88679-137">NOTES</span></span>

## <span data-ttu-id="88679-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88679-138">RELATED LINKS</span></span>
