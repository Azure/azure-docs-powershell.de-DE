---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ac96a07fb7ec32589ac351fc592c4c2848e75978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479529"
---
# <span data-ttu-id="50d90-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="50d90-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="50d90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50d90-102">SYNOPSIS</span></span>
<span data-ttu-id="50d90-103">Fügt eine ausgehende Regelkonfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="50d90-103">Adds an outbound rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50d90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50d90-104">SYNTAX</span></span>

### <span data-ttu-id="50d90-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="50d90-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50d90-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="50d90-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50d90-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50d90-107">DESCRIPTION</span></span>
<span data-ttu-id="50d90-108">Mit dem Cmdlet **Add-AzureRmLoadBalancerOutboundRuleConfig** wird eine ausgehende Regelkonfiguration zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="50d90-108">The **Add-AzureRmLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="50d90-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50d90-109">EXAMPLES</span></span>

### <span data-ttu-id="50d90-110">Beispiel 1: Hinzufügen einer ausgehenden Regelkonfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="50d90-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="50d90-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="50d90-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="50d90-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an **Add-AzureRmLoadBalancerOutboundRuleConfig** zu übergeben, wodurch dem Lastenausgleichsmodul eine ausgehende Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="50d90-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="50d90-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="50d90-113">PARAMETERS</span></span>

### <span data-ttu-id="50d90-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="50d90-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="50d90-115">Die Anzahl der ausgehenden Ports, die für NAT verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="50d90-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="50d90-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50d90-116">-BackendAddressPool</span></span>
<span data-ttu-id="50d90-117">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="50d90-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="50d90-118">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="50d90-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d90-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="50d90-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="50d90-120">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="50d90-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="50d90-121">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="50d90-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d90-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d90-122">-DefaultProfile</span></span>
<span data-ttu-id="50d90-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50d90-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50d90-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="50d90-124">-EnableTcpReset</span></span>
<span data-ttu-id="50d90-125">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="50d90-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="50d90-126">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="50d90-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="50d90-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="50d90-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="50d90-128">Die Frontend-IP-Adressen des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="50d90-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d90-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="50d90-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="50d90-130">Timeout für die TCP-Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="50d90-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="50d90-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50d90-131">-LoadBalancer</span></span>
<span data-ttu-id="50d90-132">Der Verweis der Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="50d90-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="50d90-133">-Name</span><span class="sxs-lookup"><span data-stu-id="50d90-133">-Name</span></span>
<span data-ttu-id="50d90-134">Der Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="50d90-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="50d90-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="50d90-135">-Protocol</span></span>
<span data-ttu-id="50d90-136">Protokoll – TCP, UDP oder alle</span><span class="sxs-lookup"><span data-stu-id="50d90-136">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d90-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="50d90-137">-Confirm</span></span>
<span data-ttu-id="50d90-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50d90-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50d90-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50d90-139">-WhatIf</span></span>
<span data-ttu-id="50d90-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50d90-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50d90-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50d90-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50d90-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d90-142">CommonParameters</span></span>
<span data-ttu-id="50d90-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d90-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d90-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d90-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d90-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50d90-145">INPUTS</span></span>

### <span data-ttu-id="50d90-146">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50d90-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="50d90-147">System. Int32 System. String System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Network. Models. PSResourceId; Microsoft. Azure. Commands. Network; Version = 6.5.0.0; Kultur = neutral; PublicKeyToken = null]] Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50d90-147">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="50d90-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50d90-148">OUTPUTS</span></span>

### <span data-ttu-id="50d90-149">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50d90-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="50d90-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="50d90-150">NOTES</span></span>

## <span data-ttu-id="50d90-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50d90-151">RELATED LINKS</span></span>
