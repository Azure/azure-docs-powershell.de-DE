---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 9bc4c582956b30a8298b9579d92b2cd4fe0e31a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009679"
---
# <span data-ttu-id="8ebee-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ebee-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="8ebee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ebee-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebee-103">Erstellt eine ausgehende Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="8ebee-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="8ebee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ebee-104">SYNTAX</span></span>

### <span data-ttu-id="8ebee-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ebee-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ebee-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ebee-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ebee-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ebee-107">DESCRIPTION</span></span>
<span data-ttu-id="8ebee-108">Das Cmdlet **New-AzLoadBalancerOutboundRuleConfig** erstellt eine ausgehende Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="8ebee-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8ebee-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ebee-109">EXAMPLES</span></span>

### <span data-ttu-id="8ebee-110">Beispiel 1: Erstellen einer ausgehenden Regelkonfiguration für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="8ebee-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="8ebee-111">Der erste Befehl erstellt eine öffentliche IP-Adresse mit dem Namen MyPublicIP in der Ressourcengruppe mit dem Namen myresourcegroup und speichert Sie dann in der $publicip-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ebee-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="8ebee-112">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip und speichert Sie dann in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ebee-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="8ebee-113">Der dritte Befehl erstellt eine Konfiguration des Back-End-Adresspools mit dem Namen BackendAddressPool01 und speichert ihn dann in der $Backend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ebee-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="8ebee-114">Der vierte Befehl erstellt eine ausgehende Regelkonfiguration mit dem Namen MyOutboundRule unter Verwendung der Front-End-und Back-End-Objekte in $Frontend und $Backend.</span><span class="sxs-lookup"><span data-stu-id="8ebee-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="8ebee-115">Die Parameter *Protocol* , *FrontendIPConfiguration* und *BackendAddressPool* sind alle zum Erstellen einer ausgehenden Regelkonfiguration erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ebee-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="8ebee-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8ebee-116">Example 2</span></span>

<span data-ttu-id="8ebee-117">Erstellt eine ausgehende Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="8ebee-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="8ebee-118">automatisch</span><span class="sxs-lookup"><span data-stu-id="8ebee-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="8ebee-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ebee-119">PARAMETERS</span></span>

### <span data-ttu-id="8ebee-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="8ebee-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="8ebee-121">Die Anzahl der ausgehenden Ports, die für NAT verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8ebee-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="8ebee-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8ebee-122">-BackendAddressPool</span></span>
<span data-ttu-id="8ebee-123">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="8ebee-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="8ebee-124">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="8ebee-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="8ebee-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8ebee-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="8ebee-126">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="8ebee-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="8ebee-127">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="8ebee-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="8ebee-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebee-128">-DefaultProfile</span></span>
<span data-ttu-id="8ebee-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ebee-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ebee-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8ebee-130">-EnableTcpReset</span></span>
<span data-ttu-id="8ebee-131">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="8ebee-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="8ebee-132">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="8ebee-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="8ebee-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ebee-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8ebee-134">Die Frontend-IP-Adressen des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="8ebee-134">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="8ebee-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8ebee-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8ebee-136">Timeout für die TCP-Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="8ebee-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="8ebee-137">-Name</span><span class="sxs-lookup"><span data-stu-id="8ebee-137">-Name</span></span>
<span data-ttu-id="8ebee-138">Der Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="8ebee-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="8ebee-139">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8ebee-139">-Protocol</span></span>
<span data-ttu-id="8ebee-140">Protokoll – TCP, UDP oder alle</span><span class="sxs-lookup"><span data-stu-id="8ebee-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="8ebee-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ebee-141">-Confirm</span></span>
<span data-ttu-id="8ebee-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ebee-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ebee-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ebee-143">-WhatIf</span></span>
<span data-ttu-id="8ebee-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ebee-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ebee-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ebee-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ebee-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebee-146">CommonParameters</span></span>
<span data-ttu-id="8ebee-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ebee-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebee-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ebee-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebee-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ebee-149">INPUTS</span></span>

### <span data-ttu-id="8ebee-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8ebee-150">System.Int32</span></span>

### <span data-ttu-id="8ebee-151">System. String</span><span class="sxs-lookup"><span data-stu-id="8ebee-151">System.String</span></span>

### <span data-ttu-id="8ebee-152">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="8ebee-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="8ebee-153">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8ebee-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="8ebee-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ebee-154">OUTPUTS</span></span>

### <span data-ttu-id="8ebee-155">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="8ebee-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="8ebee-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ebee-156">NOTES</span></span>

## <span data-ttu-id="8ebee-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ebee-157">RELATED LINKS</span></span>

[<span data-ttu-id="8ebee-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ebee-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="8ebee-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ebee-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="8ebee-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ebee-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="8ebee-161">Satz-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ebee-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
