---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F3D44471-50F0-4737-9AF5-3DE7222EAF9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9aa386b47c02ed945cad63c00425534d68e66f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005691"
---
# <span data-ttu-id="c432e-101">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c432e-101">Remove-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c432e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c432e-102">SYNOPSIS</span></span>
<span data-ttu-id="c432e-103">Entfernt eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c432e-103">Removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="c432e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c432e-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c432e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c432e-105">DESCRIPTION</span></span>
<span data-ttu-id="c432e-106">Das Cmdlet **Remove-AzureVirtualNetworkGatewayConnection** entfernt eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c432e-106">The **Remove-AzureVirtualNetworkGatewayConnection** cmdlet removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="c432e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c432e-107">EXAMPLES</span></span>

## <span data-ttu-id="c432e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c432e-108">PARAMETERS</span></span>

### <span data-ttu-id="c432e-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="c432e-109">-ConnectedEntityId</span></span>
<span data-ttu-id="c432e-110">Gibt die ID einer verbundenen Entität an.</span><span class="sxs-lookup"><span data-stu-id="c432e-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="c432e-111">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="c432e-111">-GatewayId</span></span>
<span data-ttu-id="c432e-112">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="c432e-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="c432e-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="c432e-113">-Profile</span></span>
<span data-ttu-id="c432e-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c432e-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c432e-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c432e-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c432e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c432e-116">CommonParameters</span></span>
<span data-ttu-id="c432e-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c432e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c432e-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c432e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c432e-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c432e-119">INPUTS</span></span>

## <span data-ttu-id="c432e-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c432e-120">OUTPUTS</span></span>

## <span data-ttu-id="c432e-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="c432e-121">NOTES</span></span>

## <span data-ttu-id="c432e-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c432e-122">RELATED LINKS</span></span>

[<span data-ttu-id="c432e-123">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c432e-123">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c432e-124">Neu – AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c432e-124">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c432e-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c432e-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


