---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 9bbfa0aec2da00ada25fc4bb8a5334f67e80e41a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850648"
---
# <span data-ttu-id="d7180-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d7180-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="d7180-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7180-102">SYNOPSIS</span></span>
<span data-ttu-id="d7180-103">Entfernt eine Konfiguration des Back-End-Adresspools aus einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="d7180-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7180-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7180-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7180-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7180-105">DESCRIPTION</span></span>
<span data-ttu-id="d7180-106">Das Cmdlet **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** entfernt einen Back-End-Adresspool aus einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="d7180-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="d7180-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7180-107">EXAMPLES</span></span>

### <span data-ttu-id="d7180-108">Beispiel 1: Entfernen einer Konfiguration des Back-End-Adresspools von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="d7180-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="d7180-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und übergibt es an **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , wodurch die BackendAddressPool02-Konfiguration von MyLoadBalancer entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d7180-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="d7180-110">Schließlich aktualisiert das Set-AzureRmLoadBalancer-Cmdlet MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d7180-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="d7180-111">Beachten Sie, dass eine Konfiguration des Back-End-Adresspools vorhanden sein muss, bevor Sie Sie löschen können.</span><span class="sxs-lookup"><span data-stu-id="d7180-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="d7180-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7180-112">PARAMETERS</span></span>

### <span data-ttu-id="d7180-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7180-113">-DefaultProfile</span></span>
<span data-ttu-id="d7180-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7180-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7180-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7180-115">-LoadBalancer</span></span>
<span data-ttu-id="d7180-116">Gibt das Load Balancer an, das den zu entfernenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="d7180-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="d7180-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d7180-117">-Name</span></span>
<span data-ttu-id="d7180-118">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="d7180-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7180-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7180-119">CommonParameters</span></span>
<span data-ttu-id="d7180-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7180-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7180-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7180-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7180-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7180-122">INPUTS</span></span>

### <span data-ttu-id="d7180-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7180-123">PSLoadBalancer</span></span>
<span data-ttu-id="d7180-124">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7180-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d7180-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7180-125">OUTPUTS</span></span>

### <span data-ttu-id="d7180-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7180-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d7180-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7180-127">NOTES</span></span>

## <span data-ttu-id="d7180-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7180-128">RELATED LINKS</span></span>

[<span data-ttu-id="d7180-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d7180-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d7180-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7180-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d7180-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d7180-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d7180-132">Neu – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d7180-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


