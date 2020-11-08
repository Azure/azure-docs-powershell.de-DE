---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005643"
---
# <span data-ttu-id="68944-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="68944-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="68944-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68944-102">SYNOPSIS</span></span>
<span data-ttu-id="68944-103">Legt den Schlüssel für ein Azure Virtual Network-Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="68944-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="68944-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68944-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="68944-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68944-105">DESCRIPTION</span></span>
<span data-ttu-id="68944-106">Das Cmdlet " **Set-AzureVirtualNetworkGatewayKey** " legt den Schlüssel für ein Azure Virtual Network-Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="68944-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="68944-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68944-107">EXAMPLES</span></span>

## <span data-ttu-id="68944-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68944-108">PARAMETERS</span></span>

### <span data-ttu-id="68944-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="68944-109">-ConnectedEntityId</span></span>
<span data-ttu-id="68944-110">Gibt die ID einer verbundenen Entität an.</span><span class="sxs-lookup"><span data-stu-id="68944-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="68944-111">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="68944-111">-GatewayId</span></span>
<span data-ttu-id="68944-112">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="68944-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="68944-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="68944-113">-Profile</span></span>
<span data-ttu-id="68944-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="68944-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="68944-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="68944-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="68944-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="68944-116">-SharedKey</span></span>
<span data-ttu-id="68944-117">Gibt einen freigegebenen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="68944-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="68944-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68944-118">CommonParameters</span></span>
<span data-ttu-id="68944-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68944-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68944-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68944-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68944-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68944-121">INPUTS</span></span>

## <span data-ttu-id="68944-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68944-122">OUTPUTS</span></span>

## <span data-ttu-id="68944-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="68944-123">NOTES</span></span>

## <span data-ttu-id="68944-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68944-124">RELATED LINKS</span></span>

[<span data-ttu-id="68944-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="68944-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="68944-126">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="68944-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)


