---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: bed9eebb8812c0bd75eb19c3e8666d6a3b418a13
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850627"
---
# <span data-ttu-id="b30d7-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b30d7-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="b30d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b30d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b30d7-103">Entfernt eine Prüf Punkt Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="b30d7-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b30d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b30d7-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b30d7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b30d7-105">DESCRIPTION</span></span>
<span data-ttu-id="b30d7-106">Das Cmdlet **Remove-AzureRmLoadBalancerProbeConfig** entfernt eine Prüf Punkt Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="b30d7-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="b30d7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b30d7-107">EXAMPLES</span></span>

### <span data-ttu-id="b30d7-108">Beispiel 1: Entfernen einer Prüf Punkt Konfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="b30d7-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="b30d7-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b30d7-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="b30d7-110">Der zweite Befehl löscht die Konfiguration mit dem Namen myprobe aus dem Lastenausgleichsmodul in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="b30d7-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="b30d7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b30d7-111">PARAMETERS</span></span>

### <span data-ttu-id="b30d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30d7-112">-DefaultProfile</span></span>
<span data-ttu-id="b30d7-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b30d7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b30d7-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b30d7-114">-LoadBalancer</span></span>
<span data-ttu-id="b30d7-115">Gibt das Load Balancer an, das die vom Cmdlet entfernte Prüf Punkt Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="b30d7-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b30d7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b30d7-116">-Name</span></span>
<span data-ttu-id="b30d7-117">Gibt den Namen der Prüf Punkt Konfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b30d7-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b30d7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30d7-118">CommonParameters</span></span>
<span data-ttu-id="b30d7-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30d7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30d7-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b30d7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30d7-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b30d7-121">INPUTS</span></span>

### <span data-ttu-id="b30d7-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b30d7-122">PSLoadBalancer</span></span>
<span data-ttu-id="b30d7-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b30d7-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b30d7-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b30d7-124">OUTPUTS</span></span>

### <span data-ttu-id="b30d7-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b30d7-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b30d7-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b30d7-126">NOTES</span></span>

## <span data-ttu-id="b30d7-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b30d7-127">RELATED LINKS</span></span>

[<span data-ttu-id="b30d7-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b30d7-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="b30d7-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b30d7-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b30d7-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b30d7-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="b30d7-131">Neu – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b30d7-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="b30d7-132">Satz-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b30d7-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


