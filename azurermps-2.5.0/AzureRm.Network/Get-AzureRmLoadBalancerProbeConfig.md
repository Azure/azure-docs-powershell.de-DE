---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 30989d3b9c71821c2eae3cdfd97f9e4e5fc0cb15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850727"
---
# <span data-ttu-id="246a6-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="246a6-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="246a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="246a6-102">SYNOPSIS</span></span>
<span data-ttu-id="246a6-103">Ruft eine Prüf Punkt Konfiguration für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="246a6-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="246a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="246a6-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="246a6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="246a6-105">DESCRIPTION</span></span>
<span data-ttu-id="246a6-106">Das Cmdlet " **Get-AzureRmLoadBalancerProbeConfig** " ruft mindestens eine Prüf Punkt Konfiguration für ein Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="246a6-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="246a6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="246a6-107">EXAMPLES</span></span>

### <span data-ttu-id="246a6-108">Beispiel 1: Abrufen der Prüf Punkt Konfiguration eines Lastenausgleichsmoduls</span><span class="sxs-lookup"><span data-stu-id="246a6-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="246a6-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="246a6-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="246a6-110">Der zweite Befehl ruft die zugeordnete Prüf Punkt Konfiguration mit dem Namen myprobe vom Lastenausgleichsmodul in $SLB ab.</span><span class="sxs-lookup"><span data-stu-id="246a6-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="246a6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="246a6-111">PARAMETERS</span></span>

### <span data-ttu-id="246a6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246a6-112">-DefaultProfile</span></span>
<span data-ttu-id="246a6-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="246a6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="246a6-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="246a6-114">-LoadBalancer</span></span>
<span data-ttu-id="246a6-115">Gibt das Load Balancer an, das der abzurufenden Prüf Punkt Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="246a6-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="246a6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="246a6-116">-Name</span></span>
<span data-ttu-id="246a6-117">Gibt den Namen der abzurufenden Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="246a6-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="246a6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246a6-118">CommonParameters</span></span>
<span data-ttu-id="246a6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="246a6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246a6-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="246a6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246a6-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="246a6-121">INPUTS</span></span>

### <span data-ttu-id="246a6-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="246a6-122">PSLoadBalancer</span></span>
<span data-ttu-id="246a6-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="246a6-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="246a6-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="246a6-124">OUTPUTS</span></span>

### <span data-ttu-id="246a6-125">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="246a6-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="246a6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="246a6-126">NOTES</span></span>

## <span data-ttu-id="246a6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="246a6-127">RELATED LINKS</span></span>

[<span data-ttu-id="246a6-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="246a6-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="246a6-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="246a6-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="246a6-130">Neu – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="246a6-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="246a6-131">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="246a6-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="246a6-132">Satz-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="246a6-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


