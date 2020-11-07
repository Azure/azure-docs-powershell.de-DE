---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3e11b1ca7b83a4f01ce2d344874f4da02b399221
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660903"
---
# <span data-ttu-id="ed374-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed374-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="ed374-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed374-102">SYNOPSIS</span></span>
<span data-ttu-id="ed374-103">Fügt eine Netzwerk Sicherheitsregel-Konfiguration zu einer Netzwerksicherheitsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed374-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="ed374-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed374-104">SYNTAX</span></span>

### <span data-ttu-id="ed374-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed374-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed374-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed374-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed374-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed374-107">DESCRIPTION</span></span>
<span data-ttu-id="ed374-108">Mit dem Cmdlet **Add-AzNetworkSecurityRuleConfig** wird eine Netzwerk Sicherheitsregel-Konfiguration zu einer Azure Network Security-Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ed374-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="ed374-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed374-109">EXAMPLES</span></span>

### <span data-ttu-id="ed374-110">1: Hinzufügen einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="ed374-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="ed374-111">Der erste Befehl ruft eine Azure Network Security-Gruppe mit dem Namen "nsg1" aus der Ressourcengruppe "RG1" ab.</span><span class="sxs-lookup"><span data-stu-id="ed374-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="ed374-112">Der zweite Befehl fügt eine Netzwerk Sicherheitsregel mit dem Namen "RDP-Regel" hinzu, die den Datenverkehr vom Internet auf Port 3389 zum abgerufenen Netzwerk Sicherheitsgruppenobjekt ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ed374-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="ed374-113">Behält die geänderte Azure Network Security-Gruppe bei.</span><span class="sxs-lookup"><span data-stu-id="ed374-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="ed374-114">2: Hinzufügen einer neuen Sicherheitsregel mit Anwendungs Sicherheitsgruppen</span><span class="sxs-lookup"><span data-stu-id="ed374-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="ed374-115">Zunächst erstellen wir zwei neue Anwendungs Sicherheitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="ed374-115">First, we create two new application security groups.</span></span> <span data-ttu-id="ed374-116">Anschließend rufen wir eine Azure Network Security-Gruppe mit dem Namen "nsg1" aus der Ressourcengruppe "RG1" ab.</span><span class="sxs-lookup"><span data-stu-id="ed374-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="ed374-117">und fügen Sie eine Netzwerk Sicherheitsregel mit dem Namen "RDP-Regel" hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed374-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="ed374-118">Die Regel ermöglicht den Datenverkehr von allen IP-Konfigurationen in der Anwendungs Sicherheitsgruppe "srcAsg" zu allen IP-Konfigurationen in "destAsg" auf Port 3389.</span><span class="sxs-lookup"><span data-stu-id="ed374-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="ed374-119">Nach dem Hinzufügen der Regel behalten wir die geänderte Azure Network Security-Gruppe bei.</span><span class="sxs-lookup"><span data-stu-id="ed374-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="ed374-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed374-120">PARAMETERS</span></span>

### <span data-ttu-id="ed374-121">-Access</span><span class="sxs-lookup"><span data-stu-id="ed374-121">-Access</span></span>
<span data-ttu-id="ed374-122">Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="ed374-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="ed374-123">Zulässige Werte für diesen Parameter sind: allow und Deny.</span><span class="sxs-lookup"><span data-stu-id="ed374-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="ed374-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed374-124">-DefaultProfile</span></span>
<span data-ttu-id="ed374-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed374-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed374-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed374-126">-Description</span></span>
<span data-ttu-id="ed374-127">Gibt eine Beschreibung der Konfiguration einer Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="ed374-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="ed374-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ed374-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="ed374-129">Gibt ein Ziel Adresspräfix an.</span><span class="sxs-lookup"><span data-stu-id="ed374-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="ed374-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ed374-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed374-131">Eine CIDR-Adresse (classlos InterDomain Routing)</span><span class="sxs-lookup"><span data-stu-id="ed374-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="ed374-132">Ein Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="ed374-132">A destination IP address range</span></span>
- <span data-ttu-id="ed374-133">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht, die Sie mit Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ed374-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="ed374-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed374-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="ed374-135">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed374-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="ed374-136">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed374-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ed374-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ed374-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="ed374-138">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed374-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="ed374-139">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed374-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ed374-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="ed374-140">-DestinationPortRange</span></span>
<span data-ttu-id="ed374-141">Gibt einen Zielport oder einen Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="ed374-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="ed374-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ed374-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed374-143">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="ed374-143">An integer</span></span>
- <span data-ttu-id="ed374-144">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="ed374-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="ed374-145">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="ed374-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="ed374-146">-Richtung</span><span class="sxs-lookup"><span data-stu-id="ed374-146">-Direction</span></span>
<span data-ttu-id="ed374-147">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="ed374-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="ed374-148">Die zulässigen Werte für diesen Parameter lauten: ein-und ausgehende.</span><span class="sxs-lookup"><span data-stu-id="ed374-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="ed374-149">-Name</span><span class="sxs-lookup"><span data-stu-id="ed374-149">-Name</span></span>
<span data-ttu-id="ed374-150">Gibt den Namen einer Netzwerk Sicherheitsregel Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ed374-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="ed374-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed374-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ed374-152">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ed374-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="ed374-153">Dieses Cmdlet fügt dem Objekt, das dieser Parameter angibt, eine Konfiguration für die Netzwerk Sicherheitsregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed374-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed374-154">-Priorität</span><span class="sxs-lookup"><span data-stu-id="ed374-154">-Priority</span></span>
<span data-ttu-id="ed374-155">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ed374-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="ed374-156">Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="ed374-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="ed374-157">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ed374-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="ed374-158">Je niedriger die Prioritätszahl ist, desto höher ist die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="ed374-158">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="ed374-159">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ed374-159">-Protocol</span></span>
<span data-ttu-id="ed374-160">Gibt das Netzwerkprotokoll an, für das eine Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="ed374-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="ed374-161">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ed374-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed374-162">TCP</span><span class="sxs-lookup"><span data-stu-id="ed374-162">Tcp</span></span>
- <span data-ttu-id="ed374-163">UDP</span><span class="sxs-lookup"><span data-stu-id="ed374-163">Udp</span></span>
- <span data-ttu-id="ed374-164">Platzhalterzeichen (\*) zur Übereinstimmung mit beiden</span><span class="sxs-lookup"><span data-stu-id="ed374-164">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="ed374-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ed374-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="ed374-166">Gibt das Präfix einer Quelladresse an.</span><span class="sxs-lookup"><span data-stu-id="ed374-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="ed374-167">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ed374-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed374-168">ein CIDR</span><span class="sxs-lookup"><span data-stu-id="ed374-168">A CIDR</span></span>
- <span data-ttu-id="ed374-169">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="ed374-169">A source IP range</span></span>
- <span data-ttu-id="ed374-170">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="ed374-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="ed374-171">Sie können auch Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed374-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="ed374-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed374-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="ed374-173">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed374-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="ed374-174">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed374-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ed374-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ed374-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="ed374-176">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed374-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="ed374-177">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed374-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ed374-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="ed374-178">-SourcePortRange</span></span>
<span data-ttu-id="ed374-179">Gibt einen Quell Port oder-Bereich an.</span><span class="sxs-lookup"><span data-stu-id="ed374-179">Specifies a source port or range.</span></span>
<span data-ttu-id="ed374-180">Dieser Wert wird als ganze Zahl ausgedrückt, als ein Bereich zwischen 0 und 65535, oder als Platzhalterzeichen (\*), um einem beliebigen Quell-Port zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ed374-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="ed374-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed374-181">CommonParameters</span></span>
<span data-ttu-id="ed374-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed374-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed374-183">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed374-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed374-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed374-184">INPUTS</span></span>

### <span data-ttu-id="ed374-185">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed374-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ed374-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed374-186">OUTPUTS</span></span>

### <span data-ttu-id="ed374-187">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed374-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ed374-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed374-188">NOTES</span></span>

## <span data-ttu-id="ed374-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed374-189">RELATED LINKS</span></span>

[<span data-ttu-id="ed374-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed374-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ed374-191">Neu – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed374-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ed374-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed374-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ed374-193">Satz-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed374-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


