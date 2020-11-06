---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1c813a7ac23ae8bc161f10df02ac618d5f6a7a81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498294"
---
# <span data-ttu-id="e5dd0-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5dd0-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="e5dd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="e5dd0-103">Legt eine ausgehende Regelkonfiguration für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-103">Sets an outbound rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5dd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5dd0-104">SYNTAX</span></span>

### <span data-ttu-id="e5dd0-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5dd0-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5dd0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5dd0-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5dd0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5dd0-107">DESCRIPTION</span></span>
<span data-ttu-id="e5dd0-108">Das Cmdlet " **Set-AzureRmLoadBalancerOutboundRuleConfig** " legt eine ausgehende Regelkonfiguration für ein Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-108">The **Set-AzureRmLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e5dd0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5dd0-109">EXAMPLES</span></span>

### <span data-ttu-id="e5dd0-110">Beispiel 1: Ändern der Konfiguration der ausgehenden Regel auf einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="e5dd0-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="e5dd0-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="e5dd0-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzureRmLoadBalancerOutboundRuleConfig zu übergeben, wodurch eine ausgehende Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="e5dd0-113">Der dritte Befehl übergibt das Load Balancer an " **AzureRmLoadBalancerOutboundRuleConfig** ", wodurch die Konfiguration der ausgehenden Regel gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="e5dd0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5dd0-114">PARAMETERS</span></span>

### <span data-ttu-id="e5dd0-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="e5dd0-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="e5dd0-116">Die Anzahl der ausgehenden Ports, die für NAT verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="e5dd0-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e5dd0-117">-BackendAddressPool</span></span>
<span data-ttu-id="e5dd0-118">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="e5dd0-119">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="e5dd0-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e5dd0-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="e5dd0-121">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="e5dd0-122">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="e5dd0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5dd0-123">-DefaultProfile</span></span>
<span data-ttu-id="e5dd0-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5dd0-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="e5dd0-125">-EnableTcpReset</span></span>
<span data-ttu-id="e5dd0-126">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="e5dd0-127">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e5dd0-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5dd0-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e5dd0-129">Die Frontend-IP-Adressen des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="e5dd0-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e5dd0-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e5dd0-131">Timeout für die TCP-Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="e5dd0-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="e5dd0-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5dd0-132">-LoadBalancer</span></span>
<span data-ttu-id="e5dd0-133">Der Verweis der Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="e5dd0-134">-Name</span><span class="sxs-lookup"><span data-stu-id="e5dd0-134">-Name</span></span>
<span data-ttu-id="e5dd0-135">Der Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="e5dd0-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e5dd0-136">-Protocol</span></span>
<span data-ttu-id="e5dd0-137">Protokoll – TCP, UDP oder alle</span><span class="sxs-lookup"><span data-stu-id="e5dd0-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="e5dd0-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5dd0-138">-Confirm</span></span>
<span data-ttu-id="e5dd0-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5dd0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5dd0-140">-WhatIf</span></span>
<span data-ttu-id="e5dd0-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5dd0-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5dd0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5dd0-143">CommonParameters</span></span>
<span data-ttu-id="e5dd0-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5dd0-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5dd0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5dd0-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5dd0-146">INPUTS</span></span>

### <span data-ttu-id="e5dd0-147">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5dd0-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="e5dd0-148">System. Int32 System. String System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Network. Models. PSResourceId; Microsoft. Azure. Commands. Network; Version = 6.5.0.0; Kultur = neutral; PublicKeyToken = null]] Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e5dd0-148">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e5dd0-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5dd0-149">OUTPUTS</span></span>

### <span data-ttu-id="e5dd0-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5dd0-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e5dd0-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5dd0-151">NOTES</span></span>

## <span data-ttu-id="e5dd0-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5dd0-152">RELATED LINKS</span></span>
