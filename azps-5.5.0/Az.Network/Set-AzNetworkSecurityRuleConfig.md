---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169631"
---
# <span data-ttu-id="56974-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56974-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="56974-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56974-102">SYNOPSIS</span></span>
<span data-ttu-id="56974-103">Aktualisiert die Konfiguration einer Netzwerksicherheitsregel für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="56974-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="56974-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56974-104">SYNTAX</span></span>

### <span data-ttu-id="56974-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="56974-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56974-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="56974-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56974-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56974-107">DESCRIPTION</span></span>
<span data-ttu-id="56974-108">Das **Cmdlet Set-AzNetworkSecurityRuleConfig** aktualisiert eine Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="56974-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="56974-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56974-109">EXAMPLES</span></span>

### <span data-ttu-id="56974-110">Beispiel 1: Ändern der Zugriffskonfiguration in einer Netzwerksicherheitsregel</span><span class="sxs-lookup"><span data-stu-id="56974-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="56974-111">Der erste Befehl ruft die Netzwerksicherheitsgruppe "NSG-FrontEnd" ab und speichert sie dann in der Variablengruppe $nsg.</span><span class="sxs-lookup"><span data-stu-id="56974-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="56974-112">Der zweite Befehl verwendet den Pipelineoperator, um die Sicherheitsgruppe in $nsg an Get-AzNetworkSecurityRuleConfig zu übergeben, die die Sicherheitsregelkonfiguration namens "rdp-rule" erhält.</span><span class="sxs-lookup"><span data-stu-id="56974-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="56974-113">Mit dem dritten Befehl wird die Zugriffskonfiguration von rdp-rule in "Verweigern" geändert.</span><span class="sxs-lookup"><span data-stu-id="56974-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="56974-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="56974-114">Example 2</span></span>

<span data-ttu-id="56974-115">Aktualisiert die Konfiguration einer Netzwerksicherheitsregel für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="56974-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="56974-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="56974-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="56974-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56974-117">PARAMETERS</span></span>

### <span data-ttu-id="56974-118">-Access</span><span class="sxs-lookup"><span data-stu-id="56974-118">-Access</span></span>
<span data-ttu-id="56974-119">Gibt an, ob Netzwerkdatenverkehr zulässig oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="56974-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="56974-120">Die zulässigen Werte für diesen Parameter sind: Zulassen und Verweigern.</span><span class="sxs-lookup"><span data-stu-id="56974-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="56974-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56974-121">-DefaultProfile</span></span>
<span data-ttu-id="56974-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56974-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56974-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56974-123">-Description</span></span>
<span data-ttu-id="56974-124">Gibt eine Beschreibung für eine Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="56974-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="56974-125">Die maximale Größe beträgt 140 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="56974-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="56974-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="56974-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="56974-127">Gibt ein Zieladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="56974-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="56974-128">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="56974-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56974-129">Eine klassenloses domänenübergreifendes Routing (CIDR)</span><span class="sxs-lookup"><span data-stu-id="56974-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="56974-130">Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="56974-130">A destination IP address range</span></span> 
- <span data-ttu-id="56974-131">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit beliebigen IP-Adressen. Sie können Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="56974-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="56974-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="56974-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="56974-133">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="56974-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="56974-134">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56974-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="56974-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="56974-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="56974-136">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="56974-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="56974-137">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56974-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="56974-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="56974-138">-DestinationPortRange</span></span>
<span data-ttu-id="56974-139">Gibt einen Zielport oder Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="56974-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="56974-140">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="56974-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56974-141">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="56974-141">An integer</span></span> 
- <span data-ttu-id="56974-142">Ein Bereich ganzer Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="56974-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="56974-143">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einem Port</span><span class="sxs-lookup"><span data-stu-id="56974-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="56974-144">-Direction</span><span class="sxs-lookup"><span data-stu-id="56974-144">-Direction</span></span>
<span data-ttu-id="56974-145">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="56974-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="56974-146">Die zulässigen Werte für diesen Parameter sind: "Ein- und ausgehend".</span><span class="sxs-lookup"><span data-stu-id="56974-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="56974-147">-Name</span><span class="sxs-lookup"><span data-stu-id="56974-147">-Name</span></span>
<span data-ttu-id="56974-148">Gibt den Namen der Netzwerksicherheitsregelkonfiguration an, die von diesem Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="56974-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="56974-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="56974-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="56974-150">Gibt das **NetworkSecurityGroup-Objekt** an, das die Konfiguration der Netzwerksicherheitsregel enthält, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="56974-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="56974-151">-Priority</span><span class="sxs-lookup"><span data-stu-id="56974-151">-Priority</span></span>
<span data-ttu-id="56974-152">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="56974-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="56974-153">Die zulässigen Werte für diesen Parameter sind:Eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="56974-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="56974-154">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="56974-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="56974-155">Je niedriger die Prioritätsnummer, desto höher die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="56974-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="56974-156">-Protocol</span><span class="sxs-lookup"><span data-stu-id="56974-156">-Protocol</span></span>
<span data-ttu-id="56974-157">Gibt das Netzwerkprotokoll an, auf das eine Regelkonfiguration angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="56974-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="56974-158">Die zulässigen Werte für diesen Parameter sind: --Tcp</span><span class="sxs-lookup"><span data-stu-id="56974-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="56974-159">Udp</span><span class="sxs-lookup"><span data-stu-id="56974-159">Udp</span></span>
- <span data-ttu-id="56974-160">Ein Platzhalterzeichen (\*) für beides</span><span class="sxs-lookup"><span data-stu-id="56974-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="56974-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="56974-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="56974-162">Gibt ein Quelladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="56974-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="56974-163">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="56974-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56974-164">A CIDR</span><span class="sxs-lookup"><span data-stu-id="56974-164">A CIDR</span></span>
- <span data-ttu-id="56974-165">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="56974-165">A source IP range</span></span>
- <span data-ttu-id="56974-166">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einer beliebigen IP-Adresse. Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="56974-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="56974-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="56974-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="56974-168">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="56974-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="56974-169">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56974-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="56974-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="56974-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="56974-171">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="56974-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="56974-172">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56974-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="56974-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="56974-173">-SourcePortRange</span></span>
<span data-ttu-id="56974-174">Gibt den Quellport oder -bereich an.</span><span class="sxs-lookup"><span data-stu-id="56974-174">Specifies the source port or range.</span></span>
<span data-ttu-id="56974-175">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="56974-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56974-176">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="56974-176">An integer</span></span>
- <span data-ttu-id="56974-177">Ein Bereich ganzer Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="56974-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="56974-178">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einem Port</span><span class="sxs-lookup"><span data-stu-id="56974-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="56974-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56974-179">CommonParameters</span></span>
<span data-ttu-id="56974-180">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56974-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56974-181">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56974-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56974-182">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56974-182">INPUTS</span></span>

### <span data-ttu-id="56974-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="56974-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="56974-184">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56974-184">OUTPUTS</span></span>

### <span data-ttu-id="56974-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="56974-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="56974-186">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56974-186">NOTES</span></span>

## <span data-ttu-id="56974-187">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56974-187">RELATED LINKS</span></span>

[<span data-ttu-id="56974-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56974-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="56974-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56974-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="56974-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56974-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="56974-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56974-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


