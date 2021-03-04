---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: a6bec76345df188ca58e8b790637e35606de1f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943997"
---
# <span data-ttu-id="ba18e-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba18e-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ba18e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba18e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba18e-103">Erstellt eine eingehende NAT-Regelkonfiguration für einen Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="ba18e-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ba18e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba18e-104">SYNTAX</span></span>

### <span data-ttu-id="ba18e-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba18e-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba18e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba18e-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba18e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba18e-107">DESCRIPTION</span></span>
<span data-ttu-id="ba18e-108">Das **Cmdlet New-AzLoadBalancerInboundNatRuleConfig** erstellt eine Nat-Regelkonfiguration (Inbound Network Address Translation) für einen Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="ba18e-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ba18e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba18e-109">EXAMPLES</span></span>

### <span data-ttu-id="ba18e-110">Beispiel 1: Erstellen einer eingehenden NAT-Regelkonfiguration für einen Load Balancer</span><span class="sxs-lookup"><span data-stu-id="ba18e-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="ba18e-111">Mit dem ersten Befehl wird eine öffentliche IP-Adresse namens "MyPublicIP" in der Ressourcengruppe "MyResourceGroup" erstellt und dann in der $publicip gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ba18e-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="ba18e-112">Mit dem zweiten Befehl wird eine Front-End-IP-Konfiguration namens FrontendIpConfig01 mithilfe der öffentlichen IP-Adresse in $publicip erstellt und dann in der $frontend gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ba18e-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="ba18e-113">Mit dem dritten Befehl wird eine eingehende NAT-Regelkonfiguration mit dem Namen MyInboundNatRule mithilfe des Front-End-Objekts in $frontend.</span><span class="sxs-lookup"><span data-stu-id="ba18e-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="ba18e-114">Das TCP-Protokoll wird angegeben, und der Front-End-Port ist 3389, in diesem Fall identisch mit dem Back-End-Port.</span><span class="sxs-lookup"><span data-stu-id="ba18e-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="ba18e-115">Die *Parameter FrontendIpConfiguration,* *Protocol,* *FrontendPort* und *Back-EndPort* sind alle erforderlich, um eine eingehende NAT-Regelkonfiguration zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ba18e-115">The *FrontendIpConfiguration*, *Protocol*, *FrontendPort*, and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="ba18e-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba18e-116">PARAMETERS</span></span>

### <span data-ttu-id="ba18e-117">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="ba18e-117">-BackendPort</span></span>
<span data-ttu-id="ba18e-118">Gibt den Back-End-Port für Datenverkehr an, der mit dieser Regelkonfiguration übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="ba18e-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="ba18e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba18e-119">-DefaultProfile</span></span>
<span data-ttu-id="ba18e-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba18e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba18e-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ba18e-121">-EnableFloatingIP</span></span>
<span data-ttu-id="ba18e-122">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba18e-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ba18e-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ba18e-123">-EnableTcpReset</span></span>
<span data-ttu-id="ba18e-124">Empfangen eines bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="ba18e-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ba18e-125">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ba18e-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ba18e-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba18e-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ba18e-127">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ba18e-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ba18e-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ba18e-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ba18e-129">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ba18e-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ba18e-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ba18e-130">-FrontendPort</span></span>
<span data-ttu-id="ba18e-131">Gibt den Front-End-Port an, der mit einer Load Balancer-Regelkonfiguration übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="ba18e-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ba18e-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ba18e-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ba18e-133">Gibt die Dauer in Minuten an, für die der Zustand der Unterhaltungen in einem Lastenausgleich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="ba18e-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ba18e-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ba18e-134">-Name</span></span>
<span data-ttu-id="ba18e-135">Gibt den Namen der Regelkonfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ba18e-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ba18e-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ba18e-136">-Protocol</span></span>
<span data-ttu-id="ba18e-137">Gibt ein Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="ba18e-137">Specifies a protocol.</span></span>
<span data-ttu-id="ba18e-138">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ba18e-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba18e-139">Tcp</span><span class="sxs-lookup"><span data-stu-id="ba18e-139">Tcp</span></span>
- <span data-ttu-id="ba18e-140">Udp</span><span class="sxs-lookup"><span data-stu-id="ba18e-140">Udp</span></span>

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

### <span data-ttu-id="ba18e-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba18e-141">-Confirm</span></span>
<span data-ttu-id="ba18e-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba18e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba18e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba18e-143">-WhatIf</span></span>
<span data-ttu-id="ba18e-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba18e-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba18e-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba18e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba18e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba18e-146">CommonParameters</span></span>
<span data-ttu-id="ba18e-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba18e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba18e-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba18e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba18e-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba18e-149">INPUTS</span></span>

### <span data-ttu-id="ba18e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ba18e-150">System.String</span></span>

### <span data-ttu-id="ba18e-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ba18e-151">System.Int32</span></span>

### <span data-ttu-id="ba18e-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba18e-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ba18e-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba18e-153">OUTPUTS</span></span>

### <span data-ttu-id="ba18e-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="ba18e-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="ba18e-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba18e-155">NOTES</span></span>

## <span data-ttu-id="ba18e-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba18e-156">RELATED LINKS</span></span>

[<span data-ttu-id="ba18e-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba18e-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ba18e-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba18e-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ba18e-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ba18e-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ba18e-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ba18e-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="ba18e-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba18e-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ba18e-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba18e-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


