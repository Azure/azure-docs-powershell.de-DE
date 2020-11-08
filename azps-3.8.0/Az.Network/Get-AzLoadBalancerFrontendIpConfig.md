---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003543"
---
# <span data-ttu-id="d17e9-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d17e9-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="d17e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d17e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d17e9-103">Ruft eine Front-End-IP-Konfiguration in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="d17e9-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="d17e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d17e9-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d17e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d17e9-105">DESCRIPTION</span></span>
<span data-ttu-id="d17e9-106">Das Cmdlet " **Get-AzLoadBalancerFrontendIpConfig** " Ruft eine Front-End-IP-Konfiguration oder eine Liste der Front-End-IP-Konfigurationen in einem Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="d17e9-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="d17e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d17e9-107">EXAMPLES</span></span>

### <span data-ttu-id="d17e9-108">Beispiel 1: Abrufen einer Front-End-IP-Konfiguration in einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="d17e9-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="d17e9-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="d17e9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="d17e9-110">Der zweite Befehl ruft die Front-End-IP-Konfiguration ab, die diesem Lastenausgleichsmodul zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d17e9-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="d17e9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d17e9-111">PARAMETERS</span></span>

### <span data-ttu-id="d17e9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17e9-112">-DefaultProfile</span></span>
<span data-ttu-id="d17e9-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d17e9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d17e9-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d17e9-114">-LoadBalancer</span></span>
<span data-ttu-id="d17e9-115">Gibt das Load Balancer an, das der zu erhaltenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d17e9-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d17e9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d17e9-116">-Name</span></span>
<span data-ttu-id="d17e9-117">Gibt den Namen des Load Balancer an, der die zu erhaltende Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="d17e9-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d17e9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17e9-118">CommonParameters</span></span>
<span data-ttu-id="d17e9-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17e9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17e9-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d17e9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17e9-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d17e9-121">INPUTS</span></span>

### <span data-ttu-id="d17e9-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d17e9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d17e9-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d17e9-123">OUTPUTS</span></span>

### <span data-ttu-id="d17e9-124">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d17e9-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d17e9-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d17e9-125">NOTES</span></span>

## <span data-ttu-id="d17e9-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d17e9-126">RELATED LINKS</span></span>

[<span data-ttu-id="d17e9-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d17e9-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d17e9-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d17e9-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d17e9-129">Neu – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d17e9-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d17e9-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d17e9-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d17e9-131">Satz-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d17e9-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


