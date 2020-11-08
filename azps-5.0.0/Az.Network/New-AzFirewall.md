---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 031c926d25fe55a9572fe12922ccee26b6371a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178539"
---
# <span data-ttu-id="4532e-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4532e-101">New-AzFirewall</span></span>

## <span data-ttu-id="4532e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4532e-102">SYNOPSIS</span></span>
<span data-ttu-id="4532e-103">Erstellt eine neue Firewall in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4532e-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="4532e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4532e-104">SYNTAX</span></span>

### <span data-ttu-id="4532e-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="4532e-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4532e-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="4532e-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4532e-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="4532e-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4532e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4532e-108">DESCRIPTION</span></span>
<span data-ttu-id="4532e-109">Das Cmdlet **New-AzFirewall** erstellt eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="4532e-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="4532e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4532e-110">EXAMPLES</span></span>

### <span data-ttu-id="4532e-111">Beispiel 1: Erstellen einer Firewall, die mit einem virtuellen Netzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="4532e-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="4532e-112">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4532e-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="4532e-113">Da keine Regeln angegeben wurden, blockiert die Firewall den gesamten Datenverkehr (Standardverhalten).</span><span class="sxs-lookup"><span data-stu-id="4532e-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="4532e-114">Threat Intel wird auch im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="4532e-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="4532e-115">Beispiel 2: Erstellen einer Firewall, die den gesamten HTTPS-Datenverkehr zulässt</span><span class="sxs-lookup"><span data-stu-id="4532e-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="4532e-116">In diesem Beispiel wird eine Firewall erstellt, die den gesamten HTTPS-Datenverkehr auf Port 443 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="4532e-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="4532e-117">Threat Intel wird im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="4532e-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="4532e-118">Beispiel 3: DNAT-Umleiten von Datenverkehr bestimmt zu 10.1.2.3:80 zu 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="4532e-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="4532e-119">In diesem Beispiel wurde eine Firewall erstellt, die die Ziel-IP-Adresse und den Port aller Pakete übersetzte, die zu 10.1.2.3:80 zu 10.2.3.4:8080 Threat Intel in diesem Beispiel deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4532e-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="4532e-120">Beispiel 4: Erstellen einer Firewall ohne Regeln und mit Threat Intel im Warnungsmodus</span><span class="sxs-lookup"><span data-stu-id="4532e-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="4532e-121">In diesem Beispiel wird eine Firewall erstellt, die den gesamten Datenverkehr (Standardverhalten) blockiert und im Warnungsmodus eine Bedrohung für Intel ausführt.</span><span class="sxs-lookup"><span data-stu-id="4532e-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="4532e-122">Dies bedeutet, dass Warnungsprotokolle für böswilligen Datenverkehr ausgegeben werden, bevor die anderen Regeln angewendet werden (in diesem Fall nur die Standardregel – alle verweigern).</span><span class="sxs-lookup"><span data-stu-id="4532e-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="4532e-123">Beispiel 5: Erstellen einer Firewall, die den gesamten HTTP-Datenverkehr auf Port 8080 zulässt, blockiert aber bösartige Domänen, die von Threat Intel identifiziert werden</span><span class="sxs-lookup"><span data-stu-id="4532e-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="4532e-124">In diesem Beispiel wird eine Firewall erstellt, die den gesamten HTTP-Datenverkehr auf Port 8080 zulässt, es sei denn, Sie wird von Intel als bösartig eingestuft.</span><span class="sxs-lookup"><span data-stu-id="4532e-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="4532e-125">Bei der Ausführung im Modus "verweigern", im Gegensatz zu "Warnung", wird der Datenverkehr, der als böswillige Bedrohung angesehen wird, nicht nur protokolliert, sondern auch blockiert.</span><span class="sxs-lookup"><span data-stu-id="4532e-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="4532e-126">Beispiel 6: Erstellen einer Firewall ohne Regeln und mit Verfügbarkeits Zonen</span><span class="sxs-lookup"><span data-stu-id="4532e-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="4532e-127">In diesem Beispiel wird eine Firewall mit allen verfügbaren Verfügbarkeits Zonen erstellt.</span><span class="sxs-lookup"><span data-stu-id="4532e-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="4532e-128">Beispiel 7: Erstellen einer Firewall mit zwei oder mehr öffentlichen IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="4532e-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="4532e-129">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" mit zwei öffentlichen IP-Adressen verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4532e-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="4532e-130">Beispiel 8: Erstellen einer Firewall, die MSSQL-Datenverkehr zu einer bestimmten SQL-Datenbank ermöglicht</span><span class="sxs-lookup"><span data-stu-id="4532e-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="4532e-131">In diesem Beispiel wird eine Firewall erstellt, die den MSSQL-Datenverkehr auf dem Standard Port 1433 in die SQL-Datenbank SQL1.Database.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="4532e-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="4532e-132">Beispiel 9: Erstellen einer Firewall, die mit einem virtuellen Hub verbunden ist</span><span class="sxs-lookup"><span data-stu-id="4532e-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="4532e-133">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Hub "vHub" verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4532e-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="4532e-134">Eine Firewall-Richtlinien $FP wird an die Firewall angefügt.</span><span class="sxs-lookup"><span data-stu-id="4532e-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="4532e-135">Diese Firewall erlaubt/verweigert den Datenverkehr basierend auf den Regeln, die in der Firewall-Richtlinie $FP erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="4532e-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="4532e-136">Der virtuelle Hub und die Firewall sollten sich in denselben Regionen befinden.</span><span class="sxs-lookup"><span data-stu-id="4532e-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="4532e-137">Beispiel 10: Erstellen einer Firewall mit der Einrichtung von Threat Intelligence-Whitelists</span><span class="sxs-lookup"><span data-stu-id="4532e-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="4532e-138">In diesem Beispiel wird eine Firewall erstellt, die "www.Microsoft.com" und "8.8.8.8" aus "Threat Intelligence" Whitelist</span><span class="sxs-lookup"><span data-stu-id="4532e-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="4532e-139">Beispiel 11: Erstellen einer Firewall mit angepasster privater Bereichs Einrichtung</span><span class="sxs-lookup"><span data-stu-id="4532e-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="4532e-140">In diesem Beispiel wird eine Firewall erstellt, die "99.99.99.0/24" und "66.66.0.0/16" als private IP-Bereiche behandelt und Datenverkehr nicht an diese Adressen SNAT.</span><span class="sxs-lookup"><span data-stu-id="4532e-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="4532e-141">Beispiel 12: Erstellen einer Firewall mit einem Verwaltungs-Subnetz und einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="4532e-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="4532e-142">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4532e-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="4532e-143">Da keine Regeln angegeben wurden, blockiert die Firewall den gesamten Datenverkehr (Standardverhalten).</span><span class="sxs-lookup"><span data-stu-id="4532e-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="4532e-144">Threat Intel wird auch im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="4532e-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="4532e-145">Zur Unterstützung von Szenarien mit erzwungenem Tunneling verwendet diese Firewall das Subnetz "AzureFirewallManagementSubnet" und die öffentliche Verwaltungs-IP-Adresse für den Verwaltungsdatenverkehr.</span><span class="sxs-lookup"><span data-stu-id="4532e-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="4532e-146">Beispiel 13: Erstellen einer Firewall mit an ein virtuelles Netzwerk angeschlossener Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4532e-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="4532e-147">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4532e-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="4532e-148">Die Regeln und Bedrohungsinformationen, die auf die Firewall angewendet werden, werden aus der Firewall-Richtlinie übernommen.</span><span class="sxs-lookup"><span data-stu-id="4532e-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="4532e-149">Beispiel 14: Erstellen einer Firewall mit DNS-Proxy-und DNS-Servern</span><span class="sxs-lookup"><span data-stu-id="4532e-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="4532e-150">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4532e-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="4532e-151">DNS-Proxy ist für diese Firewall aktiviert, und es werden zwei DNS-Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4532e-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="4532e-152">Sie müssen auch den DNS-Proxy für Netzwerkregeln festlegen, wenn Netzwerkregeln mit FQDNs vorhanden sind, wird der DNS-Proxy ebenfalls für Sie verwendet.</span><span class="sxs-lookup"><span data-stu-id="4532e-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="4532e-153">Beispiel 15: Erstellen einer Firewall mit mehreren IPS.</span><span class="sxs-lookup"><span data-stu-id="4532e-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="4532e-154">Die Firewall kann dem virtuellen Hub zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="4532e-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="4532e-155">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Hub "Hub" in derselben Ressourcengruppe wie die Firewall verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4532e-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="4532e-156">Der Firewall werden 2 öffentliche IPS zugewiesen, die implizit erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4532e-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="4532e-157">16: Erstellen Sie eine Firewall mit Allow Active FTP.</span><span class="sxs-lookup"><span data-stu-id="4532e-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="4532e-158">In diesem Beispiel wird eine Firewall mit "Allow Active FTP Flag" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4532e-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="4532e-159">Parameter</span><span class="sxs-lookup"><span data-stu-id="4532e-159">PARAMETERS</span></span>

### <span data-ttu-id="4532e-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="4532e-160">-AllowActiveFTP</span></span>
<span data-ttu-id="4532e-161">Ermöglicht Active FTP auf der Firewall.</span><span class="sxs-lookup"><span data-stu-id="4532e-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="4532e-162">Standardmäßig ist es deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4532e-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="4532e-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4532e-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="4532e-164">Gibt die Sammlungen von Anwendungsregeln für die neue Firewall an.</span><span class="sxs-lookup"><span data-stu-id="4532e-164">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="4532e-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4532e-165">-AsJob</span></span>
<span data-ttu-id="4532e-166">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4532e-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4532e-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4532e-167">-DefaultProfile</span></span>
<span data-ttu-id="4532e-168">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4532e-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4532e-169">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="4532e-169">-DnsServer</span></span>
<span data-ttu-id="4532e-170">Die Liste der für die DNS-Auflösung zu verwendenden DNS-Server</span><span class="sxs-lookup"><span data-stu-id="4532e-170">The list of DNS Servers to be used for DNS resolution,</span></span>

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

### <span data-ttu-id="4532e-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="4532e-171">-EnableDnsProxy</span></span>
<span data-ttu-id="4532e-172">Aktivieren des DNS-Proxys</span><span class="sxs-lookup"><span data-stu-id="4532e-172">Enable DNS Proxy.</span></span> <span data-ttu-id="4532e-173">Standardmäßig ist es deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4532e-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="4532e-174">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="4532e-174">-FirewallPolicyId</span></span>
<span data-ttu-id="4532e-175">Die Firewall-Richtlinie, die an die Firewall angefügt ist</span><span class="sxs-lookup"><span data-stu-id="4532e-175">The firewall policy attached to the firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-176">-Force</span><span class="sxs-lookup"><span data-stu-id="4532e-176">-Force</span></span>
<span data-ttu-id="4532e-177">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4532e-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4532e-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="4532e-178">-HubIPAddress</span></span>
<span data-ttu-id="4532e-179">Die IP-Adressen für die Firewall, die an einen virtuellen Hub angefügt ist</span><span class="sxs-lookup"><span data-stu-id="4532e-179">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-180">-Standort</span><span class="sxs-lookup"><span data-stu-id="4532e-180">-Location</span></span>
<span data-ttu-id="4532e-181">Gibt den Bereich für die Firewall an.</span><span class="sxs-lookup"><span data-stu-id="4532e-181">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="4532e-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4532e-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="4532e-183">Eine oder mehrere öffentliche IP-Adressen, die für den Verwaltungsdatenverkehr verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4532e-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="4532e-184">Die öffentlichen IP-Adressen müssen die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="4532e-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-185">-Name</span><span class="sxs-lookup"><span data-stu-id="4532e-185">-Name</span></span>
<span data-ttu-id="4532e-186">Gibt den Namen der Azure-Firewall an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4532e-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4532e-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4532e-187">-NatRuleCollection</span></span>
<span data-ttu-id="4532e-188">Die Liste der AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="4532e-188">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="4532e-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4532e-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="4532e-190">Die Liste der AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="4532e-190">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="4532e-191">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="4532e-191">-PrivateRange</span></span>
<span data-ttu-id="4532e-192">Die privaten IP-Bereiche, in denen der Datenverkehr nicht SNAT'ed werden soll</span><span class="sxs-lookup"><span data-stu-id="4532e-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="4532e-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4532e-193">-PublicIpAddress</span></span>
<span data-ttu-id="4532e-194">Eine oder mehrere öffentliche IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="4532e-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="4532e-195">Die öffentlichen IP-Adressen müssen die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="4532e-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="4532e-196">-PublicIpName</span></span>
<span data-ttu-id="4532e-197">Öffentlicher IP-Name.</span><span class="sxs-lookup"><span data-stu-id="4532e-197">Public Ip Name.</span></span> <span data-ttu-id="4532e-198">Die öffentliche IP-Adresse muss die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="4532e-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4532e-199">-ResourceGroupName</span></span>
<span data-ttu-id="4532e-200">Gibt den Namen einer Ressourcengruppe an, die die Firewall enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="4532e-200">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="4532e-201">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4532e-201">-SkuName</span></span>
<span data-ttu-id="4532e-202">Der SKU-Name für Firewall</span><span class="sxs-lookup"><span data-stu-id="4532e-202">The sku name for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Sku
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4532e-203">-SkuTier</span></span>
<span data-ttu-id="4532e-204">Die SKU-Ebene für Firewall</span><span class="sxs-lookup"><span data-stu-id="4532e-204">The sku tier for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="4532e-205">-Tag</span></span>
<span data-ttu-id="4532e-206">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="4532e-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4532e-207">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4532e-207">For example:</span></span>

<span data-ttu-id="4532e-208">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="4532e-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4532e-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="4532e-209">-ThreatIntelMode</span></span>
<span data-ttu-id="4532e-210">Gibt den Vorgangsmodus für Threat Intelligence an.</span><span class="sxs-lookup"><span data-stu-id="4532e-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="4532e-211">Der Standardmodus ist "Alert", nicht "aus".</span><span class="sxs-lookup"><span data-stu-id="4532e-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="4532e-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="4532e-213">Die Whitelist für Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="4532e-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="4532e-214">-VirtualHubId</span></span>
<span data-ttu-id="4532e-215">Der virtuelle Hub, an den eine Firewall angefügt ist</span><span class="sxs-lookup"><span data-stu-id="4532e-215">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4532e-216">-VirtualNetwork</span></span>
<span data-ttu-id="4532e-217">Virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="4532e-217">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4532e-218">-VirtualNetworkName</span></span>
<span data-ttu-id="4532e-219">Gibt den Namen des virtuellen Netzwerks an, für das die Firewall bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4532e-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="4532e-220">Virtuelles Netzwerk und Firewall müssen derselben Ressourcengruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="4532e-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4532e-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="4532e-221">-Zone</span></span>
<span data-ttu-id="4532e-222">Eine Liste der Verfügbarkeits Zonen, die angibt, woher die Firewall stammen muss.</span><span class="sxs-lookup"><span data-stu-id="4532e-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="4532e-223">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4532e-223">-Confirm</span></span>
<span data-ttu-id="4532e-224">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4532e-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4532e-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4532e-225">-WhatIf</span></span>
<span data-ttu-id="4532e-226">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4532e-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4532e-227">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4532e-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4532e-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4532e-228">CommonParameters</span></span>
<span data-ttu-id="4532e-229">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4532e-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4532e-230">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4532e-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4532e-231">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4532e-231">INPUTS</span></span>

### <span data-ttu-id="4532e-232">System. String</span><span class="sxs-lookup"><span data-stu-id="4532e-232">System.String</span></span>

### <span data-ttu-id="4532e-233">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4532e-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="4532e-234">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="4532e-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="4532e-235">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4532e-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="4532e-236">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="4532e-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="4532e-237">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="4532e-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="4532e-238">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="4532e-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="4532e-239">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4532e-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4532e-240">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4532e-240">OUTPUTS</span></span>

### <span data-ttu-id="4532e-241">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="4532e-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="4532e-242">Notizen</span><span class="sxs-lookup"><span data-stu-id="4532e-242">NOTES</span></span>

## <span data-ttu-id="4532e-243">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4532e-243">RELATED LINKS</span></span>

[<span data-ttu-id="4532e-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4532e-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="4532e-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4532e-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="4532e-246">Satz-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4532e-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="4532e-247">Neu – AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4532e-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="4532e-248">Neu – AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4532e-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="4532e-249">Neu – AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4532e-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
