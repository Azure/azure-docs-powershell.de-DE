---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006729"
---
# <span data-ttu-id="3229d-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3229d-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3229d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3229d-102">SYNOPSIS</span></span>
<span data-ttu-id="3229d-103">Ruft eine Verbindung mit einem virtuellen Netzwerkgateway ab.</span><span class="sxs-lookup"><span data-stu-id="3229d-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="3229d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3229d-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3229d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3229d-105">DESCRIPTION</span></span>
<span data-ttu-id="3229d-106">Das Cmdlet " **Get-AzureVirtualNetworkGatewayConnection** " erhält eine Azure Virtual Network Gateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="3229d-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="3229d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3229d-107">EXAMPLES</span></span>

## <span data-ttu-id="3229d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3229d-108">PARAMETERS</span></span>

### <span data-ttu-id="3229d-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="3229d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="3229d-110">Gibt die ID einer verbundenen Entität an.</span><span class="sxs-lookup"><span data-stu-id="3229d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="3229d-111">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="3229d-111">-GatewayId</span></span>
<span data-ttu-id="3229d-112">Gibt die ID des Gateways an.</span><span class="sxs-lookup"><span data-stu-id="3229d-112">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="3229d-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="3229d-113">-Profile</span></span>
<span data-ttu-id="3229d-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3229d-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3229d-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3229d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3229d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3229d-116">CommonParameters</span></span>
<span data-ttu-id="3229d-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3229d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3229d-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3229d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3229d-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3229d-119">INPUTS</span></span>

## <span data-ttu-id="3229d-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3229d-120">OUTPUTS</span></span>

## <span data-ttu-id="3229d-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="3229d-121">NOTES</span></span>

## <span data-ttu-id="3229d-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3229d-122">RELATED LINKS</span></span>

[<span data-ttu-id="3229d-123">Neu – AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3229d-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3229d-124">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3229d-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3229d-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3229d-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)
