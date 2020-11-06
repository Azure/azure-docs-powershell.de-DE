---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 402235f4d98b39ec78ffdc67bd0a01ab16e0400a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479530"
---
# <span data-ttu-id="e36da-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e36da-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="e36da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e36da-102">SYNOPSIS</span></span>
<span data-ttu-id="e36da-103">Fügt eine eingehende NAT-Regelkonfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="e36da-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e36da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e36da-104">SYNTAX</span></span>

### <span data-ttu-id="e36da-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="e36da-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e36da-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e36da-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e36da-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e36da-107">DESCRIPTION</span></span>
<span data-ttu-id="e36da-108">Mit dem Cmdlet **Add-AzureRmLoadBalancerInboundNatRuleConfig** wird eine eingehende NAT-Regelkonfiguration (Netzwerkadressübersetzung) zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e36da-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="e36da-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e36da-109">EXAMPLES</span></span>

### <span data-ttu-id="e36da-110">Beispiel 1: Hinzufügen einer eingehenden NAT-Regelkonfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="e36da-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="e36da-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyloadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="e36da-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e36da-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an **Add-AzureRmLoadBalancerInboundNatRuleConfig** zu übergeben, wodurch dem Lastenausgleichsmodul eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e36da-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="e36da-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e36da-113">PARAMETERS</span></span>

### <span data-ttu-id="e36da-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e36da-114">-BackendPort</span></span>
<span data-ttu-id="e36da-115">Gibt den Back-End-Port für Datenverkehr an, der mit einer Regelkonfiguration übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e36da-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36da-116">-DefaultProfile</span></span>
<span data-ttu-id="e36da-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e36da-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e36da-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="e36da-118">-EnableFloatingIP</span></span>
<span data-ttu-id="e36da-119">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e36da-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36da-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="e36da-120">-EnableTcpReset</span></span>
<span data-ttu-id="e36da-121">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="e36da-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="e36da-122">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="e36da-122">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36da-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e36da-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e36da-124">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e36da-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36da-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e36da-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="e36da-126">Gibt eine ID für die Konfiguration einer Front-End-IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="e36da-126">Specifies an ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36da-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e36da-127">-FrontendPort</span></span>
<span data-ttu-id="e36da-128">Gibt den Front-End-Port an, der einer Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e36da-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36da-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e36da-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e36da-130">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="e36da-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36da-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e36da-131">-LoadBalancer</span></span>
<span data-ttu-id="e36da-132">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e36da-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="e36da-133">Dieses Cmdlet fügt dem Load Balancer eine eingehende NAT-Regelkonfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e36da-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="e36da-134">-Name</span><span class="sxs-lookup"><span data-stu-id="e36da-134">-Name</span></span>
<span data-ttu-id="e36da-135">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e36da-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36da-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e36da-136">-Protocol</span></span>
<span data-ttu-id="e36da-137">Gibt das Protokoll an, das einer eingehenden NAT-Regel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e36da-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="e36da-138">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="e36da-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36da-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e36da-139">-Confirm</span></span>
<span data-ttu-id="e36da-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e36da-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e36da-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e36da-141">-WhatIf</span></span>
<span data-ttu-id="e36da-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e36da-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e36da-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e36da-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e36da-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36da-144">CommonParameters</span></span>
<span data-ttu-id="e36da-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36da-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36da-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36da-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36da-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e36da-147">INPUTS</span></span>

### <span data-ttu-id="e36da-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e36da-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="e36da-149">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e36da-149">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="e36da-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e36da-150">OUTPUTS</span></span>

### <span data-ttu-id="e36da-151">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e36da-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e36da-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="e36da-152">NOTES</span></span>

## <span data-ttu-id="e36da-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e36da-153">RELATED LINKS</span></span>

[<span data-ttu-id="e36da-154">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e36da-154">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e36da-155">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e36da-155">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e36da-156">Neu – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e36da-156">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e36da-157">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e36da-157">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e36da-158">Satz-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e36da-158">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="e36da-159">Satz-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e36da-159">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


