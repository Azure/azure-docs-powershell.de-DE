---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 192eb5ebfa21c97aa7043c4d4719831def08d93e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850647"
---
# <span data-ttu-id="ad718-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad718-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="ad718-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad718-102">SYNOPSIS</span></span>
<span data-ttu-id="ad718-103">Entfernt eine Front-End-IP-Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="ad718-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad718-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad718-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad718-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad718-105">DESCRIPTION</span></span>
<span data-ttu-id="ad718-106">Das Cmdlet **Remove-AzureRmLoadBalancerFrontendIpConfig** entfernt eine Front-End-IP-Konfiguration von einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="ad718-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="ad718-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad718-107">EXAMPLES</span></span>

### <span data-ttu-id="ad718-108">Beispiel 1: Entfernen einer Front-End-IP-Konfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="ad718-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="ad718-109">Der erste Befehl ruft das Load Balancer ab, das der Front-End-IP-Konfiguration zugeordnet ist, die Sie entfernen möchten, und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ad718-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="ad718-110">Der zweite Befehl entfernt die zugehörige Frontend-IP-Konfiguration aus dem Load Balancer in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="ad718-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="ad718-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad718-111">PARAMETERS</span></span>

### <span data-ttu-id="ad718-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad718-112">-DefaultProfile</span></span>
<span data-ttu-id="ad718-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad718-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad718-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad718-114">-LoadBalancer</span></span>
<span data-ttu-id="ad718-115">Gibt das Load Balancer an, das die zu entfernende Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="ad718-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="ad718-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ad718-116">-Name</span></span>
<span data-ttu-id="ad718-117">Gibt den Namen der zu entfernenden Front-End-IP-Adressenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ad718-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="ad718-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad718-118">CommonParameters</span></span>
<span data-ttu-id="ad718-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad718-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad718-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad718-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad718-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad718-121">INPUTS</span></span>

### <span data-ttu-id="ad718-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad718-122">PSLoadBalancer</span></span>
<span data-ttu-id="ad718-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad718-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ad718-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad718-124">OUTPUTS</span></span>

### <span data-ttu-id="ad718-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad718-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ad718-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad718-126">NOTES</span></span>

## <span data-ttu-id="ad718-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad718-127">RELATED LINKS</span></span>

[<span data-ttu-id="ad718-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad718-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ad718-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad718-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ad718-130">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad718-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ad718-131">Neu – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad718-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ad718-132">Satz-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad718-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


