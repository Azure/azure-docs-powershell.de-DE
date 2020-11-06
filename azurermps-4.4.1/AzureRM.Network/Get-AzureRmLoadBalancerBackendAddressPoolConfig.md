---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 3df754ddb267abe915724d6d709f4b59a1eda265
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500798"
---
# <span data-ttu-id="6669f-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6669f-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="6669f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6669f-102">SYNOPSIS</span></span>
<span data-ttu-id="6669f-103">Ruft eine Konfiguration des Back-End-Adresspools für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="6669f-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6669f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6669f-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6669f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6669f-105">DESCRIPTION</span></span>
<span data-ttu-id="6669f-106">Das Cmdlet " **Get-AzureRmLoadBalancerBackendAddressPoolConfig** " Ruft einen einzelnen Back-End-Adresspool oder eine Liste von Back-End-Adresspools in einem Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="6669f-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="6669f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6669f-107">EXAMPLES</span></span>

### <span data-ttu-id="6669f-108">Beispiel 1: Abrufen des Back-End-Adresspools</span><span class="sxs-lookup"><span data-stu-id="6669f-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="6669f-109">Der erste Befehl ruft ein vorhandenes Lastenausgleichsmodul mit dem Namen "MyLoadBalancer" in der Ressourcengruppe "myresourcegroup" ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6669f-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="6669f-110">Der zweite Befehl ruft die zugeordnete Konfiguration des Back-End-Adresspools mit dem Namen "BackendAddressPool02" für das Load Balancer in $LoadBalancer ab.</span><span class="sxs-lookup"><span data-stu-id="6669f-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="6669f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6669f-111">PARAMETERS</span></span>

### <span data-ttu-id="6669f-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6669f-112">-LoadBalancer</span></span>
<span data-ttu-id="6669f-113">Gibt das Load Balancer an, das dem zurückzugebenden Back-End-Adresspool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6669f-113">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6669f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6669f-114">-Name</span></span>
<span data-ttu-id="6669f-115">Gibt den Namen des Load Balancer an, der den zurückzugebenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="6669f-115">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="6669f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6669f-116">-DefaultProfile</span></span>
<span data-ttu-id="6669f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6669f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6669f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6669f-118">CommonParameters</span></span>
<span data-ttu-id="6669f-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6669f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6669f-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6669f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6669f-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6669f-121">INPUTS</span></span>

### <span data-ttu-id="6669f-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6669f-122">PSLoadBalancer</span></span>
<span data-ttu-id="6669f-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6669f-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="6669f-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6669f-124">OUTPUTS</span></span>

### <span data-ttu-id="6669f-125">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6669f-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="6669f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6669f-126">NOTES</span></span>

## <span data-ttu-id="6669f-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6669f-127">RELATED LINKS</span></span>

[<span data-ttu-id="6669f-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6669f-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="6669f-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6669f-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="6669f-130">Neu – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6669f-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="6669f-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6669f-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


