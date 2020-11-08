---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006721"
---
# <span data-ttu-id="c765c-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="c765c-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="c765c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c765c-102">SYNOPSIS</span></span>
<span data-ttu-id="c765c-103">Ruft die IPSec-Parameter für ein Azure Virtual Network-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="c765c-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="c765c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c765c-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c765c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c765c-105">DESCRIPTION</span></span>
<span data-ttu-id="c765c-106">Das Cmdlet " **Get-AzureVirtualNetworkGatewayIPsecParameters** " Ruft die IPSec-Parameter für ein Azure Virtual Network-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="c765c-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="c765c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c765c-107">EXAMPLES</span></span>

## <span data-ttu-id="c765c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c765c-108">PARAMETERS</span></span>

### <span data-ttu-id="c765c-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="c765c-109">-ConnectedEntityId</span></span>
<span data-ttu-id="c765c-110">Gibt die ID eines verbundenen einspringers an.</span><span class="sxs-lookup"><span data-stu-id="c765c-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="c765c-111">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="c765c-111">-GatewayId</span></span>
<span data-ttu-id="c765c-112">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="c765c-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="c765c-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="c765c-113">-Profile</span></span>
<span data-ttu-id="c765c-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c765c-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c765c-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c765c-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c765c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c765c-116">CommonParameters</span></span>
<span data-ttu-id="c765c-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c765c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c765c-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c765c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c765c-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c765c-119">INPUTS</span></span>

## <span data-ttu-id="c765c-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c765c-120">OUTPUTS</span></span>

## <span data-ttu-id="c765c-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="c765c-121">NOTES</span></span>

## <span data-ttu-id="c765c-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c765c-122">RELATED LINKS</span></span>

[<span data-ttu-id="c765c-123">Satz-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="c765c-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)


