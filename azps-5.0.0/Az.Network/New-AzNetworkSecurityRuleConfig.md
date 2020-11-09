---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301479"
---
# <span data-ttu-id="018f7-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="018f7-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="018f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="018f7-102">SYNOPSIS</span></span>
<span data-ttu-id="018f7-103">Erstellt eine Netzwerk Sicherheitsregel-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="018f7-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="018f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="018f7-104">SYNTAX</span></span>

### <span data-ttu-id="018f7-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="018f7-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="018f7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="018f7-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="018f7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="018f7-107">DESCRIPTION</span></span>
<span data-ttu-id="018f7-108">Das Cmdlet **New-AzNetworkSecurityRuleConfig** erstellt eine Azure Network Security Rule-Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="018f7-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="018f7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="018f7-109">EXAMPLES</span></span>

### <span data-ttu-id="018f7-110">Beispiel 1: Erstellen einer Netzwerk Sicherheitsregel zum Zulassen von RDP</span><span class="sxs-lookup"><span data-stu-id="018f7-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="018f7-111">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff aus dem Internet auf Port 3389 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="018f7-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="018f7-112">Beispiel 2: Erstellen einer Netzwerk Sicherheitsregel, die http zulässt</span><span class="sxs-lookup"><span data-stu-id="018f7-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="018f7-113">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff aus dem Internet auf Port 80 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="018f7-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="018f7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="018f7-114">PARAMETERS</span></span>

### <span data-ttu-id="018f7-115">-Access</span><span class="sxs-lookup"><span data-stu-id="018f7-115">-Access</span></span>
<span data-ttu-id="018f7-116">Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="018f7-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="018f7-117">Zulässige Werte für diesen Parameter sind: allow und Deny.</span><span class="sxs-lookup"><span data-stu-id="018f7-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="018f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018f7-118">-DefaultProfile</span></span>
<span data-ttu-id="018f7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="018f7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="018f7-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="018f7-120">-Description</span></span>
<span data-ttu-id="018f7-121">Gibt eine Beschreibung der zu erstellenden Netzwerk Sicherheitsregel Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="018f7-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="018f7-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="018f7-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="018f7-123">Gibt ein Ziel Adresspräfix an.</span><span class="sxs-lookup"><span data-stu-id="018f7-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="018f7-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="018f7-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="018f7-125">Eine CIDR-Adresse (classlos InterDomain Routing)</span><span class="sxs-lookup"><span data-stu-id="018f7-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="018f7-126">Ein Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="018f7-126">A destination IP address range</span></span> 
- <span data-ttu-id="018f7-127">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht, die Sie mit Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden können.</span><span class="sxs-lookup"><span data-stu-id="018f7-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="018f7-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="018f7-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="018f7-129">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="018f7-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="018f7-130">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="018f7-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="018f7-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="018f7-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="018f7-132">Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="018f7-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="018f7-133">Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="018f7-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="018f7-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="018f7-134">-DestinationPortRange</span></span>
<span data-ttu-id="018f7-135">Gibt einen Zielport oder einen Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="018f7-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="018f7-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="018f7-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="018f7-137">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="018f7-137">An integer</span></span>
- <span data-ttu-id="018f7-138">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="018f7-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="018f7-139">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="018f7-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="018f7-140">-Richtung</span><span class="sxs-lookup"><span data-stu-id="018f7-140">-Direction</span></span>
<span data-ttu-id="018f7-141">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="018f7-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="018f7-142">Die zulässigen Werte für diesen Parameter lauten: ein-und ausgehende.</span><span class="sxs-lookup"><span data-stu-id="018f7-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="018f7-143">-Name</span><span class="sxs-lookup"><span data-stu-id="018f7-143">-Name</span></span>
<span data-ttu-id="018f7-144">Gibt den Namen der von diesem Cmdlet erstellten Konfiguration der Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="018f7-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="018f7-145">-Priorität</span><span class="sxs-lookup"><span data-stu-id="018f7-145">-Priority</span></span>
<span data-ttu-id="018f7-146">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="018f7-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="018f7-147">Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="018f7-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="018f7-148">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="018f7-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="018f7-149">Je niedriger die Prioritätszahl ist, desto höher ist die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="018f7-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="018f7-150">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="018f7-150">-Protocol</span></span>
<span data-ttu-id="018f7-151">Gibt das Netzwerkprotokoll an, für das eine neue Regelkonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="018f7-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="018f7-152">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="018f7-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="018f7-153">TCP</span><span class="sxs-lookup"><span data-stu-id="018f7-153">Tcp</span></span>
- <span data-ttu-id="018f7-154">UDP</span><span class="sxs-lookup"><span data-stu-id="018f7-154">Udp</span></span>
- <span data-ttu-id="018f7-155">Platzhalterzeichen (\*), um beide zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="018f7-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="018f7-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="018f7-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="018f7-157">Gibt das Präfix einer Quelladresse an.</span><span class="sxs-lookup"><span data-stu-id="018f7-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="018f7-158">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="018f7-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="018f7-159">ein CIDR</span><span class="sxs-lookup"><span data-stu-id="018f7-159">A CIDR</span></span>
- <span data-ttu-id="018f7-160">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="018f7-160">A source IP range</span></span>
- <span data-ttu-id="018f7-161">Ein Platzhalterzeichen (\*), das einer beliebigen IP-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="018f7-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="018f7-162">Sie können auch Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.</span><span class="sxs-lookup"><span data-stu-id="018f7-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="018f7-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="018f7-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="018f7-164">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="018f7-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="018f7-165">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="018f7-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="018f7-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="018f7-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="018f7-167">Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="018f7-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="018f7-168">Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="018f7-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="018f7-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="018f7-169">-SourcePortRange</span></span>
<span data-ttu-id="018f7-170">Gibt den Quell Port oder-Bereich an.</span><span class="sxs-lookup"><span data-stu-id="018f7-170">Specifies the source port or range.</span></span>
<span data-ttu-id="018f7-171">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="018f7-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="018f7-172">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="018f7-172">An integer</span></span>
- <span data-ttu-id="018f7-173">Ein Bereich von ganzen Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="018f7-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="018f7-174">Ein Platzhalterzeichen (\*), das mit einem beliebigen Port übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="018f7-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="018f7-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018f7-175">CommonParameters</span></span>
<span data-ttu-id="018f7-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="018f7-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018f7-177">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="018f7-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018f7-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="018f7-178">INPUTS</span></span>

### <span data-ttu-id="018f7-179">Keine</span><span class="sxs-lookup"><span data-stu-id="018f7-179">None</span></span>

## <span data-ttu-id="018f7-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="018f7-180">OUTPUTS</span></span>

### <span data-ttu-id="018f7-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="018f7-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="018f7-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="018f7-182">NOTES</span></span>

## <span data-ttu-id="018f7-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="018f7-183">RELATED LINKS</span></span>

[<span data-ttu-id="018f7-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="018f7-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="018f7-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="018f7-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="018f7-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="018f7-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="018f7-187">Satz-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="018f7-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


