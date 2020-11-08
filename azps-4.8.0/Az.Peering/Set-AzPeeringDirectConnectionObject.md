---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009604"
---
# <span data-ttu-id="2c0c7-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="2c0c7-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="2c0c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c0c7-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0c7-103">Legt die direkten Verbindungsinformationen fest oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="2c0c7-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="2c0c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c0c7-104">SYNTAX</span></span>

### <span data-ttu-id="2c0c7-105">Bandbreite (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c0c7-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c0c7-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="2c0c7-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c0c7-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="2c0c7-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c0c7-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="2c0c7-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c0c7-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="2c0c7-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c0c7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c0c7-110">DESCRIPTION</span></span>
<span data-ttu-id="2c0c7-111">In Verbindung mit Update-AzPeering verwendet, handelt es sich um einen Arbeitsspeicher Vorgang, der nur mit beibehalten wird `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="2c0c7-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="2c0c7-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c0c7-112">EXAMPLES</span></span>

### <span data-ttu-id="2c0c7-113">Upgrade-Bandbreite</span><span class="sxs-lookup"><span data-stu-id="2c0c7-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="2c0c7-114">Aktualisiert die Bandbreite für die erste Verbindung im Peering-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2c0c7-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="2c0c7-115">Aktualisieren der BGP-Sitzungsadresse</span><span class="sxs-lookup"><span data-stu-id="2c0c7-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="2c0c7-116">Aktualisiert die Peering-Adresse für die erste Verbindung im Peering-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2c0c7-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="2c0c7-117">Update Verwendung für peeringdienst</span><span class="sxs-lookup"><span data-stu-id="2c0c7-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="2c0c7-118">Aktualisiert die Verbindung für die Verwendung mit Peering-Dienst</span><span class="sxs-lookup"><span data-stu-id="2c0c7-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="2c0c7-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c0c7-119">PARAMETERS</span></span>

### <span data-ttu-id="2c0c7-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="2c0c7-120">-BandwidthInMbps</span></span>
<span data-ttu-id="2c0c7-121">Die an diesem Speicherort in Mbit/s angebotene Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="2c0c7-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0c7-122">-DefaultProfile</span></span>
<span data-ttu-id="2c0c7-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c0c7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c0c7-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c0c7-124">-InputObject</span></span>
<span data-ttu-id="2c0c7-125">Das direkte Verbindungsobjekt</span><span class="sxs-lookup"><span data-stu-id="2c0c7-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c0c7-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="2c0c7-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="2c0c7-127">Das maximal angekündigte IPv4</span><span class="sxs-lookup"><span data-stu-id="2c0c7-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0c7-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="2c0c7-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="2c0c7-129">Das maximal angekündigte IPv6</span><span class="sxs-lookup"><span data-stu-id="2c0c7-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0c7-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="2c0c7-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="2c0c7-131">Der MD5-Authentifizierungsschlüssel für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2c0c7-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="2c0c7-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="2c0c7-132">-SessionPrefixV4</span></span>
<span data-ttu-id="2c0c7-133">Die IPv4-Adresse der Peer Sitzung</span><span class="sxs-lookup"><span data-stu-id="2c0c7-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0c7-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="2c0c7-134">-SessionPrefixV6</span></span>
<span data-ttu-id="2c0c7-135">Die IPv6-Adresse der Peer Sitzung</span><span class="sxs-lookup"><span data-stu-id="2c0c7-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0c7-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="2c0c7-136">-UseForPeeringService</span></span>
<span data-ttu-id="2c0c7-137">Aktivieren Sie diese Option für die Verwendung mit Microsoft Peering Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="2c0c7-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0c7-138">CommonParameters</span></span>
<span data-ttu-id="2c0c7-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c0c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0c7-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c0c7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0c7-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c0c7-141">INPUTS</span></span>

### <span data-ttu-id="2c0c7-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="2c0c7-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="2c0c7-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c0c7-143">OUTPUTS</span></span>

### <span data-ttu-id="2c0c7-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="2c0c7-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="2c0c7-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c0c7-145">NOTES</span></span>

## <span data-ttu-id="2c0c7-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c0c7-146">RELATED LINKS</span></span>
