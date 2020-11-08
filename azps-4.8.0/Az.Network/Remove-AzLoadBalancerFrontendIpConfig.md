---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165185"
---
# <span data-ttu-id="aee21-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aee21-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="aee21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aee21-102">SYNOPSIS</span></span>
<span data-ttu-id="aee21-103">Entfernt eine Front-End-IP-Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="aee21-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="aee21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aee21-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aee21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aee21-105">DESCRIPTION</span></span>
<span data-ttu-id="aee21-106">Das Cmdlet **Remove-AzLoadBalancerFrontendIpConfig** entfernt eine Front-End-IP-Konfiguration von einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="aee21-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="aee21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aee21-107">EXAMPLES</span></span>

### <span data-ttu-id="aee21-108">Beispiel 1: Entfernen einer Front-End-IP-Konfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="aee21-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="aee21-109">Der erste Befehl ruft das Load Balancer ab, das der Front-End-IP-Konfiguration zugeordnet ist, die Sie entfernen möchten, und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="aee21-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="aee21-110">Der zweite Befehl entfernt die zugehörige Frontend-IP-Konfiguration aus dem Load Balancer in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="aee21-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="aee21-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="aee21-111">PARAMETERS</span></span>

### <span data-ttu-id="aee21-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee21-112">-DefaultProfile</span></span>
<span data-ttu-id="aee21-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aee21-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aee21-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aee21-114">-LoadBalancer</span></span>
<span data-ttu-id="aee21-115">Gibt das Load Balancer an, das die zu entfernende Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="aee21-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="aee21-116">-Name</span><span class="sxs-lookup"><span data-stu-id="aee21-116">-Name</span></span>
<span data-ttu-id="aee21-117">Gibt den Namen der zu entfernenden Front-End-IP-Adressenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="aee21-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="aee21-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aee21-118">-Confirm</span></span>
<span data-ttu-id="aee21-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aee21-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee21-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee21-120">-WhatIf</span></span>
<span data-ttu-id="aee21-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aee21-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aee21-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aee21-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee21-123">CommonParameters</span></span>
<span data-ttu-id="aee21-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aee21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee21-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aee21-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee21-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aee21-126">INPUTS</span></span>

### <span data-ttu-id="aee21-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aee21-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="aee21-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aee21-128">OUTPUTS</span></span>

### <span data-ttu-id="aee21-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aee21-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="aee21-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="aee21-130">NOTES</span></span>

## <span data-ttu-id="aee21-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aee21-131">RELATED LINKS</span></span>

[<span data-ttu-id="aee21-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aee21-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="aee21-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aee21-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="aee21-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aee21-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="aee21-135">Neu – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aee21-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="aee21-136">Satz-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aee21-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


