---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006200"
---
# <span data-ttu-id="1c9e1-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="1c9e1-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="1c9e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9e1-103">Erstellt ein virtuelles Azure RemoteApp-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="1c9e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c9e1-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1c9e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c9e1-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9e1-106">Mit dem Cmdlet **New-AzureRemoteAppVNet** wird ein virtuelles Azure RemoteApp-Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="1c9e1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c9e1-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9e1-108">Beispiel 1: Erstellen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="1c9e1-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="1c9e1-109">Dieser Befehl erstellt ein virtuelles Netzwerk mit dem Namen ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="1c9e1-110">Wenn Sie den Status des Vorgangs ermitteln möchten, verwenden Sie das Cmdlet **Get-AzureRemoteAppOperationResult** mit der nach Verfolgungs-ID, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="1c9e1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c9e1-111">PARAMETERS</span></span>

### <span data-ttu-id="1c9e1-112">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="1c9e1-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="1c9e1-113">Gibt ein Array der IPv4-Adressen der DNS-Server an.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e1-114">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="1c9e1-114">-GatewayType</span></span>
<span data-ttu-id="1c9e1-115">Gibt den Typ des zu verwendenden Gateway-Routings an.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="1c9e1-116">Die zulässigen Werte für diesen Parameter sind: StaticRouting oder DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e1-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="1c9e1-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="1c9e1-118">Gibt ein Array von Zeichenfolgen an, mit denen der lokale Netzwerk Adressraum in der CIDR-Notation (classly InterDomain Routing) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="1c9e1-119">Dieser Adressraum darf sich nicht mit dem virtuellen Netzwerk Adressraum überlappen, den der *VirtualNetworkAddressSpace* -Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e1-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="1c9e1-120">-Location</span></span>
<span data-ttu-id="1c9e1-121">Gibt den Speicherort an, an dem das virtuelle Netzwerk erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e1-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="1c9e1-122">-Profile</span></span>
<span data-ttu-id="1c9e1-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c9e1-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c9e1-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="1c9e1-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="1c9e1-126">Gibt ein Array von Zeichenfolgen an, die den virtuellen Netzwerk Adressraum in der CIDR-Notation angeben.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="1c9e1-127">Dieser muss sich im privaten IP-Adressbereich befinden und kann sich nicht mit dem lokalen Netzwerk Adressraum überlappen, der vom *LocalNetworkAddressSpace* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e1-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="1c9e1-128">-VNetName</span></span>
<span data-ttu-id="1c9e1-129">Gibt den Namen des virtuellen Azure RemoteApp-Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="1c9e1-130">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="1c9e1-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="1c9e1-131">Gibt die Adresse des VPN-Geräts (virtuelles privates Netzwerk) an.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="1c9e1-132">Dies muss eine öffentlich zugängliche Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-132">This must be a public-facing address.</span></span>

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

### <span data-ttu-id="1c9e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9e1-133">CommonParameters</span></span>
<span data-ttu-id="1c9e1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9e1-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c9e1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9e1-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c9e1-136">INPUTS</span></span>

## <span data-ttu-id="1c9e1-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c9e1-137">OUTPUTS</span></span>

## <span data-ttu-id="1c9e1-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c9e1-138">NOTES</span></span>

## <span data-ttu-id="1c9e1-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c9e1-139">RELATED LINKS</span></span>

[<span data-ttu-id="1c9e1-140">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="1c9e1-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="1c9e1-141">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="1c9e1-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="1c9e1-142">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="1c9e1-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="1c9e1-143">Satz-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="1c9e1-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


