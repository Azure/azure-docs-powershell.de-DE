---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006258"
---
# <span data-ttu-id="3d5d5-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="3d5d5-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="3d5d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5d5-103">Legt die Eigenschaften eines virtuellen Azure RemoteApp-Netzwerks fest.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="3d5d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d5d5-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d5d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d5d5-105">DESCRIPTION</span></span>
<span data-ttu-id="3d5d5-106">Das Cmdlet " **Set-AzureRemoteAppVNet** " legt die Eigenschaften eines virtuellen Azure RemoteApp-Netzwerks fest.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="3d5d5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d5d5-107">EXAMPLES</span></span>

### <span data-ttu-id="3d5d5-108">Beispiel 1: Einrichten der Eigenschaften eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="3d5d5-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="3d5d5-109">Mit diesem Befehl werden die Eigenschaften eines virtuellen Netzwerks mit dem Namen ContosoVNet festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="3d5d5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d5d5-110">PARAMETERS</span></span>

### <span data-ttu-id="3d5d5-111">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="3d5d5-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="3d5d5-112">Gibt die IPv4-Adressen der DNS-Server an.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5d5-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="3d5d5-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="3d5d5-114">Gibt den lokalen Netzwerk Adressraum in der CIDR-Notation (Classes Inter-Domain Routing) an.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="3d5d5-115">Dieser darf den virtuellen Netzwerk Adressraum nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5d5-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="3d5d5-116">-Profile</span></span>
<span data-ttu-id="3d5d5-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d5d5-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d5d5-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="3d5d5-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="3d5d5-120">Gibt den virtuellen Netzwerk Adressraum in der CIDR-Notation an.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="3d5d5-121">Dieser muss sich im privaten IP-Adressbereich befinden und kann den lokalen Netzwerk Adressraum nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5d5-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="3d5d5-122">-VNetName</span></span>
<span data-ttu-id="3d5d5-123">Gibt den Namen des virtuellen Azure RemoteApp-Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5d5-124">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="3d5d5-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="3d5d5-125">Gibt die Adresse des VPN-Geräts (virtuelles privates Netzwerk) an.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="3d5d5-126">Dies muss eine öffentlich zugängliche Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5d5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5d5-127">CommonParameters</span></span>
<span data-ttu-id="3d5d5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5d5-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d5d5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5d5-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d5d5-130">INPUTS</span></span>

## <span data-ttu-id="3d5d5-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d5d5-131">OUTPUTS</span></span>

## <span data-ttu-id="3d5d5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d5d5-132">NOTES</span></span>

## <span data-ttu-id="3d5d5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d5d5-133">RELATED LINKS</span></span>

[<span data-ttu-id="3d5d5-134">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="3d5d5-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


