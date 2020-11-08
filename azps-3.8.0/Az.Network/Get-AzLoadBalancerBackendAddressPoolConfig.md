---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003546"
---
# <span data-ttu-id="8d354-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8d354-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="8d354-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d354-102">SYNOPSIS</span></span>
<span data-ttu-id="8d354-103">Ruft eine Konfiguration des Back-End-Adresspools für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="8d354-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="8d354-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d354-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d354-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d354-105">DESCRIPTION</span></span>
<span data-ttu-id="8d354-106">Das Cmdlet " **Get-AzLoadBalancerBackendAddressPoolConfig** " Ruft einen einzelnen Back-End-Adresspool oder eine Liste von Back-End-Adresspools in einem Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="8d354-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="8d354-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d354-107">EXAMPLES</span></span>

### <span data-ttu-id="8d354-108">Beispiel 1: Abrufen des Back-End-Adresspools</span><span class="sxs-lookup"><span data-stu-id="8d354-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="8d354-109">Der erste Befehl ruft ein vorhandenes Lastenausgleichsmodul mit dem Namen "MyLoadBalancer" in der Ressourcengruppe "myresourcegroup" ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8d354-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="8d354-110">Der zweite Befehl ruft die zugeordnete Konfiguration des Back-End-Adresspools mit dem Namen "BackendAddressPool02" für das Load Balancer in $LoadBalancer ab.</span><span class="sxs-lookup"><span data-stu-id="8d354-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="8d354-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d354-111">PARAMETERS</span></span>

### <span data-ttu-id="8d354-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d354-112">-DefaultProfile</span></span>
<span data-ttu-id="8d354-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d354-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d354-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d354-114">-LoadBalancer</span></span>
<span data-ttu-id="8d354-115">Gibt das Load Balancer an, das dem zurückzugebenden Back-End-Adresspool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8d354-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="8d354-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8d354-116">-Name</span></span>
<span data-ttu-id="8d354-117">Gibt den Namen des Load Balancer an, der den zurückzugebenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="8d354-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="8d354-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d354-118">CommonParameters</span></span>
<span data-ttu-id="8d354-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d354-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d354-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d354-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d354-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d354-121">INPUTS</span></span>

### <span data-ttu-id="8d354-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d354-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8d354-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d354-123">OUTPUTS</span></span>

### <span data-ttu-id="8d354-124">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8d354-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="8d354-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d354-125">NOTES</span></span>

## <span data-ttu-id="8d354-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d354-126">RELATED LINKS</span></span>

[<span data-ttu-id="8d354-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8d354-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8d354-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d354-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8d354-129">Neu – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8d354-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8d354-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8d354-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


