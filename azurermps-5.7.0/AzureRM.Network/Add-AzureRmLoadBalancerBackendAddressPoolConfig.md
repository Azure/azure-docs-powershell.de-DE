---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 82775229bc368f80c03a886b10a631a4482341df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496453"
---
# <span data-ttu-id="c65df-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c65df-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="c65df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c65df-102">SYNOPSIS</span></span>
<span data-ttu-id="c65df-103">Fügt eine Konfiguration des Back-End-Adresspools zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="c65df-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c65df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c65df-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c65df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c65df-105">DESCRIPTION</span></span>
<span data-ttu-id="c65df-106">Das Cmdlet **Add-AzureRmLoadBalancerBackend** fügt einem Azure Load Balancer einen Back-End-Adresspool hinzu.</span><span class="sxs-lookup"><span data-stu-id="c65df-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="c65df-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c65df-107">EXAMPLES</span></span>

### <span data-ttu-id="c65df-108">Beispiel 1 Hinzufügen einer Konfiguration des Back-End-Adresspools zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="c65df-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="c65df-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab, fügt den Back-End-Adresspool mit dem Namen BackendAddressPool02 zu MyLoadBalancer hinzu und verwendet dann das Cmdlet " **Satz-AzureRmLoadBalancer** ", um MyLoadBalancer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c65df-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="c65df-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c65df-110">PARAMETERS</span></span>

### <span data-ttu-id="c65df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65df-111">-DefaultProfile</span></span>
<span data-ttu-id="c65df-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c65df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c65df-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c65df-113">-LoadBalancer</span></span>
<span data-ttu-id="c65df-114">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c65df-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="c65df-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c65df-115">-Name</span></span>
<span data-ttu-id="c65df-116">Gibt den Namen der hinzuzufügenden Konfiguration des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="c65df-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="c65df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65df-117">CommonParameters</span></span>
<span data-ttu-id="c65df-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c65df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65df-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65df-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65df-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c65df-120">INPUTS</span></span>

### <span data-ttu-id="c65df-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c65df-121">PSLoadBalancer</span></span>
<span data-ttu-id="c65df-122">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c65df-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c65df-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c65df-123">OUTPUTS</span></span>

### <span data-ttu-id="c65df-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c65df-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c65df-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="c65df-125">NOTES</span></span>

## <span data-ttu-id="c65df-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c65df-126">RELATED LINKS</span></span>

[<span data-ttu-id="c65df-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c65df-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c65df-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c65df-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="c65df-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c65df-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c65df-130">Neu – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c65df-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c65df-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c65df-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


