---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 1a71b48387948d65ba0db24fdb2c236a11a9a44d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505301"
---
# <span data-ttu-id="fb142-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb142-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="fb142-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb142-102">SYNOPSIS</span></span>
<span data-ttu-id="fb142-103">Entfernt eine Front-End-IP-Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="fb142-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb142-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb142-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb142-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb142-105">DESCRIPTION</span></span>
<span data-ttu-id="fb142-106">Das Cmdlet **Remove-AzureRmLoadBalancerFrontendIpConfig** entfernt eine Front-End-IP-Konfiguration von einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="fb142-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="fb142-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb142-107">EXAMPLES</span></span>

### <span data-ttu-id="fb142-108">Beispiel 1: Entfernen einer Front-End-IP-Konfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="fb142-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="fb142-109">Der erste Befehl ruft das Load Balancer ab, das der Front-End-IP-Konfiguration zugeordnet ist, die Sie entfernen möchten, und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb142-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="fb142-110">Der zweite Befehl entfernt die zugehörige Frontend-IP-Konfiguration aus dem Load Balancer in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="fb142-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="fb142-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb142-111">PARAMETERS</span></span>

### <span data-ttu-id="fb142-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb142-112">-DefaultProfile</span></span>
<span data-ttu-id="fb142-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb142-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb142-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb142-114">-LoadBalancer</span></span>
<span data-ttu-id="fb142-115">Gibt das Load Balancer an, das die zu entfernende Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="fb142-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="fb142-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fb142-116">-Name</span></span>
<span data-ttu-id="fb142-117">Gibt den Namen der zu entfernenden Front-End-IP-Adressenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="fb142-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="fb142-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb142-118">-Confirm</span></span>
<span data-ttu-id="fb142-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb142-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb142-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb142-120">-WhatIf</span></span>
<span data-ttu-id="fb142-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb142-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb142-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb142-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb142-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb142-123">CommonParameters</span></span>
<span data-ttu-id="fb142-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb142-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb142-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb142-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb142-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb142-126">INPUTS</span></span>

### <span data-ttu-id="fb142-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb142-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="fb142-128">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fb142-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="fb142-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb142-129">OUTPUTS</span></span>

### <span data-ttu-id="fb142-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb142-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fb142-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb142-131">NOTES</span></span>

## <span data-ttu-id="fb142-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb142-132">RELATED LINKS</span></span>

[<span data-ttu-id="fb142-133">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb142-133">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="fb142-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb142-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="fb142-135">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb142-135">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="fb142-136">Neu – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb142-136">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="fb142-137">Satz-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb142-137">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


