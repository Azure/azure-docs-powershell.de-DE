---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50a8cd14c6ea61f7c772df96f4addb9ae7955444
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821563"
---
# <span data-ttu-id="2f7d4-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f7d4-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="2f7d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7d4-103">Erstellt eine ausgehende Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="2f7d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f7d4-104">SYNTAX</span></span>

### <span data-ttu-id="2f7d4-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f7d4-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f7d4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f7d4-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f7d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f7d4-107">DESCRIPTION</span></span>
<span data-ttu-id="2f7d4-108">Das Cmdlet **New-AzLoadBalancerOutboundRuleConfig** erstellt eine ausgehende Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="2f7d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f7d4-109">EXAMPLES</span></span>

### <span data-ttu-id="2f7d4-110">Beispiel 1: Erstellen einer ausgehenden Regelkonfiguration für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="2f7d4-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="2f7d4-111">Der erste Befehl erstellt eine öffentliche IP-Adresse mit dem Namen MyPublicIP in der Ressourcengruppe mit dem Namen myresourcegroup und speichert Sie dann in der $publicip-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="2f7d4-112">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip und speichert Sie dann in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="2f7d4-113">Der dritte Befehl erstellt eine Konfiguration des Back-End-Adresspools mit dem Namen BackendAddressPool01 und speichert ihn dann in der $Backend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="2f7d4-114">Der vierte Befehl erstellt eine ausgehende Regelkonfiguration mit dem Namen MyOutboundRule unter Verwendung der Front-End-und Back-End-Objekte in $Frontend und $Backend.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="2f7d4-115">Die Parameter *Protocol* , *FrontendIPConfiguration* und *BackendAddressPool* sind alle zum Erstellen einer ausgehenden Regelkonfiguration erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="2f7d4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f7d4-116">PARAMETERS</span></span>

### <span data-ttu-id="2f7d4-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="2f7d4-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="2f7d4-118">Die Anzahl der ausgehenden Ports, die für NAT verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-118">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="2f7d4-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2f7d4-119">-BackendAddressPool</span></span>
<span data-ttu-id="2f7d4-120">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="2f7d4-121">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="2f7d4-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2f7d4-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="2f7d4-123">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="2f7d4-124">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="2f7d4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7d4-125">-DefaultProfile</span></span>
<span data-ttu-id="2f7d4-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f7d4-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2f7d4-127">-EnableTcpReset</span></span>
<span data-ttu-id="2f7d4-128">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="2f7d4-129">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="2f7d4-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f7d4-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="2f7d4-131">Die Frontend-IP-Adressen des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-131">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="2f7d4-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2f7d4-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2f7d4-133">Timeout für die TCP-Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="2f7d4-133">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="2f7d4-134">-Name</span><span class="sxs-lookup"><span data-stu-id="2f7d4-134">-Name</span></span>
<span data-ttu-id="2f7d4-135">Der Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="2f7d4-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2f7d4-136">-Protocol</span></span>
<span data-ttu-id="2f7d4-137">Protokoll – TCP, UDP oder alle</span><span class="sxs-lookup"><span data-stu-id="2f7d4-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="2f7d4-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f7d4-138">-Confirm</span></span>
<span data-ttu-id="2f7d4-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f7d4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f7d4-140">-WhatIf</span></span>
<span data-ttu-id="2f7d4-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f7d4-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f7d4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7d4-143">CommonParameters</span></span>
<span data-ttu-id="2f7d4-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f7d4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7d4-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f7d4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7d4-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f7d4-146">INPUTS</span></span>

### <span data-ttu-id="2f7d4-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2f7d4-147">System.Int32</span></span>

### <span data-ttu-id="2f7d4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2f7d4-148">System.String</span></span>

### <span data-ttu-id="2f7d4-149">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="2f7d4-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="2f7d4-150">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2f7d4-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="2f7d4-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f7d4-151">OUTPUTS</span></span>

### <span data-ttu-id="2f7d4-152">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="2f7d4-152">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="2f7d4-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f7d4-153">NOTES</span></span>

## <span data-ttu-id="2f7d4-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f7d4-154">RELATED LINKS</span></span>

[<span data-ttu-id="2f7d4-155">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f7d4-155">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="2f7d4-156">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f7d4-156">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="2f7d4-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f7d4-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="2f7d4-158">Satz-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f7d4-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
