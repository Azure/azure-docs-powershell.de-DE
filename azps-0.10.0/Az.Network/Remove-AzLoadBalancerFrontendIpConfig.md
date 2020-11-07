---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9782d56fb18f0f00c52e9ff37ef0d62a609f980
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841152"
---
# <span data-ttu-id="5b751-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b751-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="5b751-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b751-102">SYNOPSIS</span></span>
<span data-ttu-id="5b751-103">Entfernt eine Front-End-IP-Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="5b751-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="5b751-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b751-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b751-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b751-105">DESCRIPTION</span></span>
<span data-ttu-id="5b751-106">Das Cmdlet **Remove-AzLoadBalancerFrontendIpConfig** entfernt eine Front-End-IP-Konfiguration von einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="5b751-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="5b751-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b751-107">EXAMPLES</span></span>

### <span data-ttu-id="5b751-108">Beispiel 1: Entfernen einer Front-End-IP-Konfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="5b751-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="5b751-109">Der erste Befehl ruft das Load Balancer ab, das der Front-End-IP-Konfiguration zugeordnet ist, die Sie entfernen möchten, und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5b751-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="5b751-110">Der zweite Befehl entfernt die zugehörige Frontend-IP-Konfiguration aus dem Load Balancer in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="5b751-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="5b751-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b751-111">PARAMETERS</span></span>

### <span data-ttu-id="5b751-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b751-112">-DefaultProfile</span></span>
<span data-ttu-id="5b751-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b751-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b751-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b751-114">-LoadBalancer</span></span>
<span data-ttu-id="5b751-115">Gibt das Load Balancer an, das die zu entfernende Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="5b751-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="5b751-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5b751-116">-Name</span></span>
<span data-ttu-id="5b751-117">Gibt den Namen der zu entfernenden Front-End-IP-Adressenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5b751-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="5b751-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b751-118">CommonParameters</span></span>
<span data-ttu-id="5b751-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b751-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b751-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b751-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b751-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b751-121">INPUTS</span></span>

### <span data-ttu-id="5b751-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b751-122">PSLoadBalancer</span></span>
<span data-ttu-id="5b751-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b751-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5b751-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b751-124">OUTPUTS</span></span>

### <span data-ttu-id="5b751-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b751-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5b751-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b751-126">NOTES</span></span>

## <span data-ttu-id="5b751-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b751-127">RELATED LINKS</span></span>

[<span data-ttu-id="5b751-128">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b751-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5b751-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b751-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5b751-130">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b751-130">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5b751-131">Neu – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b751-131">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5b751-132">Satz-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b751-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


