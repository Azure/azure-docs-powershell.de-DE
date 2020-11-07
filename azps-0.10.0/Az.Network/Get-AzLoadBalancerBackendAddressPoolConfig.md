---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 9c2341494f1508563523a181532ce98347051ac3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841639"
---
# <span data-ttu-id="423b0-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="423b0-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="423b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="423b0-102">SYNOPSIS</span></span>
<span data-ttu-id="423b0-103">Ruft eine Konfiguration des Back-End-Adresspools für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="423b0-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="423b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="423b0-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="423b0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="423b0-105">DESCRIPTION</span></span>
<span data-ttu-id="423b0-106">Das Cmdlet " **Get-AzLoadBalancerBackendAddressPoolConfig** " Ruft einen einzelnen Back-End-Adresspool oder eine Liste von Back-End-Adresspools in einem Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="423b0-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="423b0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="423b0-107">EXAMPLES</span></span>

### <span data-ttu-id="423b0-108">Beispiel 1: Abrufen des Back-End-Adresspools</span><span class="sxs-lookup"><span data-stu-id="423b0-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="423b0-109">Der erste Befehl ruft ein vorhandenes Lastenausgleichsmodul mit dem Namen "MyLoadBalancer" in der Ressourcengruppe "myresourcegroup" ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="423b0-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="423b0-110">Der zweite Befehl ruft die zugeordnete Konfiguration des Back-End-Adresspools mit dem Namen "BackendAddressPool02" für das Load Balancer in $LoadBalancer ab.</span><span class="sxs-lookup"><span data-stu-id="423b0-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="423b0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="423b0-111">PARAMETERS</span></span>

### <span data-ttu-id="423b0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423b0-112">-DefaultProfile</span></span>
<span data-ttu-id="423b0-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="423b0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423b0-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="423b0-114">-LoadBalancer</span></span>
<span data-ttu-id="423b0-115">Gibt das Load Balancer an, das dem zurückzugebenden Back-End-Adresspool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="423b0-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="423b0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="423b0-116">-Name</span></span>
<span data-ttu-id="423b0-117">Gibt den Namen des Load Balancer an, der den zurückzugebenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="423b0-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="423b0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423b0-118">CommonParameters</span></span>
<span data-ttu-id="423b0-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="423b0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423b0-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="423b0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423b0-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="423b0-121">INPUTS</span></span>

### <span data-ttu-id="423b0-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="423b0-122">PSLoadBalancer</span></span>
<span data-ttu-id="423b0-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="423b0-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="423b0-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="423b0-124">OUTPUTS</span></span>

### <span data-ttu-id="423b0-125">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="423b0-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="423b0-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="423b0-126">NOTES</span></span>

## <span data-ttu-id="423b0-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="423b0-127">RELATED LINKS</span></span>

[<span data-ttu-id="423b0-128">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="423b0-128">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="423b0-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="423b0-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="423b0-130">Neu – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="423b0-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="423b0-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="423b0-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


