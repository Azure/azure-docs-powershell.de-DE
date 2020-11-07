---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: b2b1667a9326a9c25d78639e397146c0dd85dc5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841800"
---
# <span data-ttu-id="92782-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92782-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="92782-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92782-102">SYNOPSIS</span></span>
<span data-ttu-id="92782-103">Fügt eine Netzwerk Sicherheitsregel-Konfiguration zu einer Netzwerksicherheitsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="92782-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="92782-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92782-104">SYNTAX</span></span>

### <span data-ttu-id="92782-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="92782-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92782-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="92782-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92782-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92782-107">DESCRIPTION</span></span>
<span data-ttu-id="92782-108">Mit dem Cmdlet **Add-AzNetworkSecurityRuleConfig** wird eine Netzwerk Sicherheitsregel-Konfiguration zu einer Azure Network Security-Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="92782-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="92782-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92782-109">EXAMPLES</span></span>

### <span data-ttu-id="92782-110">1: Hinzufügen einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="92782-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="92782-111">Der erste Befehl ruft eine Azure Network Security-Gruppe mit dem Namen "nsg1" aus der Ressourcengruppe "RG1" ab.</span><span class="sxs-lookup"><span data-stu-id="92782-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="92782-112">Der zweite Befehl fügt eine Netzwerk Sicherheitsregel mit dem Namen "RDP-Regel" hinzu, die den Datenverkehr vom Internet auf Port 3389 zum abgerufenen Netzwerk Sicherheitsgruppenobjekt ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="92782-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="92782-113">Behält die geänderte Azure Network Security-Gruppe bei.</span><span class="sxs-lookup"><span data-stu-id="92782-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="92782-114">1: Hinzufügen einer neuen Sicherheitsregel mit Anwendungs Sicherheitsgruppen</span><span class="sxs-lookup"><span data-stu-id="92782-114">1: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="92782-115">Zunächst erstellen wir zwei neue Anwendungs Sicherheitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="92782-115">First, we create two new application security groups.</span></span> <span data-ttu-id="92782-116">Anschließend rufen wir eine Azure Network Security-Gruppe mit dem Namen "nsg1" aus der Ressourcengruppe "RG1" ab.</span><span class="sxs-lookup"><span data-stu-id="92782-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="92782-117">und fügen Sie eine Netzwerk Sicherheitsregel mit dem Namen "RDP-Regel" hinzu.</span><span class="sxs-lookup"><span data-stu-id="92782-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="92782-118">Die Regel ermöglicht den Datenverkehr von allen IP-Konfigurationen in der Anwendungs Sicherheitsgruppe "srcAsg" zu allen IP-Konfigurationen in "destAsg" auf Port 3389.</span><span class="sxs-lookup"><span data-stu-id="92782-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="92782-119">Nach dem Hinzufügen der Regel behalten wir die geänderte Azure Network Security-Gruppe bei.</span><span class="sxs-lookup"><span data-stu-id="92782-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="92782-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="92782-120">PARAMETERS</span></span>

### <span data-ttu-id="92782-121">-Access</span><span class="sxs-lookup"><span data-stu-id="92782-121">-Access</span></span>
<span data-ttu-id="92782-122">Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="92782-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="92782-123">Zulässige Werte für diesen Parameter sind: allow und Deny.</span><span class="sxs-lookup"><span data-stu-id="92782-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="92782-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92782-124">-DefaultProfile</span></span>
<span data-ttu-id="92782-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92782-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92782-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92782-126">-Description</span></span>
<span data-ttu-id="92782-127">Gibt eine Beschreibung der Konfiguration einer Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="92782-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="92782-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="92782-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="92782-129">Gibt ein Ziel Adresspräfix an.</span><span class="sxs-lookup"><span data-stu-id="92782-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="92782-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="92782-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="92782-131">Eine CIDR-Adresse (classlos InterDomain Routing)</span><span class="sxs-lookup"><span data-stu-id="92782-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="92782-132">Ein Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="92782-132">A destination IP address range</span></span>
- <span data-ttu-id="92782-133">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht</span><span class="sxs-lookup"><span data-stu-id="92782-133">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="92782-134">Sie können Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.</span><span class="sxs-lookup"><span data-stu-id="92782-134">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="92782-135">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92782-135">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="92782-136">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="92782-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="92782-137">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92782-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="92782-138">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="92782-138">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="92782-139">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="92782-139">The application security group set as destination for the rule.</span></span> <span data-ttu-id="92782-140">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92782-140">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="92782-141">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="92782-141">-DestinationPortRange</span></span>
<span data-ttu-id="92782-142">Gibt einen Zielport oder einen Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="92782-142">Specifies a destination port or range.</span></span>
<span data-ttu-id="92782-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="92782-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="92782-144">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="92782-144">An integer</span></span>
- <span data-ttu-id="92782-145">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="92782-145">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="92782-146">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="92782-146">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="92782-147">-Richtung</span><span class="sxs-lookup"><span data-stu-id="92782-147">-Direction</span></span>
<span data-ttu-id="92782-148">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="92782-148">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="92782-149">Die zulässigen Werte für diesen Parameter lauten: ein-und ausgehende.</span><span class="sxs-lookup"><span data-stu-id="92782-149">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="92782-150">-Name</span><span class="sxs-lookup"><span data-stu-id="92782-150">-Name</span></span>
<span data-ttu-id="92782-151">Gibt den Namen einer Netzwerk Sicherheitsregel Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="92782-151">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="92782-152">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92782-152">-NetworkSecurityGroup</span></span>
<span data-ttu-id="92782-153">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="92782-153">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="92782-154">Dieses Cmdlet fügt dem Objekt, das dieser Parameter angibt, eine Konfiguration für die Netzwerk Sicherheitsregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="92782-154">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92782-155">-Priorität</span><span class="sxs-lookup"><span data-stu-id="92782-155">-Priority</span></span>
<span data-ttu-id="92782-156">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="92782-156">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="92782-157">Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="92782-157">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="92782-158">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="92782-158">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="92782-159">Je niedriger die Prioritätszahl ist, desto höher ist die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="92782-159">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="92782-160">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="92782-160">-Protocol</span></span>
<span data-ttu-id="92782-161">Gibt das Netzwerkprotokoll an, für das eine Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="92782-161">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="92782-162">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="92782-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="92782-163">TCP</span><span class="sxs-lookup"><span data-stu-id="92782-163">Tcp</span></span>
- <span data-ttu-id="92782-164">UDP</span><span class="sxs-lookup"><span data-stu-id="92782-164">Udp</span></span>
- <span data-ttu-id="92782-165">Platzhalterzeichen (\*) zur Übereinstimmung mit beiden</span><span class="sxs-lookup"><span data-stu-id="92782-165">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="92782-166">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="92782-166">-SourceAddressPrefix</span></span>
<span data-ttu-id="92782-167">Gibt das Präfix einer Quelladresse an.</span><span class="sxs-lookup"><span data-stu-id="92782-167">Specifies a source address prefix.</span></span>
<span data-ttu-id="92782-168">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="92782-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="92782-169">ein CIDR</span><span class="sxs-lookup"><span data-stu-id="92782-169">A CIDR</span></span>
- <span data-ttu-id="92782-170">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="92782-170">A source IP range</span></span>
- <span data-ttu-id="92782-171">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="92782-171">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="92782-172">Sie können auch Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.</span><span class="sxs-lookup"><span data-stu-id="92782-172">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="92782-173">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92782-173">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="92782-174">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="92782-174">The application security group set as source for the rule.</span></span> <span data-ttu-id="92782-175">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92782-175">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="92782-176">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="92782-176">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="92782-177">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="92782-177">The application security group set as source for the rule.</span></span> <span data-ttu-id="92782-178">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92782-178">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="92782-179">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="92782-179">-SourcePortRange</span></span>
<span data-ttu-id="92782-180">Gibt einen Quell Port oder-Bereich an.</span><span class="sxs-lookup"><span data-stu-id="92782-180">Specifies a source port or range.</span></span>
<span data-ttu-id="92782-181">Dieser Wert wird als ganze Zahl ausgedrückt, als ein Bereich zwischen 0 und 65535, oder als Platzhalterzeichen (\*), um einem beliebigen Quell-Port zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="92782-181">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="92782-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92782-182">CommonParameters</span></span>
<span data-ttu-id="92782-183">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92782-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92782-184">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92782-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92782-185">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92782-185">INPUTS</span></span>

### <span data-ttu-id="92782-186">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92782-186">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="92782-187">Der Parameter "NetworkSecurityGroup" akzeptiert den Wert vom Typ "PSNetworkSecurityGroup" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="92782-187">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="92782-188">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92782-188">OUTPUTS</span></span>

### <span data-ttu-id="92782-189">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92782-189">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="92782-190">Notizen</span><span class="sxs-lookup"><span data-stu-id="92782-190">NOTES</span></span>

## <span data-ttu-id="92782-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92782-191">RELATED LINKS</span></span>

[<span data-ttu-id="92782-192">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92782-192">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="92782-193">Neu – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92782-193">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="92782-194">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92782-194">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="92782-195">Satz-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92782-195">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


