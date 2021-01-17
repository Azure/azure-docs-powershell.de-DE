---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302723"
---
# <span data-ttu-id="2ee21-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="2ee21-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="2ee21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ee21-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee21-103">Erstellt ein im Arbeitsspeicher gespeichertes PSObject, das zum Erstellen oder Ändern eines Peerings verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ee21-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="2ee21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ee21-104">SYNTAX</span></span>

### <span data-ttu-id="2ee21-105">IPv4PrefixIPv6Prefix (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ee21-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee21-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="2ee21-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ee21-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ee21-107">DESCRIPTION</span></span>
<span data-ttu-id="2ee21-108">Erstellt ein PSObject im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="2ee21-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="2ee21-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ee21-109">EXAMPLES</span></span>

### <span data-ttu-id="2ee21-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ee21-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="2ee21-111">Neue lokale Verbindung</span><span class="sxs-lookup"><span data-stu-id="2ee21-111">New local connection</span></span>

### <span data-ttu-id="2ee21-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2ee21-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="2ee21-113">Erstellen einer direkten Peeringverbindung mit aktivierter Peeringdienstnutzung und von Microsoft bereitgestellten IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="2ee21-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="2ee21-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2ee21-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="2ee21-115">Erstellen einer direkten Peeringverbindung mit aktivierter Peeringdienstnutzung und von Peer bereitgestellten IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="2ee21-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="2ee21-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="2ee21-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="2ee21-117">Erstellen Sie eine direkte Peeringverbindung ohne BGP-Sitzungs-IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="2ee21-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="2ee21-118">Der Peer muss die IP-Adressen festlegen, bevor die bgp-Sitzung konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2ee21-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="2ee21-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ee21-119">PARAMETERS</span></span>

### <span data-ttu-id="2ee21-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="2ee21-120">-BandwidthInMbps</span></span>
<span data-ttu-id="2ee21-121">Die an dieser Position in Mbit/s angebotene Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="2ee21-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee21-122">-DefaultProfile</span></span>
<span data-ttu-id="2ee21-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ee21-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ee21-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="2ee21-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="2ee21-125">Die maximal angekündigte IPv4-Größe</span><span class="sxs-lookup"><span data-stu-id="2ee21-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee21-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="2ee21-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="2ee21-127">Die maximal angekündigte IPv6-Größe</span><span class="sxs-lookup"><span data-stu-id="2ee21-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee21-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="2ee21-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="2ee21-129">Der MD5-Authentifizierungsschlüssel für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2ee21-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee21-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="2ee21-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="2ee21-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span><span class="sxs-lookup"><span data-stu-id="2ee21-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee21-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="2ee21-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="2ee21-133">Die Id der Peeringeinrichtung, die auf https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="2ee21-133">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="2ee21-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="2ee21-134">-SessionPrefixV4</span></span>
<span data-ttu-id="2ee21-135">Die Peersitzungs-IPv4-Adresse</span><span class="sxs-lookup"><span data-stu-id="2ee21-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee21-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="2ee21-136">-SessionPrefixV6</span></span>
<span data-ttu-id="2ee21-137">Die Peersitzungs-IPv6-Adresse</span><span class="sxs-lookup"><span data-stu-id="2ee21-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee21-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="2ee21-138">-UseForPeeringService</span></span>
<span data-ttu-id="2ee21-139">Aktivieren Sie die Verwendung mit Microsoft Peering Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="2ee21-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee21-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee21-140">CommonParameters</span></span>
<span data-ttu-id="2ee21-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee21-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee21-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ee21-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee21-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ee21-143">INPUTS</span></span>

### <span data-ttu-id="2ee21-144">Keine</span><span class="sxs-lookup"><span data-stu-id="2ee21-144">None</span></span>

## <span data-ttu-id="2ee21-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ee21-145">OUTPUTS</span></span>

### <span data-ttu-id="2ee21-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="2ee21-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="2ee21-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2ee21-147">NOTES</span></span>

## <span data-ttu-id="2ee21-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2ee21-148">RELATED LINKS</span></span>
