---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: cff46867b92010969118ced67f53f5bd94c8337f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997185"
---
# <span data-ttu-id="184de-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184de-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="184de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="184de-102">SYNOPSIS</span></span>
<span data-ttu-id="184de-103">Aktualisiert eine Netzwerk Sicherheitsregel-Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="184de-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="184de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="184de-104">SYNTAX</span></span>

### <span data-ttu-id="184de-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="184de-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="184de-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="184de-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="184de-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="184de-107">DESCRIPTION</span></span>
<span data-ttu-id="184de-108">Das Cmdlet " **Satz-AzNetworkSecurityRuleConfig** " aktualisiert eine Netzwerk Sicherheitsregel-Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="184de-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="184de-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="184de-109">EXAMPLES</span></span>

### <span data-ttu-id="184de-110">Beispiel 1: Ändern der Zugriffskonfiguration in einer Netzwerk Sicherheitsregel</span><span class="sxs-lookup"><span data-stu-id="184de-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="184de-111">Der erste Befehl ruft die Netzwerksicherheitsgruppe mit dem Namen NSG-Frontend ab und speichert Sie dann in der Variablen $NSG.</span><span class="sxs-lookup"><span data-stu-id="184de-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="184de-112">Der zweite Befehl verwendet den Pipelineoperator, um die Sicherheitsgruppe in $NSG an Get-AzNetworkSecurityRuleConfig zu übergeben, wodurch die Sicherheitsregel Konfiguration mit dem Namen RDP-Rule abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="184de-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="184de-113">Der dritte Befehl ändert die Zugriffskonfiguration der RDP-Regel in Deny.</span><span class="sxs-lookup"><span data-stu-id="184de-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="184de-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="184de-114">PARAMETERS</span></span>

### <span data-ttu-id="184de-115">-Access</span><span class="sxs-lookup"><span data-stu-id="184de-115">-Access</span></span>
<span data-ttu-id="184de-116">Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="184de-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="184de-117">Zulässige Werte für diesen Parameter sind: allow und Deny.</span><span class="sxs-lookup"><span data-stu-id="184de-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="184de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184de-118">-DefaultProfile</span></span>
<span data-ttu-id="184de-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="184de-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="184de-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="184de-120">-Description</span></span>
<span data-ttu-id="184de-121">Gibt eine Beschreibung für eine Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="184de-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="184de-122">Die maximale Größe beträgt 140 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="184de-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="184de-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="184de-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="184de-124">Gibt ein Ziel Adresspräfix an.</span><span class="sxs-lookup"><span data-stu-id="184de-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="184de-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="184de-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="184de-126">Eine CIDR-Adresse (classlos InterDomain Routing)</span><span class="sxs-lookup"><span data-stu-id="184de-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="184de-127">Ein Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="184de-127">A destination IP address range</span></span> 
- <span data-ttu-id="184de-128">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht, die Sie mit Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden können.</span><span class="sxs-lookup"><span data-stu-id="184de-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="184de-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="184de-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="184de-130">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="184de-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="184de-131">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="184de-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="184de-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="184de-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="184de-133">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="184de-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="184de-134">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="184de-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="184de-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="184de-135">-DestinationPortRange</span></span>
<span data-ttu-id="184de-136">Gibt einen Zielport oder einen Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="184de-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="184de-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="184de-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="184de-138">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="184de-138">An integer</span></span> 
- <span data-ttu-id="184de-139">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="184de-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="184de-140">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="184de-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="184de-141">-Richtung</span><span class="sxs-lookup"><span data-stu-id="184de-141">-Direction</span></span>
<span data-ttu-id="184de-142">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="184de-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="184de-143">Die zulässigen Werte für diesen Parameter lauten: ein-und ausgehende.</span><span class="sxs-lookup"><span data-stu-id="184de-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="184de-144">-Name</span><span class="sxs-lookup"><span data-stu-id="184de-144">-Name</span></span>
<span data-ttu-id="184de-145">Gibt den Namen der Netzwerk Sicherheitsregel Konfiguration an, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="184de-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="184de-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="184de-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="184de-147">Gibt das **NetworkSecurityGroup** -Objekt an, das die festzulegende Netzwerk Sicherheitsregel Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="184de-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="184de-148">-Priorität</span><span class="sxs-lookup"><span data-stu-id="184de-148">-Priority</span></span>
<span data-ttu-id="184de-149">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="184de-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="184de-150">Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="184de-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="184de-151">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="184de-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="184de-152">Je niedriger die Prioritätszahl ist, desto höher ist die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="184de-152">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="184de-153">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="184de-153">-Protocol</span></span>
<span data-ttu-id="184de-154">Gibt das Netzwerkprotokoll an, für das eine Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="184de-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="184de-155">Die akzeptablen Werte für diesen Parameter sind:--TCP</span><span class="sxs-lookup"><span data-stu-id="184de-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="184de-156">UDP</span><span class="sxs-lookup"><span data-stu-id="184de-156">Udp</span></span>
- <span data-ttu-id="184de-157">Ein Platzhalterzeichen (\*), das mit beiden übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="184de-157">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="184de-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="184de-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="184de-159">Gibt das Präfix einer Quelladresse an.</span><span class="sxs-lookup"><span data-stu-id="184de-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="184de-160">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="184de-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="184de-161">ein CIDR</span><span class="sxs-lookup"><span data-stu-id="184de-161">A CIDR</span></span>
- <span data-ttu-id="184de-162">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="184de-162">A source IP range</span></span>
- <span data-ttu-id="184de-163">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="184de-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="184de-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="184de-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="184de-165">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="184de-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="184de-166">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="184de-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="184de-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="184de-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="184de-168">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="184de-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="184de-169">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="184de-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="184de-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="184de-170">-SourcePortRange</span></span>
<span data-ttu-id="184de-171">Gibt den Quell Port oder-Bereich an.</span><span class="sxs-lookup"><span data-stu-id="184de-171">Specifies the source port or range.</span></span>
<span data-ttu-id="184de-172">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="184de-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="184de-173">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="184de-173">An integer</span></span>
- <span data-ttu-id="184de-174">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="184de-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="184de-175">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="184de-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="184de-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184de-176">CommonParameters</span></span>
<span data-ttu-id="184de-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="184de-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184de-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="184de-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184de-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="184de-179">INPUTS</span></span>

### <span data-ttu-id="184de-180">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="184de-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="184de-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="184de-181">OUTPUTS</span></span>

### <span data-ttu-id="184de-182">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="184de-182">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="184de-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="184de-183">NOTES</span></span>

## <span data-ttu-id="184de-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="184de-184">RELATED LINKS</span></span>

[<span data-ttu-id="184de-185">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184de-185">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="184de-186">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184de-186">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="184de-187">Neu – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184de-187">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="184de-188">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184de-188">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


