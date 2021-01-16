---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295169"
---
# <span data-ttu-id="3936c-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="3936c-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="3936c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3936c-102">SYNOPSIS</span></span>
<span data-ttu-id="3936c-103">Legt die Informationen zur Exchange-Verbindung fest oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="3936c-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="3936c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3936c-104">SYNTAX</span></span>

### <span data-ttu-id="3936c-105">IPv4Address (Standard)</span><span class="sxs-lookup"><span data-stu-id="3936c-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3936c-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="3936c-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3936c-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="3936c-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3936c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3936c-108">DESCRIPTION</span></span>
<span data-ttu-id="3936c-109">Wird in Verbindung mit Update-AzPeering verwendet, ist dies ein Speichervorgang und wird nur beibehalten `Update-AzPeering` mit.</span><span class="sxs-lookup"><span data-stu-id="3936c-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="3936c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3936c-110">EXAMPLES</span></span>

### <span data-ttu-id="3936c-111">Aktualisieren des #A0</span><span class="sxs-lookup"><span data-stu-id="3936c-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="3936c-112">Aktualisiert den #A0 für die erste Verbindung im Peeringobjekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3936c-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="3936c-113">Aktualisieren der Bgp-Sitzungsadresse</span><span class="sxs-lookup"><span data-stu-id="3936c-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="3936c-114">Aktualisiert die Peeringadresse für die erste Verbindung im Peeringobjekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3936c-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="3936c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3936c-115">PARAMETERS</span></span>

### <span data-ttu-id="3936c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3936c-116">-DefaultProfile</span></span>
<span data-ttu-id="3936c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3936c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3936c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3936c-118">-InputObject</span></span>
<span data-ttu-id="3936c-119">Das Exchange-Verbindungsobjekt</span><span class="sxs-lookup"><span data-stu-id="3936c-119">The exchange connection object</span></span>

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

### <span data-ttu-id="3936c-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="3936c-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="3936c-121">Die maximal angekündigte IPv4-Größe</span><span class="sxs-lookup"><span data-stu-id="3936c-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="3936c-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="3936c-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="3936c-123">Die maximal angekündigte IPv6-Größe</span><span class="sxs-lookup"><span data-stu-id="3936c-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="3936c-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="3936c-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="3936c-125">Der MD5-Authentifizierungsschlüssel für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="3936c-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="3936c-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="3936c-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="3936c-127">Die Peersitzungs-IPv4-Adresse</span><span class="sxs-lookup"><span data-stu-id="3936c-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="3936c-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="3936c-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="3936c-129">Die Peersitzungs-IPv6-Adresse</span><span class="sxs-lookup"><span data-stu-id="3936c-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="3936c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3936c-130">CommonParameters</span></span>
<span data-ttu-id="3936c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3936c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3936c-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3936c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3936c-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3936c-133">INPUTS</span></span>

### <span data-ttu-id="3936c-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="3936c-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="3936c-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3936c-135">OUTPUTS</span></span>

### <span data-ttu-id="3936c-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="3936c-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="3936c-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3936c-137">NOTES</span></span>

## <span data-ttu-id="3936c-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3936c-138">RELATED LINKS</span></span>
