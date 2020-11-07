---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: e3afa3ee5809af2760225be674990827c117bdfa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821535"
---
# <span data-ttu-id="3aa87-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3aa87-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="3aa87-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3aa87-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa87-103">Erstellt eine Netzwerk Sicherheitsregel-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3aa87-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="3aa87-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aa87-104">SYNTAX</span></span>

### <span data-ttu-id="3aa87-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="3aa87-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3aa87-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa87-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aa87-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3aa87-107">DESCRIPTION</span></span>
<span data-ttu-id="3aa87-108">Das Cmdlet **New-AzNetworkSecurityRuleConfig** erstellt eine Azure Network Security Rule-Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3aa87-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="3aa87-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3aa87-109">EXAMPLES</span></span>

### <span data-ttu-id="3aa87-110">1: Erstellen einer Netzwerk Sicherheitsregel zum Zulassen von RDP</span><span class="sxs-lookup"><span data-stu-id="3aa87-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="3aa87-111">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff aus dem Internet auf Port 3389 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="3aa87-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="3aa87-112">2: Erstellen einer Netzwerk Sicherheitsregel, die http zulässt</span><span class="sxs-lookup"><span data-stu-id="3aa87-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="3aa87-113">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff aus dem Internet auf Port 80 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="3aa87-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="3aa87-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3aa87-114">PARAMETERS</span></span>

### <span data-ttu-id="3aa87-115">-Access</span><span class="sxs-lookup"><span data-stu-id="3aa87-115">-Access</span></span>
<span data-ttu-id="3aa87-116">Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="3aa87-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="3aa87-117">Zulässige Werte für diesen Parameter sind: allow und Deny.</span><span class="sxs-lookup"><span data-stu-id="3aa87-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="3aa87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa87-118">-DefaultProfile</span></span>
<span data-ttu-id="3aa87-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3aa87-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aa87-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3aa87-120">-Description</span></span>
<span data-ttu-id="3aa87-121">Gibt eine Beschreibung der zu erstellenden Netzwerk Sicherheitsregel Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="3aa87-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="3aa87-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3aa87-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="3aa87-123">Gibt ein Ziel Adresspräfix an.</span><span class="sxs-lookup"><span data-stu-id="3aa87-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="3aa87-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3aa87-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3aa87-125">Eine CIDR-Adresse (classlos InterDomain Routing)</span><span class="sxs-lookup"><span data-stu-id="3aa87-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="3aa87-126">Ein Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="3aa87-126">A destination IP address range</span></span> 
- <span data-ttu-id="3aa87-127">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht, die Sie mit Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden können.</span><span class="sxs-lookup"><span data-stu-id="3aa87-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="3aa87-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3aa87-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="3aa87-129">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3aa87-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3aa87-130">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3aa87-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3aa87-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3aa87-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="3aa87-132">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3aa87-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3aa87-133">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3aa87-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3aa87-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="3aa87-134">-DestinationPortRange</span></span>
<span data-ttu-id="3aa87-135">Gibt einen Zielport oder einen Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="3aa87-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="3aa87-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3aa87-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3aa87-137">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="3aa87-137">An integer</span></span>
- <span data-ttu-id="3aa87-138">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="3aa87-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3aa87-139">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="3aa87-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="3aa87-140">-Richtung</span><span class="sxs-lookup"><span data-stu-id="3aa87-140">-Direction</span></span>
<span data-ttu-id="3aa87-141">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="3aa87-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="3aa87-142">Die zulässigen Werte für diesen Parameter lauten: ein-und ausgehende.</span><span class="sxs-lookup"><span data-stu-id="3aa87-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="3aa87-143">-Name</span><span class="sxs-lookup"><span data-stu-id="3aa87-143">-Name</span></span>
<span data-ttu-id="3aa87-144">Gibt den Namen der von diesem Cmdlet erstellten Konfiguration der Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="3aa87-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3aa87-145">-Priorität</span><span class="sxs-lookup"><span data-stu-id="3aa87-145">-Priority</span></span>
<span data-ttu-id="3aa87-146">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="3aa87-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="3aa87-147">Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="3aa87-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="3aa87-148">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="3aa87-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="3aa87-149">Je niedriger die Prioritätszahl ist, desto höher ist die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="3aa87-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="3aa87-150">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3aa87-150">-Protocol</span></span>
<span data-ttu-id="3aa87-151">Gibt das Netzwerkprotokoll an, für das eine neue Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="3aa87-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="3aa87-152">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3aa87-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3aa87-153">TCP</span><span class="sxs-lookup"><span data-stu-id="3aa87-153">Tcp</span></span>
- <span data-ttu-id="3aa87-154">UDP</span><span class="sxs-lookup"><span data-stu-id="3aa87-154">Udp</span></span>
- <span data-ttu-id="3aa87-155">Platzhalterzeichen (\*), um beide zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3aa87-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="3aa87-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3aa87-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="3aa87-157">Gibt das Präfix einer Quelladresse an.</span><span class="sxs-lookup"><span data-stu-id="3aa87-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="3aa87-158">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3aa87-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3aa87-159">ein CIDR</span><span class="sxs-lookup"><span data-stu-id="3aa87-159">A CIDR</span></span>
- <span data-ttu-id="3aa87-160">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="3aa87-160">A source IP range</span></span>
- <span data-ttu-id="3aa87-161">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="3aa87-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="3aa87-162">Sie können auch Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.</span><span class="sxs-lookup"><span data-stu-id="3aa87-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="3aa87-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3aa87-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="3aa87-164">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3aa87-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="3aa87-165">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3aa87-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3aa87-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3aa87-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="3aa87-167">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3aa87-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="3aa87-168">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3aa87-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3aa87-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="3aa87-169">-SourcePortRange</span></span>
<span data-ttu-id="3aa87-170">Gibt den Quell Port oder-Bereich an.</span><span class="sxs-lookup"><span data-stu-id="3aa87-170">Specifies the source port or range.</span></span>
<span data-ttu-id="3aa87-171">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3aa87-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3aa87-172">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="3aa87-172">An integer</span></span>
- <span data-ttu-id="3aa87-173">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="3aa87-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3aa87-174">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="3aa87-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="3aa87-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa87-175">CommonParameters</span></span>
<span data-ttu-id="3aa87-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa87-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa87-177">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa87-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa87-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3aa87-178">INPUTS</span></span>

### <span data-ttu-id="3aa87-179">Keine</span><span class="sxs-lookup"><span data-stu-id="3aa87-179">None</span></span>

## <span data-ttu-id="3aa87-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3aa87-180">OUTPUTS</span></span>

### <span data-ttu-id="3aa87-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="3aa87-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="3aa87-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="3aa87-182">NOTES</span></span>

## <span data-ttu-id="3aa87-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3aa87-183">RELATED LINKS</span></span>

[<span data-ttu-id="3aa87-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3aa87-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3aa87-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3aa87-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3aa87-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3aa87-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3aa87-187">Satz-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3aa87-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


