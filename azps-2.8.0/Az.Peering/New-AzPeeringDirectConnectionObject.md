---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: abc1b5206762e4a2d57bd64bdc784b375606cde5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824016"
---
# <span data-ttu-id="78128-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="78128-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="78128-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78128-102">SYNOPSIS</span></span>
<span data-ttu-id="78128-103">Erstellt eine im Arbeitsspeicher PSObject, die zum Erstellen oder Ändern eines Peerings verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="78128-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="78128-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78128-104">SYNTAX</span></span>

### <span data-ttu-id="78128-105">IPv4PrefixIPv6Prefix (Standard)</span><span class="sxs-lookup"><span data-stu-id="78128-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78128-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="78128-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78128-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78128-107">DESCRIPTION</span></span>
<span data-ttu-id="78128-108">Erstellt eine im Speicher PSObject</span><span class="sxs-lookup"><span data-stu-id="78128-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="78128-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78128-109">EXAMPLES</span></span>

### <span data-ttu-id="78128-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78128-110">Example 1</span></span>
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

<span data-ttu-id="78128-111">Neue lokale Verbindung</span><span class="sxs-lookup"><span data-stu-id="78128-111">New local connection</span></span>

### <span data-ttu-id="78128-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="78128-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="78128-113">Erstellen einer direkten Peeringverbindung mit Verwendung für Peering-Dienst aktiviert und von Microsoft bereitgestellte IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="78128-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="78128-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="78128-114">Example 3</span></span>
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

<span data-ttu-id="78128-115">Erstellen einer direkten Peeringverbindung mit der Verwendung für Peering-Dienst aktiviert und bereitgestellte IP-Adressen für Peers</span><span class="sxs-lookup"><span data-stu-id="78128-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="78128-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="78128-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="78128-117">Erstellen Sie eine direkte Peeringverbindung ohne BGP-Sitzungs-IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="78128-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="78128-118">Der Peer muss die IP-Adressen festgelegt haben, bevor die BGP-Sitzung konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="78128-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="78128-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="78128-119">PARAMETERS</span></span>

### <span data-ttu-id="78128-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="78128-120">-BandwidthInMbps</span></span>
<span data-ttu-id="78128-121">Die an diesem Speicherort in Mbit/s angebotene Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="78128-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="78128-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78128-122">-DefaultProfile</span></span>
<span data-ttu-id="78128-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78128-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78128-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="78128-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="78128-125">Das maximal angekündigte IPv4</span><span class="sxs-lookup"><span data-stu-id="78128-125">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="78128-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="78128-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="78128-127">Das maximal angekündigte IPv6</span><span class="sxs-lookup"><span data-stu-id="78128-127">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="78128-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="78128-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="78128-129">Der MD5-Authentifizierungsschlüssel für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="78128-129">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="78128-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="78128-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="78128-131">Flag aktivieren, das Microsoft auffordert, die BGP-Sitzungs Adressen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="78128-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

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

### <span data-ttu-id="78128-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="78128-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="78128-133">Die ID der Peering-Einrichtung, die auf gefunden wurde https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="78128-133">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="78128-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="78128-134">-SessionPrefixV4</span></span>
<span data-ttu-id="78128-135">Die IPv4-Adresse der Peer Sitzung</span><span class="sxs-lookup"><span data-stu-id="78128-135">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="78128-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="78128-136">-SessionPrefixV6</span></span>
<span data-ttu-id="78128-137">Die IPv6-Adresse der Peer Sitzung</span><span class="sxs-lookup"><span data-stu-id="78128-137">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="78128-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="78128-138">-UseForPeeringService</span></span>
<span data-ttu-id="78128-139">Aktivieren Sie diese Option für die Verwendung mit Microsoft Peering Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="78128-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="78128-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78128-140">CommonParameters</span></span>
<span data-ttu-id="78128-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78128-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78128-142">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78128-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78128-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78128-143">INPUTS</span></span>

### <span data-ttu-id="78128-144">Keine</span><span class="sxs-lookup"><span data-stu-id="78128-144">None</span></span>

## <span data-ttu-id="78128-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78128-145">OUTPUTS</span></span>

### <span data-ttu-id="78128-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="78128-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="78128-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="78128-147">NOTES</span></span>

## <span data-ttu-id="78128-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78128-148">RELATED LINKS</span></span>
