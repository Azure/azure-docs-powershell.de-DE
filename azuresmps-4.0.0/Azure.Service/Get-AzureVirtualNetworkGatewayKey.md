---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5F016D72-80EB-462D-9646-25EC4E33293E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 485b29130fd4b54c378f3ec19389b6c24ba86c63
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006719"
---
# <span data-ttu-id="20606-101">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="20606-101">Get-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="20606-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20606-102">SYNOPSIS</span></span>
<span data-ttu-id="20606-103">Ruft den Schlüssel für ein Azure Virtual Network-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="20606-103">Gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="20606-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20606-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="20606-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20606-105">DESCRIPTION</span></span>
<span data-ttu-id="20606-106">Das Cmdlet " **Get-AzureVirtualNetworkGatewayKey** " Ruft den Schlüssel für ein Azure Virtual Network-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="20606-106">The **Get-AzureVirtualNetworkGatewayKey** cmdlet gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="20606-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20606-107">EXAMPLES</span></span>

## <span data-ttu-id="20606-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="20606-108">PARAMETERS</span></span>

### <span data-ttu-id="20606-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="20606-109">-ConnectedEntityId</span></span>
<span data-ttu-id="20606-110">Gibt die ID einer verbundenen Entität an.</span><span class="sxs-lookup"><span data-stu-id="20606-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="20606-111">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="20606-111">-GatewayId</span></span>
<span data-ttu-id="20606-112">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="20606-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="20606-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="20606-113">-Profile</span></span>
<span data-ttu-id="20606-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="20606-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="20606-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="20606-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20606-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20606-116">CommonParameters</span></span>
<span data-ttu-id="20606-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20606-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20606-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20606-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20606-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20606-119">INPUTS</span></span>

## <span data-ttu-id="20606-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20606-120">OUTPUTS</span></span>

## <span data-ttu-id="20606-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="20606-121">NOTES</span></span>

## <span data-ttu-id="20606-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20606-122">RELATED LINKS</span></span>

[<span data-ttu-id="20606-123">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="20606-123">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="20606-124">Satz-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="20606-124">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)


