---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944813"
---
# <span data-ttu-id="5e25c-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e25c-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="5e25c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e25c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e25c-103">Aktualisiert eine Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5e25c-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="5e25c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e25c-104">SYNTAX</span></span>

### <span data-ttu-id="5e25c-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e25c-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e25c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e25c-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e25c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e25c-107">DESCRIPTION</span></span>
<span data-ttu-id="5e25c-108">Das **Cmdlet Set-AzNetworkSecurityRuleConfig** aktualisiert eine Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5e25c-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="5e25c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e25c-109">EXAMPLES</span></span>

### <span data-ttu-id="5e25c-110">Beispiel 1: Ändern der Zugriffskonfiguration in einer Netzwerksicherheitsregel</span><span class="sxs-lookup"><span data-stu-id="5e25c-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="5e25c-111">Der erste Befehl ruft die Netzwerksicherheitsgruppe NSG-FrontEnd ab und speichert sie dann in der variablen $nsg.</span><span class="sxs-lookup"><span data-stu-id="5e25c-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="5e25c-112">Der zweite Befehl verwendet den Pipelineoperator, um die Sicherheitsgruppe in $nsg an Get-AzNetworkSecurityRuleConfig zu übergeben, die die Sicherheitsregelkonfiguration namens rdp-rule erhält.</span><span class="sxs-lookup"><span data-stu-id="5e25c-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="5e25c-113">Mit dem dritten Befehl wird die Zugriffskonfiguration von rdp-rule in "Verweigern" geändert.</span><span class="sxs-lookup"><span data-stu-id="5e25c-113">The third command changes the access configuration of rdp-rule to Deny.</span></span> <span data-ttu-id="5e25c-114">Dadurch wird die Regel jedoch überschrieben und nur die Parameter festgelegt, die an die Funktion Set-AzNetworkSecurityRuleConfig werden.</span><span class="sxs-lookup"><span data-stu-id="5e25c-114">However, this overwrites the rule and only sets the parameters that are passed to the Set-AzNetworkSecurityRuleConfig function.</span></span>   <span data-ttu-id="5e25c-115">HINWEIS: Es gibt keine Möglichkeit, ein einzelnes Attribut zu ändern</span><span class="sxs-lookup"><span data-stu-id="5e25c-115">NOTE: There is no way to change a single attribute</span></span>

### <span data-ttu-id="5e25c-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5e25c-116">Example 2</span></span>

<span data-ttu-id="5e25c-117">Aktualisiert eine Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5e25c-117">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="5e25c-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="5e25c-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="5e25c-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e25c-119">PARAMETERS</span></span>

### <span data-ttu-id="5e25c-120">-Access</span><span class="sxs-lookup"><span data-stu-id="5e25c-120">-Access</span></span>
<span data-ttu-id="5e25c-121">Gibt an, ob Netzwerkdatenverkehr zulässig oder verweigert ist.</span><span class="sxs-lookup"><span data-stu-id="5e25c-121">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="5e25c-122">Die zulässigen Werte für diesen Parameter sind: Zulassen und Verweigern.</span><span class="sxs-lookup"><span data-stu-id="5e25c-122">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="5e25c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e25c-123">-DefaultProfile</span></span>
<span data-ttu-id="5e25c-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e25c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e25c-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e25c-125">-Description</span></span>
<span data-ttu-id="5e25c-126">Gibt eine Beschreibung für eine Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5e25c-126">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="5e25c-127">Die maximale Größe beträgt 140 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5e25c-127">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="5e25c-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5e25c-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="5e25c-129">Gibt ein Zieladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="5e25c-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="5e25c-130">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5e25c-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e25c-131">Eine klassenloses domänenübergreifendes Routing (CIDR)</span><span class="sxs-lookup"><span data-stu-id="5e25c-131">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="5e25c-132">Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="5e25c-132">A destination IP address range</span></span> 
- <span data-ttu-id="5e25c-133">Platzhalterzeichen (\*) zur Übereinstimmung mit einer beliebigen IP-Adresse Sie können Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e25c-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="5e25c-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e25c-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="5e25c-135">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5e25c-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="5e25c-136">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e25c-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5e25c-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5e25c-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="5e25c-138">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5e25c-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="5e25c-139">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e25c-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5e25c-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="5e25c-140">-DestinationPortRange</span></span>
<span data-ttu-id="5e25c-141">Gibt einen Zielport oder -bereich an.</span><span class="sxs-lookup"><span data-stu-id="5e25c-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="5e25c-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5e25c-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e25c-143">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="5e25c-143">An integer</span></span> 
- <span data-ttu-id="5e25c-144">Ein Ganzzahlbereich zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="5e25c-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="5e25c-145">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einem beliebigen Port</span><span class="sxs-lookup"><span data-stu-id="5e25c-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="5e25c-146">-Richtung</span><span class="sxs-lookup"><span data-stu-id="5e25c-146">-Direction</span></span>
<span data-ttu-id="5e25c-147">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="5e25c-147">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="5e25c-148">Die zulässigen Werte für diesen Parameter sind: Ein- und Ausgehend.</span><span class="sxs-lookup"><span data-stu-id="5e25c-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="5e25c-149">-Name</span><span class="sxs-lookup"><span data-stu-id="5e25c-149">-Name</span></span>
<span data-ttu-id="5e25c-150">Gibt den Namen der Netzwerksicherheitsregelkonfiguration an, die von diesem Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5e25c-150">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="5e25c-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e25c-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5e25c-152">Gibt das **NetworkSecurityGroup-Objekt** an, das die netzwerksicherheitsregelkonfiguration enthält, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e25c-152">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="5e25c-153">-Priorität</span><span class="sxs-lookup"><span data-stu-id="5e25c-153">-Priority</span></span>
<span data-ttu-id="5e25c-154">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5e25c-154">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="5e25c-155">Die zulässigen Werte für diesen Parameter sind:Eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="5e25c-155">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="5e25c-156">Die Prioritätsnummer muss für jede Regel in der Auflistung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="5e25c-156">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="5e25c-157">Je niedriger die Prioritätsnummer, desto höher die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="5e25c-157">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="5e25c-158">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5e25c-158">-Protocol</span></span>
<span data-ttu-id="5e25c-159">Gibt das Netzwerkprotokoll an, für das eine Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="5e25c-159">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="5e25c-160">Die zulässigen Werte für diesen Parameter sind: --Tcp</span><span class="sxs-lookup"><span data-stu-id="5e25c-160">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="5e25c-161">Udp</span><span class="sxs-lookup"><span data-stu-id="5e25c-161">Udp</span></span>
- <span data-ttu-id="5e25c-162">Ein Platzhalterzeichen (\*) für beides</span><span class="sxs-lookup"><span data-stu-id="5e25c-162">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="5e25c-163">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5e25c-163">-SourceAddressPrefix</span></span>
<span data-ttu-id="5e25c-164">Gibt ein Quelladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="5e25c-164">Specifies a source address prefix.</span></span>
<span data-ttu-id="5e25c-165">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5e25c-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e25c-166">A CIDR</span><span class="sxs-lookup"><span data-stu-id="5e25c-166">A CIDR</span></span>
- <span data-ttu-id="5e25c-167">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="5e25c-167">A source IP range</span></span>
- <span data-ttu-id="5e25c-168">Platzhalterzeichen (\*) zur Übereinstimmung mit einer beliebigen IP-Adresse Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e25c-168">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="5e25c-169">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e25c-169">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="5e25c-170">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5e25c-170">The application security group set as source for the rule.</span></span> <span data-ttu-id="5e25c-171">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e25c-171">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5e25c-172">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5e25c-172">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="5e25c-173">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5e25c-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="5e25c-174">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e25c-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5e25c-175">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="5e25c-175">-SourcePortRange</span></span>
<span data-ttu-id="5e25c-176">Gibt den Quellport oder -bereich an.</span><span class="sxs-lookup"><span data-stu-id="5e25c-176">Specifies the source port or range.</span></span>
<span data-ttu-id="5e25c-177">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5e25c-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e25c-178">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="5e25c-178">An integer</span></span>
- <span data-ttu-id="5e25c-179">Ein Ganzzahlbereich zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="5e25c-179">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="5e25c-180">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einem beliebigen Port</span><span class="sxs-lookup"><span data-stu-id="5e25c-180">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="5e25c-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e25c-181">CommonParameters</span></span>
<span data-ttu-id="5e25c-182">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e25c-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e25c-183">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e25c-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e25c-184">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e25c-184">INPUTS</span></span>

### <span data-ttu-id="5e25c-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e25c-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5e25c-186">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e25c-186">OUTPUTS</span></span>

### <span data-ttu-id="5e25c-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e25c-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5e25c-188">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5e25c-188">NOTES</span></span>

## <span data-ttu-id="5e25c-189">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5e25c-189">RELATED LINKS</span></span>

[<span data-ttu-id="5e25c-190">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e25c-190">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5e25c-191">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e25c-191">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5e25c-192">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e25c-192">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5e25c-193">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5e25c-193">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


