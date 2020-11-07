---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660551"
---
# <span data-ttu-id="b1d89-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1d89-101">New-AzFirewall</span></span>

## <span data-ttu-id="b1d89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1d89-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d89-103">Erstellt eine neue Firewall in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b1d89-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="b1d89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1d89-104">SYNTAX</span></span>

### <span data-ttu-id="b1d89-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1d89-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1d89-106">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="b1d89-106">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1d89-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1d89-107">DESCRIPTION</span></span>
<span data-ttu-id="b1d89-108">Das Cmdlet **New-AzFirewall** erstellt eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="b1d89-108">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="b1d89-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1d89-109">EXAMPLES</span></span>

### <span data-ttu-id="b1d89-110">1: Erstellen einer Firewall, die mit einem virtuellen Netzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="b1d89-110">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="b1d89-111">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b1d89-111">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="b1d89-112">Da keine Regeln angegeben wurden, blockiert die Firewall den gesamten Datenverkehr (Standardverhalten).</span><span class="sxs-lookup"><span data-stu-id="b1d89-112">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="b1d89-113">Threat Intel wird auch im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="b1d89-113">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="b1d89-114">2: Erstellen einer Firewall, die den gesamten HTTPS-Datenverkehr zulässt</span><span class="sxs-lookup"><span data-stu-id="b1d89-114">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="b1d89-115">In diesem Beispiel wird eine Firewall erstellt, die den gesamten HTTPS-Datenverkehr auf Port 443 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b1d89-115">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="b1d89-116">Threat Intel wird im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="b1d89-116">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="b1d89-117">3: DNAT-Umleiten von Datenverkehr bestimmt zu 10.1.2.3:80 zu 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="b1d89-117">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="b1d89-118">In diesem Beispiel wurde eine Firewall erstellt, die die Ziel-IP-Adresse und den Port aller Pakete übersetzte, die zu 10.1.2.3:80 zu 10.2.3.4:8080 Threat Intel in diesem Beispiel deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b1d89-118">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="b1d89-119">4: Erstellen einer Firewall ohne Regeln und mit Threat Intel im Warnungsmodus</span><span class="sxs-lookup"><span data-stu-id="b1d89-119">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

<span data-ttu-id="b1d89-120">In diesem Beispiel wird eine Firewall erstellt, die den gesamten Datenverkehr (Standardverhalten) blockiert und im Warnungsmodus eine Bedrohung für Intel ausführt.</span><span class="sxs-lookup"><span data-stu-id="b1d89-120">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="b1d89-121">Dies bedeutet, dass Warnungsprotokolle für böswilligen Datenverkehr ausgegeben werden, bevor die anderen Regeln angewendet werden (in diesem Fall nur die Standardregel – alle verweigern).</span><span class="sxs-lookup"><span data-stu-id="b1d89-121">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="b1d89-122">5: Erstellen einer Firewall, die den gesamten HTTP-Datenverkehr auf Port 8080 zulässt, blockiert aber bösartige Domänen, die von Threat Intel identifiziert werden</span><span class="sxs-lookup"><span data-stu-id="b1d89-122">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="b1d89-123">In diesem Beispiel wird eine Firewall erstellt, die den gesamten HTTP-Datenverkehr auf Port 8080 zulässt, es sei denn, Sie wird von Intel als bösartig eingestuft.</span><span class="sxs-lookup"><span data-stu-id="b1d89-123">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="b1d89-124">Bei der Ausführung im Modus "verweigern", im Gegensatz zu "Warnung", wird der Datenverkehr, der als böswillige Bedrohung angesehen wird, nicht nur protokolliert, sondern auch blockiert.</span><span class="sxs-lookup"><span data-stu-id="b1d89-124">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

## <span data-ttu-id="b1d89-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1d89-125">PARAMETERS</span></span>

### <span data-ttu-id="b1d89-126">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b1d89-126">-ApplicationRuleCollection</span></span>
<span data-ttu-id="b1d89-127">Gibt die Sammlungen von Anwendungsregeln für die neue Firewall an.</span><span class="sxs-lookup"><span data-stu-id="b1d89-127">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1d89-128">-AsJob</span></span>
<span data-ttu-id="b1d89-129">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b1d89-129">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d89-130">-DefaultProfile</span></span>
<span data-ttu-id="b1d89-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1d89-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1d89-132">-Force</span><span class="sxs-lookup"><span data-stu-id="b1d89-132">-Force</span></span>
<span data-ttu-id="b1d89-133">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b1d89-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="b1d89-134">-Location</span></span>
<span data-ttu-id="b1d89-135">Gibt den Bereich für die Firewall an.</span><span class="sxs-lookup"><span data-stu-id="b1d89-135">Specifies the region for the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-136">-Name</span><span class="sxs-lookup"><span data-stu-id="b1d89-136">-Name</span></span>
<span data-ttu-id="b1d89-137">Gibt den Namen der Azure-Firewall an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b1d89-137">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-138">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b1d89-138">-NatRuleCollection</span></span>
<span data-ttu-id="b1d89-139">Die Liste der AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="b1d89-139">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-140">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b1d89-140">-NetworkRuleCollection</span></span>
<span data-ttu-id="b1d89-141">Die Liste der AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="b1d89-141">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-142">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="b1d89-142">-PublicIpName</span></span>
<span data-ttu-id="b1d89-143">Öffentlicher IP-Name.</span><span class="sxs-lookup"><span data-stu-id="b1d89-143">Public Ip Name.</span></span> <span data-ttu-id="b1d89-144">Die öffentliche IP-Adresse muss die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="b1d89-144">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d89-145">-ResourceGroupName</span></span>
<span data-ttu-id="b1d89-146">Gibt den Namen einer Ressourcengruppe an, die die Firewall enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="b1d89-146">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1d89-147">-Tag</span></span>
<span data-ttu-id="b1d89-148">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="b1d89-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b1d89-149">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b1d89-149">For example:</span></span>

<span data-ttu-id="b1d89-150">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="b1d89-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-151">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="b1d89-151">-ThreatIntelMode</span></span>
<span data-ttu-id="b1d89-152">Gibt den Vorgangsmodus für Threat Intelligence an.</span><span class="sxs-lookup"><span data-stu-id="b1d89-152">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="b1d89-153">Der Standardmodus ist "Alert", nicht "aus".</span><span class="sxs-lookup"><span data-stu-id="b1d89-153">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-154">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b1d89-154">-VirtualNetworkName</span></span>
<span data-ttu-id="b1d89-155">Gibt den Namen des virtuellen Netzwerks an, für das die Firewall bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b1d89-155">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="b1d89-156">Virtuelles Netzwerk und Firewall müssen derselben Ressourcengruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="b1d89-156">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1d89-157">-Confirm</span></span>
<span data-ttu-id="b1d89-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1d89-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1d89-159">-WhatIf</span></span>
<span data-ttu-id="b1d89-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1d89-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1d89-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1d89-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d89-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d89-162">CommonParameters</span></span>
<span data-ttu-id="b1d89-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d89-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d89-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d89-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d89-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1d89-165">INPUTS</span></span>

### <span data-ttu-id="b1d89-166">System. String</span><span class="sxs-lookup"><span data-stu-id="b1d89-166">System.String</span></span>

### <span data-ttu-id="b1d89-167">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="b1d89-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="b1d89-168">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="b1d89-168">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="b1d89-169">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="b1d89-169">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="b1d89-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b1d89-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b1d89-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1d89-171">OUTPUTS</span></span>

### <span data-ttu-id="b1d89-172">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b1d89-172">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="b1d89-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1d89-173">NOTES</span></span>

## <span data-ttu-id="b1d89-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1d89-174">RELATED LINKS</span></span>

[<span data-ttu-id="b1d89-175">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1d89-175">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="b1d89-176">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1d89-176">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="b1d89-177">Satz-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1d89-177">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="b1d89-178">Neu – AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b1d89-178">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="b1d89-179">Neu – AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b1d89-179">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="b1d89-180">Neu – AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b1d89-180">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
