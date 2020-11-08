---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006392"
---
# <span data-ttu-id="d1485-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1485-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="d1485-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1485-102">SYNOPSIS</span></span>
<span data-ttu-id="d1485-103">Erstellt ein Azure Virtual Network-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d1485-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="d1485-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1485-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d1485-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1485-105">DESCRIPTION</span></span>
<span data-ttu-id="d1485-106">Das Cmdlet **New-AzureVirtualNetworkGateway** erstellt ein Azure Virtual Network-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d1485-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="d1485-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1485-107">EXAMPLES</span></span>

## <span data-ttu-id="d1485-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1485-108">PARAMETERS</span></span>

### <span data-ttu-id="d1485-109">-ASN</span><span class="sxs-lookup"><span data-stu-id="d1485-109">-Asn</span></span>
<span data-ttu-id="d1485-110">Gibt die autonome Systemnummer an (ASN).</span><span class="sxs-lookup"><span data-stu-id="d1485-110">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1485-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d1485-111">-Force</span></span>
<span data-ttu-id="d1485-112">Azure Virtual Network Gateway-Erstellung nicht bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1485-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1485-113">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="d1485-113">-GatewayName</span></span>
<span data-ttu-id="d1485-114">Gibt den Namen des Gateways an.</span><span class="sxs-lookup"><span data-stu-id="d1485-114">Specifies the name of the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1485-115">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="d1485-115">-GatewaySKU</span></span>
<span data-ttu-id="d1485-116">Gibt die SKU des vom Cmdlet erstellten virtuellen Netzwerkgateways an.</span><span class="sxs-lookup"><span data-stu-id="d1485-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="d1485-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d1485-117">Valid values are:</span></span>

- <span data-ttu-id="d1485-118">Standard</span><span class="sxs-lookup"><span data-stu-id="d1485-118">Default</span></span>
- <span data-ttu-id="d1485-119">Standard</span><span class="sxs-lookup"><span data-stu-id="d1485-119">Standard</span></span>
- <span data-ttu-id="d1485-120">Hochleistungs</span><span class="sxs-lookup"><span data-stu-id="d1485-120">HighPerformance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1485-121">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="d1485-121">-GatewayType</span></span>
<span data-ttu-id="d1485-122">Gibt den Typ des Gateways an.</span><span class="sxs-lookup"><span data-stu-id="d1485-122">Specifies the type of gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1485-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="d1485-123">-Location</span></span>
<span data-ttu-id="d1485-124">Gibt den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="d1485-124">Specifies the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1485-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d1485-125">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1485-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="d1485-126">-Profile</span></span>
<span data-ttu-id="d1485-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d1485-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1485-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d1485-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d1485-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="d1485-129">-VnetId</span></span>
<span data-ttu-id="d1485-130">Gibt die ID eines virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="d1485-130">Specifies the ID of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1485-131">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d1485-131">-VNetName</span></span>
<span data-ttu-id="d1485-132">Gibt ein virtuelles Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="d1485-132">Specifies a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1485-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1485-133">CommonParameters</span></span>
<span data-ttu-id="d1485-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1485-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1485-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1485-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1485-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1485-136">INPUTS</span></span>

## <span data-ttu-id="d1485-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1485-137">OUTPUTS</span></span>

## <span data-ttu-id="d1485-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1485-138">NOTES</span></span>

## <span data-ttu-id="d1485-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1485-139">RELATED LINKS</span></span>

[<span data-ttu-id="d1485-140">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1485-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="d1485-141">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1485-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="d1485-142">Größe ändern – AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1485-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)
