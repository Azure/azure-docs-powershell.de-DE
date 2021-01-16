---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298272"
---
# <span data-ttu-id="5c122-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c122-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="5c122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c122-102">SYNOPSIS</span></span>
<span data-ttu-id="5c122-103">Erstellt eine Konfiguration für Netzwerksicherheitsregel.</span><span class="sxs-lookup"><span data-stu-id="5c122-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="5c122-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c122-104">SYNTAX</span></span>

### <span data-ttu-id="5c122-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c122-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c122-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c122-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c122-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c122-107">DESCRIPTION</span></span>
<span data-ttu-id="5c122-108">Das **Cmdlet "New-AzNetworkSecurityRuleConfig"** erstellt eine Konfiguration einer Azure-Netzwerksicherheitsregel für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5c122-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="5c122-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c122-109">EXAMPLES</span></span>

### <span data-ttu-id="5c122-110">Beispiel 1: Erstellen einer Netzwerksicherheitsregel zum Zulassen von RDP</span><span class="sxs-lookup"><span data-stu-id="5c122-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="5c122-111">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff über das Internet auf Port 3389 zu erlaubt.</span><span class="sxs-lookup"><span data-stu-id="5c122-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="5c122-112">Beispiel 2: Erstellen einer Netzwerksicherheitsregel, die HTTP zulässt</span><span class="sxs-lookup"><span data-stu-id="5c122-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="5c122-113">Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff über das Internet auf Port 80 zu erlaubt.</span><span class="sxs-lookup"><span data-stu-id="5c122-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="5c122-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c122-114">PARAMETERS</span></span>

### <span data-ttu-id="5c122-115">-Access</span><span class="sxs-lookup"><span data-stu-id="5c122-115">-Access</span></span>
<span data-ttu-id="5c122-116">Gibt an, ob Netzwerkdatenverkehr zulässig oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="5c122-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="5c122-117">Die zulässigen Werte für diesen Parameter sind: Zulassen und Verweigern.</span><span class="sxs-lookup"><span data-stu-id="5c122-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="5c122-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c122-118">-DefaultProfile</span></span>
<span data-ttu-id="5c122-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c122-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c122-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c122-120">-Description</span></span>
<span data-ttu-id="5c122-121">Gibt eine Beschreibung der Konfiguration der Netzwerksicherheitsregel an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c122-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="5c122-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5c122-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="5c122-123">Gibt ein Zieladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="5c122-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="5c122-124">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5c122-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c122-125">Eine klassenloses domänenübergreifendes Routing (CIDR)</span><span class="sxs-lookup"><span data-stu-id="5c122-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="5c122-126">Ziel-IP-Adressbereich</span><span class="sxs-lookup"><span data-stu-id="5c122-126">A destination IP address range</span></span> 
- <span data-ttu-id="5c122-127">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit beliebigen IP-Adressen. Sie können Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c122-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="5c122-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5c122-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="5c122-129">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5c122-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="5c122-130">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c122-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5c122-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5c122-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="5c122-132">Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5c122-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="5c122-133">Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c122-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5c122-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="5c122-134">-DestinationPortRange</span></span>
<span data-ttu-id="5c122-135">Gibt einen Zielport oder Zielbereich an.</span><span class="sxs-lookup"><span data-stu-id="5c122-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="5c122-136">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5c122-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c122-137">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="5c122-137">An integer</span></span>
- <span data-ttu-id="5c122-138">Ein Bereich ganzer Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="5c122-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="5c122-139">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einem Port</span><span class="sxs-lookup"><span data-stu-id="5c122-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="5c122-140">-Direction</span><span class="sxs-lookup"><span data-stu-id="5c122-140">-Direction</span></span>
<span data-ttu-id="5c122-141">Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="5c122-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="5c122-142">Die zulässigen Werte für diesen Parameter sind: "Ein- und ausgehend".</span><span class="sxs-lookup"><span data-stu-id="5c122-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="5c122-143">-Name</span><span class="sxs-lookup"><span data-stu-id="5c122-143">-Name</span></span>
<span data-ttu-id="5c122-144">Gibt den Namen der Netzwerksicherheitsregelkonfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c122-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5c122-145">-Priority</span><span class="sxs-lookup"><span data-stu-id="5c122-145">-Priority</span></span>
<span data-ttu-id="5c122-146">Gibt die Priorität einer Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5c122-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="5c122-147">Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.</span><span class="sxs-lookup"><span data-stu-id="5c122-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="5c122-148">Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="5c122-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="5c122-149">Je niedriger die Prioritätsnummer, desto höher die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="5c122-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="5c122-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5c122-150">-Protocol</span></span>
<span data-ttu-id="5c122-151">Gibt das Netzwerkprotokoll an, auf das eine neue Regelkonfiguration angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c122-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="5c122-152">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5c122-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c122-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="5c122-153">Tcp</span></span>
- <span data-ttu-id="5c122-154">Udp</span><span class="sxs-lookup"><span data-stu-id="5c122-154">Udp</span></span>
- <span data-ttu-id="5c122-155">Platzhalterzeichen (\*) für beides.</span><span class="sxs-lookup"><span data-stu-id="5c122-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="5c122-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5c122-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="5c122-157">Gibt ein Quelladressenpräfix an.</span><span class="sxs-lookup"><span data-stu-id="5c122-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="5c122-158">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5c122-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c122-159">A CIDR</span><span class="sxs-lookup"><span data-stu-id="5c122-159">A CIDR</span></span>
- <span data-ttu-id="5c122-160">Ein Quell-IP-Bereich</span><span class="sxs-lookup"><span data-stu-id="5c122-160">A source IP range</span></span>
- <span data-ttu-id="5c122-161">Ein Platzhalterzeichen (\*) für eine beliebige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5c122-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="5c122-162">Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c122-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="5c122-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5c122-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="5c122-164">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5c122-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="5c122-165">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c122-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5c122-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5c122-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="5c122-167">Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5c122-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="5c122-168">Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c122-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="5c122-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="5c122-169">-SourcePortRange</span></span>
<span data-ttu-id="5c122-170">Gibt den Quellport oder -bereich an.</span><span class="sxs-lookup"><span data-stu-id="5c122-170">Specifies the source port or range.</span></span>
<span data-ttu-id="5c122-171">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5c122-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c122-172">Eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="5c122-172">An integer</span></span>
- <span data-ttu-id="5c122-173">Ein Bereich ganzer Zahlen zwischen 0 und 65535</span><span class="sxs-lookup"><span data-stu-id="5c122-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="5c122-174">Ein Platzhalterzeichen (\*) zur Übereinstimmung mit einem Port</span><span class="sxs-lookup"><span data-stu-id="5c122-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="5c122-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c122-175">CommonParameters</span></span>
<span data-ttu-id="5c122-176">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c122-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c122-177">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c122-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c122-178">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c122-178">INPUTS</span></span>

### <span data-ttu-id="5c122-179">Keine</span><span class="sxs-lookup"><span data-stu-id="5c122-179">None</span></span>

## <span data-ttu-id="5c122-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c122-180">OUTPUTS</span></span>

### <span data-ttu-id="5c122-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="5c122-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="5c122-182">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5c122-182">NOTES</span></span>

## <span data-ttu-id="5c122-183">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5c122-183">RELATED LINKS</span></span>

[<span data-ttu-id="5c122-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c122-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5c122-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c122-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5c122-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c122-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5c122-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c122-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


