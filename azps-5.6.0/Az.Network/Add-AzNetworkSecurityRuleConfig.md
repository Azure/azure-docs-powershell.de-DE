---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 11481d2063b6acb2938361726de45f72dba539c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922827"
---
# <span data-ttu-id="79961-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79961-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="79961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79961-102">SYNOPSIS</span></span>
<span data-ttu-id="79961-103">Fügt einer Netzwerksicherheitsgruppe eine Netzwerksicherheitsregelkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="79961-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="79961-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79961-104">SYNTAX</span></span>

### <span data-ttu-id="79961-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="79961-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79961-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="79961-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79961-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79961-107">DESCRIPTION</span></span>
<span data-ttu-id="79961-108">Das **Add-AzNetworkSecurityRuleConfig-Cmdlet** fügt einer Azure-Netzwerksicherheitsgruppe eine Netzwerksicherheitsregelkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="79961-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="79961-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79961-109">EXAMPLES</span></span>

### <span data-ttu-id="79961-110">1: Hinzufügen einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="79961-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="79961-111">Der erste Befehl ruft eine Azure-Netzwerksicherheitsgruppe mit dem Namen "nsg1" aus der Ressourcengruppe "rg1" ab.</span><span class="sxs-lookup"><span data-stu-id="79961-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="79961-112">Der zweite Befehl fügt eine Netzwerksicherheitsregel mit dem Namen "rdp-rule" hinzu, die Datenverkehr aus dem Internet über Port 3389 zum abgerufenen Netzwerksicherheitsgruppeobjekt zulässt.</span><span class="sxs-lookup"><span data-stu-id="79961-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="79961-113">Die geänderte Azure-Netzwerksicherheitsgruppe wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="79961-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="79961-114">2: Hinzufügen einer neuen Sicherheitsregel mit Anwendungssicherheitsgruppen</span><span class="sxs-lookup"><span data-stu-id="79961-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="79961-115">Zuerst erstellen wir zwei neue Anwendungssicherheitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="79961-115">First, we create two new application security groups.</span></span> <span data-ttu-id="79961-116">Anschließend rufen wir eine Azure-Netzwerksicherheitsgruppe mit dem Namen "nsg1" aus der Ressourcengruppe "rg1" ab.</span><span class="sxs-lookup"><span data-stu-id="79961-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="79961-117">und fügen Sie eine Netzwerksicherheitsregel mit dem Namen "rdp-rule" hinzu.</span><span class="sxs-lookup"><span data-stu-id="79961-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="79961-118">Die Regel ermöglicht Datenverkehr von allen IP-Konfigurationen in der Anwendungssicherheitsgruppe "srcAsg" zu allen IP-Konfigurationen in "destAsg" auf Port 3389.</span><span class="sxs-lookup"><span data-stu-id="79961-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="79961-119">Nach dem Hinzufügen der Regel wird die geänderte Azure-Netzwerksicherheitsgruppe beibehalten.</span><span class="sxs-lookup"><span data-stu-id="79961-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="79961-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79961-120">PARAMETERS</span></span>

### <span data-ttu-id="79961-121">-Access</span><span class="sxs-lookup"><span data-stu-id="79961-121">-Access</span></span>
<span data-ttu-id="79961-122">Gibt an, ob Netzwerkdatenverkehr zulässig oder verweigert ist.</span><span class="sxs-lookup"><span data-stu-id="79961-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="79961-123">Die zulässigen Werte für diesen Parameter sind: Zulassen und Verweigern.</span><span class="sxs-lookup"><span data-stu-id="79961-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="79961-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79961-124">-DefaultProfile</span></span>
<span data-ttu-id="79961-125">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79961-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79961-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79961-126">-Description</span></span>
<span data-ttu-id="79961-127">Gibt eine Beschreibung einer Netzwerksicherheitsregelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="79961-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="79961-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="79961-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="79961-129">Gibt ein Zieladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="79961-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="79961-130">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="79961-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79961-131">Eine klassenloses domänenübergreifendes Routing (CIDR)</span><span class="sxs-lookup"><span data-stu-id="79961-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="79961-132">Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="79961-132">A destination IP address range</span></span>
- <span data-ttu-id="79961-133">Platzhalterzeichen (\*) zur Übereinstimmung mit einer beliebigen IP-Adresse Sie können Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="79961-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="79961-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79961-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="79961-135">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="79961-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="79961-136">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79961-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="79961-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="79961-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="79961-138">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="79961-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="79961-139">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79961-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="79961-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="79961-140">-DestinationPortRange</span></span>
<span data-ttu-id="79961-141">Gibt einen Zielport oder -bereich an.</span><span class="sxs-lookup"><span data-stu-id="79961-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="79961-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="79961-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79961-143">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="79961-143">An integer</span></span>
- <span data-ttu-id="79961-144">Ein Ganzzahlbereich zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="79961-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="79961-145">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einem beliebigen Port</span><span class="sxs-lookup"><span data-stu-id="79961-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="79961-146">-Richtung</span><span class="sxs-lookup"><span data-stu-id="79961-146">-Direction</span></span>
<span data-ttu-id="79961-147">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="79961-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="79961-148">Die zulässigen Werte für diesen Parameter sind: Ein- und Ausgehend.</span><span class="sxs-lookup"><span data-stu-id="79961-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="79961-149">-Name</span><span class="sxs-lookup"><span data-stu-id="79961-149">-Name</span></span>
<span data-ttu-id="79961-150">Gibt den Namen einer Netzwerksicherheitsregelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="79961-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="79961-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79961-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="79961-152">Gibt ein **NetworkSecurityGroup-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="79961-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="79961-153">Dieses Cmdlet fügt dem von diesem Parameter angegebenen Objekt eine Netzwerksicherheitsregelkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="79961-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79961-154">-Priorität</span><span class="sxs-lookup"><span data-stu-id="79961-154">-Priority</span></span>
<span data-ttu-id="79961-155">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="79961-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="79961-156">Die zulässigen Werte für diesen Parameter sind: Eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="79961-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="79961-157">Die Prioritätsnummer muss für jede Regel in der Auflistung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="79961-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="79961-158">Je niedriger die Prioritätsnummer, desto höher die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="79961-158">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="79961-159">-Protocol</span><span class="sxs-lookup"><span data-stu-id="79961-159">-Protocol</span></span>
<span data-ttu-id="79961-160">Gibt das Netzwerkprotokoll an, für das eine Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="79961-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="79961-161">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="79961-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79961-162">Tcp</span><span class="sxs-lookup"><span data-stu-id="79961-162">Tcp</span></span>
- <span data-ttu-id="79961-163">Udp</span><span class="sxs-lookup"><span data-stu-id="79961-163">Udp</span></span>
- <span data-ttu-id="79961-164">Platzhalterzeichen (\*) für beides</span><span class="sxs-lookup"><span data-stu-id="79961-164">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="79961-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="79961-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="79961-166">Gibt ein Quelladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="79961-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="79961-167">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="79961-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79961-168">A CIDR</span><span class="sxs-lookup"><span data-stu-id="79961-168">A CIDR</span></span>
- <span data-ttu-id="79961-169">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="79961-169">A source IP range</span></span>
- <span data-ttu-id="79961-170">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einer beliebigen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="79961-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="79961-171">Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="79961-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="79961-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79961-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="79961-173">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="79961-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="79961-174">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79961-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="79961-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="79961-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="79961-176">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="79961-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="79961-177">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79961-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="79961-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="79961-178">-SourcePortRange</span></span>
<span data-ttu-id="79961-179">Gibt einen Quellport oder -bereich an.</span><span class="sxs-lookup"><span data-stu-id="79961-179">Specifies a source port or range.</span></span>
<span data-ttu-id="79961-180">Dieser Wert wird als ganze Zahl, als Bereich zwischen 0 und 65535 oder als Platzhalterzeichen (\*) ausgedrückt, um einem beliebigen Quellport zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="79961-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="79961-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79961-181">CommonParameters</span></span>
<span data-ttu-id="79961-182">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79961-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79961-183">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79961-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79961-184">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79961-184">INPUTS</span></span>

### <span data-ttu-id="79961-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79961-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="79961-186">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79961-186">OUTPUTS</span></span>

### <span data-ttu-id="79961-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79961-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="79961-188">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79961-188">NOTES</span></span>

## <span data-ttu-id="79961-189">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79961-189">RELATED LINKS</span></span>

[<span data-ttu-id="79961-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79961-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="79961-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79961-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="79961-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79961-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="79961-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79961-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


