---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a0b1acf49aa177d05be7361eedf644320b609797
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841636"
---
# <span data-ttu-id="ca86a-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca86a-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="ca86a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca86a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca86a-103">Ruft eine Front-End-IP-Konfiguration in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="ca86a-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="ca86a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca86a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca86a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca86a-105">DESCRIPTION</span></span>
<span data-ttu-id="ca86a-106">Das Cmdlet " **Get-AzLoadBalancerFrontendIpConfig** " Ruft eine Front-End-IP-Konfiguration oder eine Liste der Front-End-IP-Konfigurationen in einem Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="ca86a-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="ca86a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca86a-107">EXAMPLES</span></span>

### <span data-ttu-id="ca86a-108">Beispiel 1: Abrufen einer Front-End-IP-Konfiguration in einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="ca86a-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="ca86a-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="ca86a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="ca86a-110">Der zweite Befehl ruft die Front-End-IP-Konfiguration ab, die diesem Lastenausgleichsmodul zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ca86a-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="ca86a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca86a-111">PARAMETERS</span></span>

### <span data-ttu-id="ca86a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca86a-112">-DefaultProfile</span></span>
<span data-ttu-id="ca86a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca86a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca86a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca86a-114">-LoadBalancer</span></span>
<span data-ttu-id="ca86a-115">Gibt das Load Balancer an, das der zu erhaltenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ca86a-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="ca86a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ca86a-116">-Name</span></span>
<span data-ttu-id="ca86a-117">Gibt den Namen des Load Balancer an, der die zu erhaltende Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="ca86a-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="ca86a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca86a-118">CommonParameters</span></span>
<span data-ttu-id="ca86a-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca86a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca86a-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca86a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca86a-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca86a-121">INPUTS</span></span>

### <span data-ttu-id="ca86a-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca86a-122">PSLoadBalancer</span></span>
<span data-ttu-id="ca86a-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca86a-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ca86a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca86a-124">OUTPUTS</span></span>

### <span data-ttu-id="ca86a-125">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca86a-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ca86a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca86a-126">NOTES</span></span>

## <span data-ttu-id="ca86a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca86a-127">RELATED LINKS</span></span>

[<span data-ttu-id="ca86a-128">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca86a-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ca86a-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca86a-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ca86a-130">Neu – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca86a-130">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ca86a-131">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca86a-131">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ca86a-132">Satz-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca86a-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


