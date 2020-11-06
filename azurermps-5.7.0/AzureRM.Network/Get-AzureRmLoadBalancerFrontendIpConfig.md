---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: f6de3902770fd799f8ce5a41d5aa1230e6821f02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478433"
---
# <span data-ttu-id="42add-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42add-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="42add-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42add-102">SYNOPSIS</span></span>
<span data-ttu-id="42add-103">Ruft eine Front-End-IP-Konfiguration in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="42add-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42add-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42add-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42add-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42add-105">DESCRIPTION</span></span>
<span data-ttu-id="42add-106">Das Cmdlet " **Get-AzureRmLoadBalancerFrontendIpConfig** " Ruft eine Front-End-IP-Konfiguration oder eine Liste der Front-End-IP-Konfigurationen in einem Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="42add-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="42add-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42add-107">EXAMPLES</span></span>

### <span data-ttu-id="42add-108">Beispiel 1: Abrufen einer Front-End-IP-Konfiguration in einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="42add-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="42add-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="42add-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="42add-110">Der zweite Befehl ruft die Front-End-IP-Konfiguration ab, die diesem Lastenausgleichsmodul zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="42add-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="42add-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="42add-111">PARAMETERS</span></span>

### <span data-ttu-id="42add-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42add-112">-DefaultProfile</span></span>
<span data-ttu-id="42add-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42add-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42add-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42add-114">-LoadBalancer</span></span>
<span data-ttu-id="42add-115">Gibt das Load Balancer an, das der zu erhaltenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="42add-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="42add-116">-Name</span><span class="sxs-lookup"><span data-stu-id="42add-116">-Name</span></span>
<span data-ttu-id="42add-117">Gibt den Namen des Load Balancer an, der die zu erhaltende Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="42add-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="42add-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42add-118">CommonParameters</span></span>
<span data-ttu-id="42add-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42add-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42add-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42add-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42add-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42add-121">INPUTS</span></span>

### <span data-ttu-id="42add-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42add-122">PSLoadBalancer</span></span>
<span data-ttu-id="42add-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="42add-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="42add-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42add-124">OUTPUTS</span></span>

### <span data-ttu-id="42add-125">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="42add-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="42add-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="42add-126">NOTES</span></span>

## <span data-ttu-id="42add-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42add-127">RELATED LINKS</span></span>

[<span data-ttu-id="42add-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42add-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="42add-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42add-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="42add-130">Neu – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42add-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="42add-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42add-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="42add-132">Satz-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42add-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


