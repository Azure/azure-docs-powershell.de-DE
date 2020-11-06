---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b51c7300296644ffeda75d1fb9e4cf695ff61def
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479466"
---
# <span data-ttu-id="d2590-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2590-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="d2590-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2590-102">SYNOPSIS</span></span>
<span data-ttu-id="d2590-103">Entfernt eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="d2590-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2590-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2590-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2590-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2590-105">DESCRIPTION</span></span>
<span data-ttu-id="d2590-106">Das Cmdlet **Remove-AzureRmLoadBalancerRuleConfig** entfernt eine Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="d2590-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d2590-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2590-107">EXAMPLES</span></span>

### <span data-ttu-id="d2590-108">Beispiel 1: Entfernen einer Regelkonfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="d2590-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d2590-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d2590-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="d2590-110">Der zweite Befehl entfernt die Regelkonfiguration mit dem Namen MyLBruleName aus dem Lastenausgleichsmodul in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d2590-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="d2590-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2590-111">PARAMETERS</span></span>

### <span data-ttu-id="d2590-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2590-112">-DefaultProfile</span></span>
<span data-ttu-id="d2590-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2590-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2590-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2590-114">-LoadBalancer</span></span>
<span data-ttu-id="d2590-115">Gibt das **LoadBalancer** -Objekt an, das die vom Cmdlet entfernte Regelkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="d2590-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d2590-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d2590-116">-Name</span></span>
<span data-ttu-id="d2590-117">Gibt den Namen der Load Balancer-Regelkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d2590-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d2590-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2590-118">-Confirm</span></span>
<span data-ttu-id="d2590-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2590-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2590-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2590-120">-WhatIf</span></span>
<span data-ttu-id="d2590-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2590-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2590-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2590-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2590-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2590-123">CommonParameters</span></span>
<span data-ttu-id="d2590-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2590-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2590-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2590-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2590-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2590-126">INPUTS</span></span>

### <span data-ttu-id="d2590-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2590-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="d2590-128">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2590-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="d2590-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2590-129">OUTPUTS</span></span>

### <span data-ttu-id="d2590-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2590-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d2590-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2590-131">NOTES</span></span>

## <span data-ttu-id="d2590-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2590-132">RELATED LINKS</span></span>

[<span data-ttu-id="d2590-133">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2590-133">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="d2590-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2590-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d2590-135">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2590-135">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="d2590-136">Neu – AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2590-136">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="d2590-137">Satz-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2590-137">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


