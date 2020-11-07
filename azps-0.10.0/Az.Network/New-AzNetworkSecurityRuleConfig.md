---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 17e73f28595a0b99c8209634a6dee6838fa4599d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841308"
---
# <span data-ttu-id="7270b-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7270b-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="7270b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7270b-102">SYNOPSIS</span></span>
<span data-ttu-id="7270b-103">Erstellt eine Netzwerk Sicherheitsregel-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7270b-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="7270b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7270b-104">SYNTAX</span></span>

### <span data-ttu-id="7270b-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="7270b-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7270b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7270b-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7270b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7270b-107">DESCRIPTION</span></span>
<span data-ttu-id="7270b-108">Das Cmdlet **New-AzNetworkSecurityRuleConfig** erstellt eine Azure Network Security Rule-Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7270b-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="7270b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7270b-109">EXAMPLES</span></span>

### <span data-ttu-id="7270b-110">1: Erstellen einer Netzwerk Sicherheitsregel zum Zulassen von RDP</span><span class="sxs-lookup"><span data-stu-id="7270b-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="7270b-111">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff aus dem Internet auf Port 3389 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="7270b-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="7270b-112">2: Erstellen einer Netzwerk Sicherheitsregel, die http zulässt</span><span class="sxs-lookup"><span data-stu-id="7270b-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="7270b-113">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff aus dem Internet auf Port 80 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="7270b-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="7270b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7270b-114">PARAMETERS</span></span>

### <span data-ttu-id="7270b-115">-Access</span><span class="sxs-lookup"><span data-stu-id="7270b-115">-Access</span></span>
<span data-ttu-id="7270b-116">Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="7270b-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="7270b-117">Zulässige Werte für diesen Parameter sind: allow und Deny.</span><span class="sxs-lookup"><span data-stu-id="7270b-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7270b-118">-DefaultProfile</span></span>
<span data-ttu-id="7270b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7270b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7270b-120">-Description</span></span>
<span data-ttu-id="7270b-121">Gibt eine Beschreibung der zu erstellenden Netzwerk Sicherheitsregel Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="7270b-121">Specifies a description of the network security rule configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7270b-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="7270b-123">Gibt ein Ziel Adresspräfix an.</span><span class="sxs-lookup"><span data-stu-id="7270b-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="7270b-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7270b-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7270b-125">Eine CIDR-Adresse (classlos InterDomain Routing)</span><span class="sxs-lookup"><span data-stu-id="7270b-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="7270b-126">Ein Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="7270b-126">A destination IP address range</span></span> 
- <span data-ttu-id="7270b-127">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht</span><span class="sxs-lookup"><span data-stu-id="7270b-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="7270b-128">Sie können Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.</span><span class="sxs-lookup"><span data-stu-id="7270b-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7270b-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="7270b-130">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7270b-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="7270b-131">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7270b-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7270b-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="7270b-133">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7270b-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="7270b-134">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7270b-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="7270b-135">-DestinationPortRange</span></span>
<span data-ttu-id="7270b-136">Gibt einen Zielport oder einen Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="7270b-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="7270b-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7270b-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7270b-138">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="7270b-138">An integer</span></span>
- <span data-ttu-id="7270b-139">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="7270b-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="7270b-140">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="7270b-140">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-141">-Richtung</span><span class="sxs-lookup"><span data-stu-id="7270b-141">-Direction</span></span>
<span data-ttu-id="7270b-142">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="7270b-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="7270b-143">Die zulässigen Werte für diesen Parameter lauten: ein-und ausgehende.</span><span class="sxs-lookup"><span data-stu-id="7270b-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-144">-Name</span><span class="sxs-lookup"><span data-stu-id="7270b-144">-Name</span></span>
<span data-ttu-id="7270b-145">Gibt den Namen der von diesem Cmdlet erstellten Konfiguration der Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="7270b-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-146">-Priorität</span><span class="sxs-lookup"><span data-stu-id="7270b-146">-Priority</span></span>
<span data-ttu-id="7270b-147">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="7270b-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="7270b-148">Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="7270b-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="7270b-149">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7270b-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="7270b-150">Je niedriger die Prioritätszahl ist, desto höher ist die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="7270b-150">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-151">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7270b-151">-Protocol</span></span>
<span data-ttu-id="7270b-152">Gibt das Netzwerkprotokoll an, für das eine neue Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="7270b-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="7270b-153">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7270b-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7270b-154">TCP</span><span class="sxs-lookup"><span data-stu-id="7270b-154">Tcp</span></span>
- <span data-ttu-id="7270b-155">UDP</span><span class="sxs-lookup"><span data-stu-id="7270b-155">Udp</span></span>
- <span data-ttu-id="7270b-156">Platzhalterzeichen (\*), um beide zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7270b-156">wildcard character (\*) to match both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7270b-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="7270b-158">Gibt das Präfix einer Quelladresse an.</span><span class="sxs-lookup"><span data-stu-id="7270b-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="7270b-159">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7270b-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7270b-160">ein CIDR</span><span class="sxs-lookup"><span data-stu-id="7270b-160">A CIDR</span></span>
- <span data-ttu-id="7270b-161">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="7270b-161">A source IP range</span></span>
- <span data-ttu-id="7270b-162">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="7270b-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="7270b-163">Sie können auch Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.</span><span class="sxs-lookup"><span data-stu-id="7270b-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7270b-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="7270b-165">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7270b-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="7270b-166">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7270b-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7270b-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="7270b-168">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7270b-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="7270b-169">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7270b-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="7270b-170">-SourcePortRange</span></span>
<span data-ttu-id="7270b-171">Gibt den Quell Port oder-Bereich an.</span><span class="sxs-lookup"><span data-stu-id="7270b-171">Specifies the source port or range.</span></span>
<span data-ttu-id="7270b-172">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7270b-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7270b-173">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="7270b-173">An integer</span></span>
- <span data-ttu-id="7270b-174">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="7270b-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="7270b-175">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="7270b-175">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270b-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7270b-176">CommonParameters</span></span>
<span data-ttu-id="7270b-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7270b-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7270b-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7270b-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7270b-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7270b-179">INPUTS</span></span>

## <span data-ttu-id="7270b-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7270b-180">OUTPUTS</span></span>

### <span data-ttu-id="7270b-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="7270b-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="7270b-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="7270b-182">NOTES</span></span>

## <span data-ttu-id="7270b-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7270b-183">RELATED LINKS</span></span>

[<span data-ttu-id="7270b-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7270b-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7270b-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7270b-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7270b-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7270b-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7270b-187">Satz-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7270b-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


