---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176942"
---
# <span data-ttu-id="4ce81-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ce81-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="4ce81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ce81-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce81-103">Aktualisiert eine Netzwerk Sicherheitsregel-Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4ce81-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="4ce81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ce81-104">SYNTAX</span></span>

### <span data-ttu-id="4ce81-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ce81-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ce81-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce81-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ce81-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ce81-107">DESCRIPTION</span></span>
<span data-ttu-id="4ce81-108">Das Cmdlet " **Satz-AzNetworkSecurityRuleConfig** " aktualisiert eine Netzwerk Sicherheitsregel-Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4ce81-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="4ce81-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ce81-109">EXAMPLES</span></span>

### <span data-ttu-id="4ce81-110">Beispiel 1: Ändern der Zugriffskonfiguration in einer Netzwerk Sicherheitsregel</span><span class="sxs-lookup"><span data-stu-id="4ce81-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="4ce81-111">Der erste Befehl ruft die Netzwerksicherheitsgruppe mit dem Namen NSG-Frontend ab und speichert Sie dann in der Variablen $NSG.</span><span class="sxs-lookup"><span data-stu-id="4ce81-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="4ce81-112">Der zweite Befehl verwendet den Pipelineoperator, um die Sicherheitsgruppe in $NSG an Get-AzNetworkSecurityRuleConfig zu übergeben, wodurch die Sicherheitsregel Konfiguration mit dem Namen RDP-Rule abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4ce81-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="4ce81-113">Der dritte Befehl ändert die Zugriffskonfiguration der RDP-Regel in Deny.</span><span class="sxs-lookup"><span data-stu-id="4ce81-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="4ce81-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ce81-114">Example 2</span></span>

<span data-ttu-id="4ce81-115">Aktualisiert eine Netzwerk Sicherheitsregel-Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4ce81-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="4ce81-116">automatisch</span><span class="sxs-lookup"><span data-stu-id="4ce81-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="4ce81-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ce81-117">PARAMETERS</span></span>

### <span data-ttu-id="4ce81-118">-Access</span><span class="sxs-lookup"><span data-stu-id="4ce81-118">-Access</span></span>
<span data-ttu-id="4ce81-119">Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="4ce81-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="4ce81-120">Zulässige Werte für diesen Parameter sind: allow und Deny.</span><span class="sxs-lookup"><span data-stu-id="4ce81-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="4ce81-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce81-121">-DefaultProfile</span></span>
<span data-ttu-id="4ce81-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ce81-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ce81-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ce81-123">-Description</span></span>
<span data-ttu-id="4ce81-124">Gibt eine Beschreibung für eine Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="4ce81-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="4ce81-125">Die maximale Größe beträgt 140 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4ce81-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="4ce81-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4ce81-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="4ce81-127">Gibt ein Ziel Adresspräfix an.</span><span class="sxs-lookup"><span data-stu-id="4ce81-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="4ce81-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4ce81-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ce81-129">Eine CIDR-Adresse (classlos InterDomain Routing)</span><span class="sxs-lookup"><span data-stu-id="4ce81-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="4ce81-130">Ein Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="4ce81-130">A destination IP address range</span></span> 
- <span data-ttu-id="4ce81-131">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht, die Sie mit Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4ce81-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="4ce81-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ce81-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="4ce81-133">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ce81-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="4ce81-134">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce81-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4ce81-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4ce81-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="4ce81-136">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ce81-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="4ce81-137">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce81-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4ce81-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="4ce81-138">-DestinationPortRange</span></span>
<span data-ttu-id="4ce81-139">Gibt einen Zielport oder einen Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="4ce81-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="4ce81-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4ce81-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ce81-141">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="4ce81-141">An integer</span></span> 
- <span data-ttu-id="4ce81-142">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="4ce81-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="4ce81-143">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="4ce81-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="4ce81-144">-Richtung</span><span class="sxs-lookup"><span data-stu-id="4ce81-144">-Direction</span></span>
<span data-ttu-id="4ce81-145">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="4ce81-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="4ce81-146">Die zulässigen Werte für diesen Parameter lauten: ein-und ausgehende.</span><span class="sxs-lookup"><span data-stu-id="4ce81-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="4ce81-147">-Name</span><span class="sxs-lookup"><span data-stu-id="4ce81-147">-Name</span></span>
<span data-ttu-id="4ce81-148">Gibt den Namen der Netzwerk Sicherheitsregel Konfiguration an, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="4ce81-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4ce81-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ce81-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4ce81-150">Gibt das **NetworkSecurityGroup** -Objekt an, das die festzulegende Netzwerk Sicherheitsregel Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="4ce81-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="4ce81-151">-Priorität</span><span class="sxs-lookup"><span data-stu-id="4ce81-151">-Priority</span></span>
<span data-ttu-id="4ce81-152">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="4ce81-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="4ce81-153">Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="4ce81-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="4ce81-154">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="4ce81-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="4ce81-155">Je niedriger die Prioritätszahl ist, desto höher ist die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="4ce81-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="4ce81-156">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4ce81-156">-Protocol</span></span>
<span data-ttu-id="4ce81-157">Gibt das Netzwerkprotokoll an, für das eine Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="4ce81-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="4ce81-158">Die akzeptablen Werte für diesen Parameter sind:--TCP</span><span class="sxs-lookup"><span data-stu-id="4ce81-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="4ce81-159">UDP</span><span class="sxs-lookup"><span data-stu-id="4ce81-159">Udp</span></span>
- <span data-ttu-id="4ce81-160">Ein Platzhalterzeichen (\*), das mit beiden übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="4ce81-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="4ce81-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4ce81-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="4ce81-162">Gibt das Präfix einer Quelladresse an.</span><span class="sxs-lookup"><span data-stu-id="4ce81-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="4ce81-163">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4ce81-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ce81-164">ein CIDR</span><span class="sxs-lookup"><span data-stu-id="4ce81-164">A CIDR</span></span>
- <span data-ttu-id="4ce81-165">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="4ce81-165">A source IP range</span></span>
- <span data-ttu-id="4ce81-166">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ce81-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="4ce81-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ce81-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="4ce81-168">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ce81-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="4ce81-169">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce81-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4ce81-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4ce81-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="4ce81-171">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ce81-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="4ce81-172">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce81-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4ce81-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="4ce81-173">-SourcePortRange</span></span>
<span data-ttu-id="4ce81-174">Gibt den Quell Port oder-Bereich an.</span><span class="sxs-lookup"><span data-stu-id="4ce81-174">Specifies the source port or range.</span></span>
<span data-ttu-id="4ce81-175">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4ce81-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ce81-176">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="4ce81-176">An integer</span></span>
- <span data-ttu-id="4ce81-177">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="4ce81-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="4ce81-178">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="4ce81-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="4ce81-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce81-179">CommonParameters</span></span>
<span data-ttu-id="4ce81-180">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce81-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce81-181">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce81-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce81-182">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ce81-182">INPUTS</span></span>

### <span data-ttu-id="4ce81-183">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ce81-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4ce81-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ce81-184">OUTPUTS</span></span>

### <span data-ttu-id="4ce81-185">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ce81-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4ce81-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ce81-186">NOTES</span></span>

## <span data-ttu-id="4ce81-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ce81-187">RELATED LINKS</span></span>

[<span data-ttu-id="4ce81-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ce81-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4ce81-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ce81-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4ce81-190">Neu – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ce81-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4ce81-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ce81-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


