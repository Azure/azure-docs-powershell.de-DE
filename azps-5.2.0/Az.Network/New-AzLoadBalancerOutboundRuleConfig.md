---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 9bc4c582956b30a8298b9579d92b2cd4fe0e31a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362478"
---
# <span data-ttu-id="f7f52-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7f52-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="f7f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f52-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f52-103">Erstellt eine ausgehende Regelkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="f7f52-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="f7f52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7f52-104">SYNTAX</span></span>

### <span data-ttu-id="f7f52-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7f52-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7f52-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7f52-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7f52-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7f52-107">DESCRIPTION</span></span>
<span data-ttu-id="f7f52-108">Das **Cmdlet "New-AzLoadBalancerOutboundRuleConfig"** erstellt eine ausgehende Regelkonfiguration für einen Azure-Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="f7f52-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f7f52-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7f52-109">EXAMPLES</span></span>

### <span data-ttu-id="f7f52-110">Beispiel 1: Erstellen einer ausgehenden Regelkonfiguration für einen Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="f7f52-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="f7f52-111">Der erste Befehl erstellt eine öffentliche IP-Adresse namens "MyPublicIP" in der Ressourcengruppe namens "MyResourceGroup" und speichert sie dann in der $publicip Variable.</span><span class="sxs-lookup"><span data-stu-id="f7f52-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="f7f52-112">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration namens FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip und speichert sie dann in der $frontend Variable.</span><span class="sxs-lookup"><span data-stu-id="f7f52-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="f7f52-113">Der dritte Befehl erstellt eine Back-End-Adresspoolkonfiguration namens Back-End-Adresspool01 und speichert sie dann in der $backend Variable.</span><span class="sxs-lookup"><span data-stu-id="f7f52-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="f7f52-114">Der vierte Befehl erstellt eine ausgehende Regelkonfiguration namens "MyOutboundRule" mit den Front-End- und Back-End-Objekten in $frontend und $backend.</span><span class="sxs-lookup"><span data-stu-id="f7f52-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="f7f52-115">Die *Parameter "Protocol",* *"FrontendIPConfiguration"* und *"Back-EndAddressPool"* sind alle erforderlich, um eine ausgehende Regelkonfiguration zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7f52-115">The *Protocol*, *FrontendIPConfiguration*, and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="f7f52-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f7f52-116">Example 2</span></span>

<span data-ttu-id="f7f52-117">Erstellt eine ausgehende Regelkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="f7f52-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="f7f52-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="f7f52-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="f7f52-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7f52-119">PARAMETERS</span></span>

### <span data-ttu-id="f7f52-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="f7f52-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="f7f52-121">Die Anzahl der ausgehenden Ports, die für NAT verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7f52-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="f7f52-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7f52-122">-BackendAddressPool</span></span>
<span data-ttu-id="f7f52-123">Ein Verweis auf einen Pool von DIPs.</span><span class="sxs-lookup"><span data-stu-id="f7f52-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="f7f52-124">Ausgehender Datenverkehr wird nach dem Zufallsprinzip für alle IPs in den Back-End-IPs geladen.</span><span class="sxs-lookup"><span data-stu-id="f7f52-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="f7f52-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f7f52-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="f7f52-126">Ein Verweis auf einen Pool von DIPs.</span><span class="sxs-lookup"><span data-stu-id="f7f52-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="f7f52-127">Ausgehender Datenverkehr wird nach dem Zufallsprinzip für alle IPs in den Back-End-IPs geladen.</span><span class="sxs-lookup"><span data-stu-id="f7f52-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="f7f52-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f52-128">-DefaultProfile</span></span>
<span data-ttu-id="f7f52-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7f52-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7f52-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f7f52-130">-EnableTcpReset</span></span>
<span data-ttu-id="f7f52-131">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f7f52-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="f7f52-132">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f7f52-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="f7f52-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7f52-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f7f52-134">Die Frontend-IP-Adressen des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="f7f52-134">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f52-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f7f52-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f7f52-136">Timeout für die TCP-Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="f7f52-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="f7f52-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f7f52-137">-Name</span></span>
<span data-ttu-id="f7f52-138">Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="f7f52-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="f7f52-139">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f7f52-139">-Protocol</span></span>
<span data-ttu-id="f7f52-140">Protokoll – TCP, UDP oder Alle</span><span class="sxs-lookup"><span data-stu-id="f7f52-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="f7f52-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7f52-141">-Confirm</span></span>
<span data-ttu-id="f7f52-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7f52-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f52-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f7f52-143">-WhatIf</span></span>
<span data-ttu-id="f7f52-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7f52-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f52-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7f52-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f52-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f52-146">CommonParameters</span></span>
<span data-ttu-id="f7f52-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f52-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f52-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f52-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f52-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7f52-149">INPUTS</span></span>

### <span data-ttu-id="f7f52-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f7f52-150">System.Int32</span></span>

### <span data-ttu-id="f7f52-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f7f52-151">System.String</span></span>

### <span data-ttu-id="f7f52-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="f7f52-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="f7f52-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7f52-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f7f52-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7f52-154">OUTPUTS</span></span>

### <span data-ttu-id="f7f52-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="f7f52-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="f7f52-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7f52-156">NOTES</span></span>

## <span data-ttu-id="f7f52-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7f52-157">RELATED LINKS</span></span>

[<span data-ttu-id="f7f52-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7f52-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="f7f52-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7f52-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="f7f52-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7f52-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="f7f52-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7f52-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
