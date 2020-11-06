---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: b6a4899fb54ffc4305f6b512046e00bda994b02e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497770"
---
# <span data-ttu-id="c559d-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="c559d-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="c559d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c559d-102">SYNOPSIS</span></span>
<span data-ttu-id="c559d-103">Listet von einem Azure Virtual Network Gateway gelernte Routen auf</span><span class="sxs-lookup"><span data-stu-id="c559d-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c559d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c559d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c559d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c559d-105">DESCRIPTION</span></span>
<span data-ttu-id="c559d-106">Listet Routen auf, die von einem Azure Virtual Network Gateway aus verschiedenen Quellen erlernt wurden.</span><span class="sxs-lookup"><span data-stu-id="c559d-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="c559d-107">Dazu gehören Routen, die über BGP gelernt werden, sowie statische Routen.</span><span class="sxs-lookup"><span data-stu-id="c559d-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="c559d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c559d-108">EXAMPLES</span></span>

### <span data-ttu-id="c559d-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c559d-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="c559d-110">Ruft für das Azure Virtual Network Gateway mit dem Namen "Gatewayname" in der Ressourcengruppe "ResourceGroup" die Routen ab, die das Azure-Gateway kennt.</span><span class="sxs-lookup"><span data-stu-id="c559d-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="c559d-111">Das Azure Virtual Network Gateway hat in diesem Fall zwei statische Routen (10.1.0.0/16 und 10.0.0.254/32) sowie eine Route, die über BGP (10.0.0.0/16) erlernt wurde.</span><span class="sxs-lookup"><span data-stu-id="c559d-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="c559d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c559d-112">PARAMETERS</span></span>

### <span data-ttu-id="c559d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c559d-113">-ResourceGroupName</span></span>
<span data-ttu-id="c559d-114">Name der Ressourcengruppe der virtuellen Netzwerk-Gateway-Ressource</span><span class="sxs-lookup"><span data-stu-id="c559d-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c559d-115">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c559d-115">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c559d-116">Name des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="c559d-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c559d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c559d-117">-DefaultProfile</span></span>
<span data-ttu-id="c559d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c559d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c559d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c559d-119">CommonParameters</span></span>
<span data-ttu-id="c559d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c559d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c559d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c559d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c559d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c559d-122">INPUTS</span></span>

### <span data-ttu-id="c559d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c559d-123">System.String</span></span>

## <span data-ttu-id="c559d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c559d-124">OUTPUTS</span></span>

### <span data-ttu-id="c559d-125">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="c559d-125">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="c559d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c559d-126">NOTES</span></span>

## <span data-ttu-id="c559d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c559d-127">RELATED LINKS</span></span>

