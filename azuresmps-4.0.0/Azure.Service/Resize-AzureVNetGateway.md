---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006293"
---
# <span data-ttu-id="48177-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="48177-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="48177-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48177-102">SYNOPSIS</span></span>
<span data-ttu-id="48177-103">Ändert die Größe eines VPN-Gateways.</span><span class="sxs-lookup"><span data-stu-id="48177-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="48177-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48177-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="48177-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48177-105">DESCRIPTION</span></span>
<span data-ttu-id="48177-106">Mit dem Cmdlet **size-AzureVNetGateway** wird die Größe eines virtuellen VPN-Gateways (virtuelles privates Netzwerk) auf eine andere SKU geändert.</span><span class="sxs-lookup"><span data-stu-id="48177-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="48177-107">Gültige SKUs für ein virtuelles Netzwerkgateway sind Standard, Standard und leistungsfähige.</span><span class="sxs-lookup"><span data-stu-id="48177-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="48177-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48177-108">EXAMPLES</span></span>

### <span data-ttu-id="48177-109">Beispiel 1: Ändern der SKU für ein virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="48177-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="48177-110">Mit diesem Befehl wird die SKU des virtuellen Netzwerkgateways für das virtuelle Netzwerk mit dem Namen ContosoVN07 in leistungsfähige geändert.</span><span class="sxs-lookup"><span data-stu-id="48177-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="48177-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="48177-111">PARAMETERS</span></span>

### <span data-ttu-id="48177-112">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="48177-112">-GatewaySKU</span></span>
<span data-ttu-id="48177-113">Gibt die SKU an, für die dieses Cmdlet die Größe des virtuellen Netzwerkgateways ändert.</span><span class="sxs-lookup"><span data-stu-id="48177-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="48177-114">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="48177-114">Valid values are:</span></span> 

- <span data-ttu-id="48177-115">Standard</span><span class="sxs-lookup"><span data-stu-id="48177-115">Default</span></span> 
- <span data-ttu-id="48177-116">Standard</span><span class="sxs-lookup"><span data-stu-id="48177-116">Standard</span></span> 
- <span data-ttu-id="48177-117">Hochleistungs</span><span class="sxs-lookup"><span data-stu-id="48177-117">HighPerformance</span></span>

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

### <span data-ttu-id="48177-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="48177-118">-Profile</span></span>
<span data-ttu-id="48177-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="48177-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="48177-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="48177-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48177-121">-VNetName</span><span class="sxs-lookup"><span data-stu-id="48177-121">-VNetName</span></span>
<span data-ttu-id="48177-122">Gibt das virtuelle Netzwerk an, in dem dieses Cmdlet die Größe eines virtuellen Netzwerkgateways ändert.</span><span class="sxs-lookup"><span data-stu-id="48177-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

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

### <span data-ttu-id="48177-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48177-123">CommonParameters</span></span>
<span data-ttu-id="48177-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48177-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48177-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48177-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48177-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48177-126">INPUTS</span></span>

## <span data-ttu-id="48177-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48177-127">OUTPUTS</span></span>

## <span data-ttu-id="48177-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="48177-128">NOTES</span></span>

## <span data-ttu-id="48177-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48177-129">RELATED LINKS</span></span>

[<span data-ttu-id="48177-130">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="48177-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="48177-131">Neu – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="48177-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="48177-132">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="48177-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="48177-133">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="48177-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="48177-134">Satz-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="48177-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


