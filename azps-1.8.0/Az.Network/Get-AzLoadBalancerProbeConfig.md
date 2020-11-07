---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4b880e98a2b0352591e4a4e8840500ba2d25e431
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660755"
---
# <span data-ttu-id="3f543-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3f543-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="3f543-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f543-102">SYNOPSIS</span></span>
<span data-ttu-id="3f543-103">Ruft eine Prüf Punkt Konfiguration für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="3f543-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="3f543-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f543-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f543-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f543-105">DESCRIPTION</span></span>
<span data-ttu-id="3f543-106">Das Cmdlet " **Get-AzLoadBalancerProbeConfig** " ruft mindestens eine Prüf Punkt Konfiguration für ein Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="3f543-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="3f543-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f543-107">EXAMPLES</span></span>

### <span data-ttu-id="3f543-108">Beispiel 1: Abrufen der Prüf Punkt Konfiguration eines Lastenausgleichsmoduls</span><span class="sxs-lookup"><span data-stu-id="3f543-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="3f543-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="3f543-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="3f543-110">Der zweite Befehl ruft die zugeordnete Prüf Punkt Konfiguration mit dem Namen myprobe vom Lastenausgleichsmodul in $SLB ab.</span><span class="sxs-lookup"><span data-stu-id="3f543-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="3f543-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f543-111">PARAMETERS</span></span>

### <span data-ttu-id="3f543-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f543-112">-DefaultProfile</span></span>
<span data-ttu-id="3f543-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f543-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f543-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f543-114">-LoadBalancer</span></span>
<span data-ttu-id="3f543-115">Gibt das Load Balancer an, das der abzurufenden Prüf Punkt Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3f543-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f543-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3f543-116">-Name</span></span>
<span data-ttu-id="3f543-117">Gibt den Namen der abzurufenden Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="3f543-117">Specifies the name of the probe configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f543-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f543-118">CommonParameters</span></span>
<span data-ttu-id="3f543-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f543-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f543-120">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f543-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f543-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f543-121">INPUTS</span></span>

### <span data-ttu-id="3f543-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f543-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3f543-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f543-123">OUTPUTS</span></span>

### <span data-ttu-id="3f543-124">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="3f543-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="3f543-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f543-125">NOTES</span></span>

## <span data-ttu-id="3f543-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f543-126">RELATED LINKS</span></span>

[<span data-ttu-id="3f543-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3f543-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="3f543-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f543-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="3f543-129">Neu – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3f543-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="3f543-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3f543-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="3f543-131">Satz-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3f543-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


