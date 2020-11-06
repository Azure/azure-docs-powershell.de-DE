---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: fa1416d7bd65236d3a4e1198d6f70efb1a860985
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481826"
---
# <span data-ttu-id="07c6b-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07c6b-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="07c6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="07c6b-103">Legt den Zielstatus für eine Netzwerk Sicherheitsregel Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="07c6b-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07c6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07c6b-104">SYNTAX</span></span>

### <span data-ttu-id="07c6b-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="07c6b-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="07c6b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="07c6b-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c6b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07c6b-107">DESCRIPTION</span></span>
<span data-ttu-id="07c6b-108">Das Cmdlet " **Set-AzureRmNetworkSecurityRuleConfig** " legt den Zielstatus für eine Azure Network Security Rule-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="07c6b-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="07c6b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07c6b-109">EXAMPLES</span></span>

### <span data-ttu-id="07c6b-110">Beispiel 1: Ändern der Zugriffskonfiguration in einer Netzwerk Sicherheitsregel</span><span class="sxs-lookup"><span data-stu-id="07c6b-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="07c6b-111">Der erste Befehl ruft die Netzwerksicherheitsgruppe mit dem Namen NSG-Frontend ab und speichert Sie dann in der Variablen $NSG.</span><span class="sxs-lookup"><span data-stu-id="07c6b-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="07c6b-112">Der zweite Befehl verwendet den Pipelineoperator, um die Sicherheitsgruppe in $NSG an Get-AzureRmNetworkSecurityRuleConfig zu übergeben, wodurch die Sicherheitsregel Konfiguration mit dem Namen RDP-Rule abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="07c6b-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="07c6b-113">Der dritte Befehl ändert die Zugriffskonfiguration der RDP-Regel in Deny.</span><span class="sxs-lookup"><span data-stu-id="07c6b-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="07c6b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="07c6b-114">PARAMETERS</span></span>

### <span data-ttu-id="07c6b-115">-Access</span><span class="sxs-lookup"><span data-stu-id="07c6b-115">-Access</span></span>
<span data-ttu-id="07c6b-116">Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="07c6b-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="07c6b-117">Zulässige Werte für diesen Parameter sind: allow und Deny.</span><span class="sxs-lookup"><span data-stu-id="07c6b-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="07c6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c6b-118">-DefaultProfile</span></span>
<span data-ttu-id="07c6b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07c6b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07c6b-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07c6b-120">-Description</span></span>
<span data-ttu-id="07c6b-121">Gibt eine Beschreibung für eine Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="07c6b-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="07c6b-122">Die maximale Größe beträgt 140 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="07c6b-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="07c6b-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="07c6b-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="07c6b-124">Gibt ein Ziel Adresspräfix an.</span><span class="sxs-lookup"><span data-stu-id="07c6b-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="07c6b-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="07c6b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07c6b-126">Eine CIDR-Adresse (classlos InterDomain Routing)</span><span class="sxs-lookup"><span data-stu-id="07c6b-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="07c6b-127">Ein Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="07c6b-127">A destination IP address range</span></span> 
- <span data-ttu-id="07c6b-128">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht</span><span class="sxs-lookup"><span data-stu-id="07c6b-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="07c6b-129">Sie können Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.</span><span class="sxs-lookup"><span data-stu-id="07c6b-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="07c6b-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="07c6b-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="07c6b-131">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="07c6b-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="07c6b-132">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07c6b-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="07c6b-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="07c6b-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="07c6b-134">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="07c6b-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="07c6b-135">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07c6b-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="07c6b-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="07c6b-136">-DestinationPortRange</span></span>
<span data-ttu-id="07c6b-137">Gibt einen Zielport oder einen Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="07c6b-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="07c6b-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="07c6b-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07c6b-139">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="07c6b-139">An integer</span></span> 
- <span data-ttu-id="07c6b-140">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="07c6b-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="07c6b-141">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="07c6b-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="07c6b-142">-Richtung</span><span class="sxs-lookup"><span data-stu-id="07c6b-142">-Direction</span></span>
<span data-ttu-id="07c6b-143">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="07c6b-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="07c6b-144">Die zulässigen Werte für diesen Parameter lauten: ein-und ausgehende.</span><span class="sxs-lookup"><span data-stu-id="07c6b-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="07c6b-145">-Name</span><span class="sxs-lookup"><span data-stu-id="07c6b-145">-Name</span></span>
<span data-ttu-id="07c6b-146">Gibt den Namen der Netzwerk Sicherheitsregel Konfiguration an, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="07c6b-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="07c6b-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="07c6b-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="07c6b-148">Gibt das **NetworkSecurityGroup** -Objekt an, das die festzulegende Netzwerk Sicherheitsregel Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="07c6b-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="07c6b-149">-Priorität</span><span class="sxs-lookup"><span data-stu-id="07c6b-149">-Priority</span></span>
<span data-ttu-id="07c6b-150">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="07c6b-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="07c6b-151">Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="07c6b-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="07c6b-152">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="07c6b-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="07c6b-153">Je niedriger die Prioritätszahl ist, desto höher ist die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="07c6b-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="07c6b-154">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="07c6b-154">-Protocol</span></span>
<span data-ttu-id="07c6b-155">Gibt das Netzwerkprotokoll an, für das eine Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="07c6b-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="07c6b-156">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="07c6b-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="07c6b-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="07c6b-157">--Tcp</span></span>
- <span data-ttu-id="07c6b-158">UDP</span><span class="sxs-lookup"><span data-stu-id="07c6b-158">Udp</span></span>
- <span data-ttu-id="07c6b-159">Ein Platzhalterzeichen (\*), das mit beiden übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="07c6b-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="07c6b-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="07c6b-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="07c6b-161">Gibt das Präfix einer Quelladresse an.</span><span class="sxs-lookup"><span data-stu-id="07c6b-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="07c6b-162">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="07c6b-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07c6b-163">ein CIDR</span><span class="sxs-lookup"><span data-stu-id="07c6b-163">A CIDR</span></span>
- <span data-ttu-id="07c6b-164">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="07c6b-164">A source IP range</span></span>
- <span data-ttu-id="07c6b-165">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht</span><span class="sxs-lookup"><span data-stu-id="07c6b-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="07c6b-166">Sie können auch Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.</span><span class="sxs-lookup"><span data-stu-id="07c6b-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="07c6b-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="07c6b-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="07c6b-168">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="07c6b-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="07c6b-169">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07c6b-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="07c6b-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="07c6b-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="07c6b-171">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="07c6b-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="07c6b-172">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07c6b-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="07c6b-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="07c6b-173">-SourcePortRange</span></span>
<span data-ttu-id="07c6b-174">Gibt den Quell Port oder-Bereich an.</span><span class="sxs-lookup"><span data-stu-id="07c6b-174">Specifies the source port or range.</span></span>
<span data-ttu-id="07c6b-175">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="07c6b-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07c6b-176">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="07c6b-176">An integer</span></span>
- <span data-ttu-id="07c6b-177">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="07c6b-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="07c6b-178">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="07c6b-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="07c6b-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c6b-179">CommonParameters</span></span>
<span data-ttu-id="07c6b-180">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c6b-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c6b-181">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07c6b-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c6b-182">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07c6b-182">INPUTS</span></span>

### <span data-ttu-id="07c6b-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="07c6b-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="07c6b-184">Der Parameter "NetworkSecurityGroup" akzeptiert den Wert vom Typ "PSNetworkSecurityGroup" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="07c6b-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="07c6b-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07c6b-185">OUTPUTS</span></span>

### <span data-ttu-id="07c6b-186">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="07c6b-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="07c6b-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="07c6b-187">NOTES</span></span>

## <span data-ttu-id="07c6b-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07c6b-188">RELATED LINKS</span></span>

[<span data-ttu-id="07c6b-189">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07c6b-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="07c6b-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07c6b-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="07c6b-191">Neu – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07c6b-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="07c6b-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07c6b-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


