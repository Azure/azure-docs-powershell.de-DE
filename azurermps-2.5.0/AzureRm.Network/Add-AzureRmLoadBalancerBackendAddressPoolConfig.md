---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 3538a74b2ac638270d5487039faf9f8268d6efa8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849255"
---
# <span data-ttu-id="816d3-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="816d3-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="816d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="816d3-102">SYNOPSIS</span></span>
<span data-ttu-id="816d3-103">Fügt eine Konfiguration des Back-End-Adresspools zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="816d3-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="816d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="816d3-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="816d3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="816d3-105">DESCRIPTION</span></span>
<span data-ttu-id="816d3-106">Das Cmdlet **Add-AzureRmLoadBalancerBackend** fügt einem Azure Load Balancer einen Back-End-Adresspool hinzu.</span><span class="sxs-lookup"><span data-stu-id="816d3-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="816d3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="816d3-107">EXAMPLES</span></span>

### <span data-ttu-id="816d3-108">Beispiel 1 Hinzufügen einer Konfiguration des Back-End-Adresspools zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="816d3-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="816d3-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab, fügt den Back-End-Adresspool mit dem Namen BackendAddressPool02 zu MyLoadBalancer hinzu und verwendet dann das Cmdlet " **Satz-AzureRmLoadBalancer** ", um MyLoadBalancer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="816d3-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="816d3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="816d3-110">PARAMETERS</span></span>

### <span data-ttu-id="816d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="816d3-111">-DefaultProfile</span></span>
<span data-ttu-id="816d3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="816d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="816d3-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="816d3-113">-LoadBalancer</span></span>
<span data-ttu-id="816d3-114">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="816d3-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="816d3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="816d3-115">-Name</span></span>
<span data-ttu-id="816d3-116">Gibt den Namen der hinzuzufügenden Konfiguration des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="816d3-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="816d3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="816d3-117">CommonParameters</span></span>
<span data-ttu-id="816d3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="816d3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="816d3-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="816d3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="816d3-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="816d3-120">INPUTS</span></span>

### <span data-ttu-id="816d3-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="816d3-121">PSLoadBalancer</span></span>
<span data-ttu-id="816d3-122">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="816d3-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="816d3-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="816d3-123">OUTPUTS</span></span>

### <span data-ttu-id="816d3-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="816d3-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="816d3-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="816d3-125">NOTES</span></span>

## <span data-ttu-id="816d3-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="816d3-126">RELATED LINKS</span></span>

[<span data-ttu-id="816d3-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="816d3-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="816d3-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="816d3-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="816d3-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="816d3-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="816d3-130">Neu – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="816d3-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="816d3-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="816d3-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


