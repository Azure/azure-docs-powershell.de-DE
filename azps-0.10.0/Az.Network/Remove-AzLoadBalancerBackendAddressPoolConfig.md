---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 30abb6f2d11eeae9749e7285a91ddeb93a1bf743
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841159"
---
# <span data-ttu-id="5f94f-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5f94f-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="5f94f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f94f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f94f-103">Entfernt eine Konfiguration des Back-End-Adresspools aus einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="5f94f-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="5f94f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f94f-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f94f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f94f-105">DESCRIPTION</span></span>
<span data-ttu-id="5f94f-106">Das Cmdlet **Remove-AzLoadBalancerBackendAddressPoolConfig** entfernt einen Back-End-Adresspool aus einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="5f94f-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="5f94f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f94f-107">EXAMPLES</span></span>

### <span data-ttu-id="5f94f-108">Beispiel 1: Entfernen einer Konfiguration des Back-End-Adresspools von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="5f94f-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="5f94f-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und übergibt es an **Remove-AzLoadBalancerBackendAddressPoolConfig** , wodurch die BackendAddressPool02-Konfiguration von MyLoadBalancer entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5f94f-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="5f94f-110">Schließlich aktualisiert das Set-AzLoadBalancer-Cmdlet MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="5f94f-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="5f94f-111">Beachten Sie, dass eine Konfiguration des Back-End-Adresspools vorhanden sein muss, bevor Sie Sie löschen können.</span><span class="sxs-lookup"><span data-stu-id="5f94f-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="5f94f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f94f-112">PARAMETERS</span></span>

### <span data-ttu-id="5f94f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f94f-113">-DefaultProfile</span></span>
<span data-ttu-id="5f94f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f94f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f94f-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f94f-115">-LoadBalancer</span></span>
<span data-ttu-id="5f94f-116">Gibt das Load Balancer an, das den zu entfernenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="5f94f-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="5f94f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5f94f-117">-Name</span></span>
<span data-ttu-id="5f94f-118">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="5f94f-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5f94f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f94f-119">CommonParameters</span></span>
<span data-ttu-id="5f94f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f94f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f94f-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f94f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f94f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f94f-122">INPUTS</span></span>

### <span data-ttu-id="5f94f-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f94f-123">PSLoadBalancer</span></span>
<span data-ttu-id="5f94f-124">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f94f-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5f94f-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f94f-125">OUTPUTS</span></span>

### <span data-ttu-id="5f94f-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f94f-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5f94f-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f94f-127">NOTES</span></span>

## <span data-ttu-id="5f94f-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f94f-128">RELATED LINKS</span></span>

[<span data-ttu-id="5f94f-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5f94f-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="5f94f-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f94f-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5f94f-131">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5f94f-131">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="5f94f-132">Neu – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5f94f-132">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


