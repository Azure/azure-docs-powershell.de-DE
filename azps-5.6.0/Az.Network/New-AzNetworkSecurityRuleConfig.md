---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 45702774e44e4b3da0b90d37e86e478c52dcba17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919576"
---
# <span data-ttu-id="40434-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="40434-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="40434-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40434-102">SYNOPSIS</span></span>
<span data-ttu-id="40434-103">Erstellt eine Netzwerksicherheitsregelkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="40434-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="40434-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40434-104">SYNTAX</span></span>

### <span data-ttu-id="40434-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="40434-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40434-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="40434-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40434-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40434-107">DESCRIPTION</span></span>
<span data-ttu-id="40434-108">Das **Cmdlet New-AzNetworkSecurityRuleConfig** erstellt eine Azure-Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="40434-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="40434-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40434-109">EXAMPLES</span></span>

### <span data-ttu-id="40434-110">Beispiel 1: Erstellen einer Netzwerksicherheitsregel zum Zulassen von RDP</span><span class="sxs-lookup"><span data-stu-id="40434-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="40434-111">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff vom Internet auf Port 3389 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="40434-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="40434-112">Beispiel 2: Erstellen einer Netzwerksicherheitsregel, die HTTP zulässt</span><span class="sxs-lookup"><span data-stu-id="40434-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="40434-113">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff vom Internet auf Port 80 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="40434-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="40434-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40434-114">PARAMETERS</span></span>

### <span data-ttu-id="40434-115">-Access</span><span class="sxs-lookup"><span data-stu-id="40434-115">-Access</span></span>
<span data-ttu-id="40434-116">Gibt an, ob Netzwerkdatenverkehr zulässig oder verweigert ist.</span><span class="sxs-lookup"><span data-stu-id="40434-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="40434-117">Die zulässigen Werte für diesen Parameter sind: Zulassen und Verweigern.</span><span class="sxs-lookup"><span data-stu-id="40434-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40434-118">-DefaultProfile</span></span>
<span data-ttu-id="40434-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40434-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40434-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40434-120">-Description</span></span>
<span data-ttu-id="40434-121">Gibt eine Beschreibung der zu erstellenden Netzwerksicherheitsregelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="40434-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="40434-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="40434-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="40434-123">Gibt ein Zieladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="40434-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="40434-124">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="40434-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="40434-125">Eine klassenloses domänenübergreifendes Routing (CIDR)</span><span class="sxs-lookup"><span data-stu-id="40434-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="40434-126">Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="40434-126">A destination IP address range</span></span> 
- <span data-ttu-id="40434-127">Platzhalterzeichen (\*) zur Übereinstimmung mit einer beliebigen IP-Adresse Sie können Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="40434-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="40434-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="40434-129">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="40434-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="40434-130">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40434-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="40434-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="40434-132">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="40434-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="40434-133">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40434-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="40434-134">-DestinationPortRange</span></span>
<span data-ttu-id="40434-135">Gibt einen Zielport oder -bereich an.</span><span class="sxs-lookup"><span data-stu-id="40434-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="40434-136">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="40434-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="40434-137">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="40434-137">An integer</span></span>
- <span data-ttu-id="40434-138">Ein Ganzzahlbereich zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="40434-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="40434-139">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einem beliebigen Port</span><span class="sxs-lookup"><span data-stu-id="40434-139">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-140">-Richtung</span><span class="sxs-lookup"><span data-stu-id="40434-140">-Direction</span></span>
<span data-ttu-id="40434-141">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="40434-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="40434-142">Die zulässigen Werte für diesen Parameter sind: Ein- und Ausgehend.</span><span class="sxs-lookup"><span data-stu-id="40434-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-143">-Name</span><span class="sxs-lookup"><span data-stu-id="40434-143">-Name</span></span>
<span data-ttu-id="40434-144">Gibt den Namen der Netzwerksicherheitsregelkonfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="40434-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="40434-145">-Priorität</span><span class="sxs-lookup"><span data-stu-id="40434-145">-Priority</span></span>
<span data-ttu-id="40434-146">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="40434-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="40434-147">Die zulässigen Werte für diesen Parameter sind: Eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="40434-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="40434-148">Die Prioritätsnummer muss für jede Regel in der Auflistung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="40434-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="40434-149">Je niedriger die Prioritätsnummer, desto höher die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="40434-149">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="40434-150">-Protocol</span></span>
<span data-ttu-id="40434-151">Gibt das Netzwerkprotokoll an, für das eine neue Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="40434-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="40434-152">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="40434-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="40434-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="40434-153">Tcp</span></span>
- <span data-ttu-id="40434-154">Udp</span><span class="sxs-lookup"><span data-stu-id="40434-154">Udp</span></span>
- <span data-ttu-id="40434-155">Platzhalterzeichen (\*) für beides.</span><span class="sxs-lookup"><span data-stu-id="40434-155">wildcard character (\*) to match both.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="40434-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="40434-157">Gibt ein Quelladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="40434-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="40434-158">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="40434-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="40434-159">A CIDR</span><span class="sxs-lookup"><span data-stu-id="40434-159">A CIDR</span></span>
- <span data-ttu-id="40434-160">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="40434-160">A source IP range</span></span>
- <span data-ttu-id="40434-161">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einer beliebigen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="40434-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="40434-162">Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="40434-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="40434-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="40434-164">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="40434-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="40434-165">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40434-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="40434-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="40434-167">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="40434-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="40434-168">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40434-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="40434-169">-SourcePortRange</span></span>
<span data-ttu-id="40434-170">Gibt den Quellport oder -bereich an.</span><span class="sxs-lookup"><span data-stu-id="40434-170">Specifies the source port or range.</span></span>
<span data-ttu-id="40434-171">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="40434-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="40434-172">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="40434-172">An integer</span></span>
- <span data-ttu-id="40434-173">Ein Ganzzahlbereich zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="40434-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="40434-174">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einem beliebigen Port</span><span class="sxs-lookup"><span data-stu-id="40434-174">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40434-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40434-175">CommonParameters</span></span>
<span data-ttu-id="40434-176">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40434-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40434-177">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40434-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40434-178">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40434-178">INPUTS</span></span>

### <span data-ttu-id="40434-179">Keine</span><span class="sxs-lookup"><span data-stu-id="40434-179">None</span></span>

## <span data-ttu-id="40434-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40434-180">OUTPUTS</span></span>

### <span data-ttu-id="40434-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="40434-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="40434-182">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="40434-182">NOTES</span></span>

## <span data-ttu-id="40434-183">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="40434-183">RELATED LINKS</span></span>

[<span data-ttu-id="40434-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="40434-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="40434-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="40434-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="40434-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="40434-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="40434-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="40434-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


