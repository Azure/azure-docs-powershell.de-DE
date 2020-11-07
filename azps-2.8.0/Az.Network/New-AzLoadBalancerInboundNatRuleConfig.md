---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6f724cb7208afb1a5f9474048b5e2dc46c17f5af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823059"
---
# <span data-ttu-id="bf569-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf569-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="bf569-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf569-102">SYNOPSIS</span></span>
<span data-ttu-id="bf569-103">Erstellt eine eingehende NAT-Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="bf569-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="bf569-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf569-104">SYNTAX</span></span>

### <span data-ttu-id="bf569-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf569-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf569-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf569-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf569-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf569-107">DESCRIPTION</span></span>
<span data-ttu-id="bf569-108">Das Cmdlet **New-AzLoadBalancerInboundNatRuleConfig** erstellt eine eingehende NAT-Regelkonfiguration für ein Azure-Lastenausgleichssystem.</span><span class="sxs-lookup"><span data-stu-id="bf569-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="bf569-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf569-109">EXAMPLES</span></span>

### <span data-ttu-id="bf569-110">Beispiel 1: Erstellen einer eingehenden NAT-Regelkonfiguration für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="bf569-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="bf569-111">Der erste Befehl erstellt eine öffentliche IP-Adresse mit dem Namen MyPublicIP in der Ressourcengruppe mit dem Namen myresourcegroup und speichert Sie dann in der $publicip-Variablen.</span><span class="sxs-lookup"><span data-stu-id="bf569-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="bf569-112">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip und speichert Sie dann in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="bf569-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="bf569-113">Der dritte Befehl erstellt eine eingehende NAT-Regelkonfiguration mit dem Namen MyInboundNatRule mit dem Front-End-Objekt in $Frontend.</span><span class="sxs-lookup"><span data-stu-id="bf569-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="bf569-114">Das TCP-Protokoll wird angegeben, und der Front-End-Port ist 3389, derselbe wie der Back-End-Port in diesem Fall.</span><span class="sxs-lookup"><span data-stu-id="bf569-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="bf569-115">Die *FrontendIpConfiguration* -, *Protocol* -, *FrontendPort* -und *BackendPort* -Parameter sind alle erforderlich, um eine eingehende NAT-Regelkonfiguration zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bf569-115">The *FrontendIpConfiguration* , *Protocol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="bf569-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf569-116">PARAMETERS</span></span>

### <span data-ttu-id="bf569-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="bf569-117">-BackendPort</span></span>
<span data-ttu-id="bf569-118">Gibt den Back-End-Port für Datenverkehr an, der von dieser Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="bf569-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="bf569-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf569-119">-DefaultProfile</span></span>
<span data-ttu-id="bf569-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf569-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf569-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="bf569-121">-EnableFloatingIP</span></span>
<span data-ttu-id="bf569-122">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf569-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="bf569-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="bf569-123">-EnableTcpReset</span></span>
<span data-ttu-id="bf569-124">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="bf569-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="bf569-125">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="bf569-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="bf569-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf569-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="bf569-127">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bf569-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bf569-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bf569-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="bf569-129">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="bf569-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="bf569-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="bf569-130">-FrontendPort</span></span>
<span data-ttu-id="bf569-131">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="bf569-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bf569-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bf569-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bf569-133">Gibt die Zeitdauer in Minuten an, für die der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="bf569-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="bf569-134">-Name</span><span class="sxs-lookup"><span data-stu-id="bf569-134">-Name</span></span>
<span data-ttu-id="bf569-135">Gibt den Namen der Regelkonfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf569-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bf569-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="bf569-136">-Protocol</span></span>
<span data-ttu-id="bf569-137">Gibt ein Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="bf569-137">Specifies a protocol.</span></span>
<span data-ttu-id="bf569-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bf569-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bf569-139">TCP</span><span class="sxs-lookup"><span data-stu-id="bf569-139">Tcp</span></span>
- <span data-ttu-id="bf569-140">UDP</span><span class="sxs-lookup"><span data-stu-id="bf569-140">Udp</span></span>

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

### <span data-ttu-id="bf569-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf569-141">-Confirm</span></span>
<span data-ttu-id="bf569-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf569-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf569-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf569-143">-WhatIf</span></span>
<span data-ttu-id="bf569-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf569-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf569-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf569-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf569-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf569-146">CommonParameters</span></span>
<span data-ttu-id="bf569-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf569-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf569-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf569-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf569-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf569-149">INPUTS</span></span>

### <span data-ttu-id="bf569-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bf569-150">System.String</span></span>

### <span data-ttu-id="bf569-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bf569-151">System.Int32</span></span>

### <span data-ttu-id="bf569-152">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf569-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="bf569-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf569-153">OUTPUTS</span></span>

### <span data-ttu-id="bf569-154">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="bf569-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="bf569-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf569-155">NOTES</span></span>

## <span data-ttu-id="bf569-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf569-156">RELATED LINKS</span></span>

[<span data-ttu-id="bf569-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf569-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bf569-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf569-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bf569-159">Neu – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf569-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="bf569-160">Neu – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bf569-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="bf569-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf569-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bf569-162">Satz-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf569-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


