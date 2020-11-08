---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006393"
---
# <span data-ttu-id="357cb-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="357cb-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="357cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="357cb-102">SYNOPSIS</span></span>
<span data-ttu-id="357cb-103">Erstellt ein VPN-Gateway in einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="357cb-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="357cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="357cb-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="357cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="357cb-105">DESCRIPTION</span></span>
<span data-ttu-id="357cb-106">Mit dem Cmdlet **New-AzureVNetGateway** wird ein VPN-Gateway (virtuelles privates Netzwerk) in einem virtuellen Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="357cb-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="357cb-107">Sie können auch die SKU des Gateways angeben, entweder Standard, Standard oder leistungsfähige.</span><span class="sxs-lookup"><span data-stu-id="357cb-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="357cb-108">Sie können den Typ angeben, entweder StaticRouting oder DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="357cb-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="357cb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="357cb-109">EXAMPLES</span></span>

### <span data-ttu-id="357cb-110">Beispiel 1: Erstellen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="357cb-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="357cb-111">Dieser Befehl erstellt ein virtuelles Netzwerkgateway für das virtuelle Netzwerk mit dem Namen ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="357cb-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="357cb-112">Das Gateway ist die Standard-SKU und verwendet dynamisches Routing.</span><span class="sxs-lookup"><span data-stu-id="357cb-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="357cb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="357cb-113">PARAMETERS</span></span>

### <span data-ttu-id="357cb-114">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="357cb-114">-GatewaySKU</span></span>
<span data-ttu-id="357cb-115">Gibt die SKU des vom Cmdlet erstellten virtuellen Netzwerkgateways an.</span><span class="sxs-lookup"><span data-stu-id="357cb-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="357cb-116">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="357cb-116">Valid values are:</span></span> 

- <span data-ttu-id="357cb-117">Standard</span><span class="sxs-lookup"><span data-stu-id="357cb-117">Default</span></span> 
- <span data-ttu-id="357cb-118">Standard</span><span class="sxs-lookup"><span data-stu-id="357cb-118">Standard</span></span> 
- <span data-ttu-id="357cb-119">Hochleistungs</span><span class="sxs-lookup"><span data-stu-id="357cb-119">HighPerformance</span></span>

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

### <span data-ttu-id="357cb-120">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="357cb-120">-GatewayType</span></span>
<span data-ttu-id="357cb-121">Gibt den Typ des Gateways an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="357cb-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="357cb-122">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="357cb-122">Valid values are:</span></span> 

- <span data-ttu-id="357cb-123">StaticRouting</span><span class="sxs-lookup"><span data-stu-id="357cb-123">StaticRouting</span></span> 
- <span data-ttu-id="357cb-124">DynamicRouting</span><span class="sxs-lookup"><span data-stu-id="357cb-124">DynamicRouting</span></span>

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

### <span data-ttu-id="357cb-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="357cb-125">-Profile</span></span>
<span data-ttu-id="357cb-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="357cb-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="357cb-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="357cb-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="357cb-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="357cb-128">-VNetName</span></span>
<span data-ttu-id="357cb-129">Gibt das virtuelle Netzwerk an, in dem mit diesem Cmdlet ein virtuelles Netzwerkgateway hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="357cb-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

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

### <span data-ttu-id="357cb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357cb-130">CommonParameters</span></span>
<span data-ttu-id="357cb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="357cb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357cb-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="357cb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357cb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="357cb-133">INPUTS</span></span>

## <span data-ttu-id="357cb-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="357cb-134">OUTPUTS</span></span>

## <span data-ttu-id="357cb-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="357cb-135">NOTES</span></span>

## <span data-ttu-id="357cb-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="357cb-136">RELATED LINKS</span></span>

[<span data-ttu-id="357cb-137">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="357cb-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="357cb-138">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="357cb-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="357cb-139">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="357cb-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="357cb-140">Größe ändern – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="357cb-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="357cb-141">Satz-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="357cb-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


