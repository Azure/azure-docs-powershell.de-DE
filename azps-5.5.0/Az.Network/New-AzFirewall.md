---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 031c926d25fe55a9572fe12922ccee26b6371a2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146945"
---
# <span data-ttu-id="d565d-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d565d-101">New-AzFirewall</span></span>

## <span data-ttu-id="d565d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d565d-102">SYNOPSIS</span></span>
<span data-ttu-id="d565d-103">Erstellt eine neue Firewall in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d565d-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="d565d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d565d-104">SYNTAX</span></span>

### <span data-ttu-id="d565d-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="d565d-105">Default (Default)</span></span>
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

### <span data-ttu-id="d565d-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="d565d-106">OldIpConfigurationParameterValues</span></span>
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

### <span data-ttu-id="d565d-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="d565d-107">IpConfigurationParameterValues</span></span>
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

## <span data-ttu-id="d565d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d565d-108">DESCRIPTION</span></span>
<span data-ttu-id="d565d-109">Das **Cmdlet "New-AzFirewall"** erstellt eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="d565d-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="d565d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d565d-110">EXAMPLES</span></span>

### <span data-ttu-id="d565d-111">Beispiel 1: Erstellen einer Firewall, die an ein virtuelles Netzwerk angefügt ist</span><span class="sxs-lookup"><span data-stu-id="d565d-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="d565d-112">In diesem Beispiel wird eine Firewall erstellt, die an das virtuelle Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d565d-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="d565d-113">Da keine Regeln angegeben wurden, blockiert die Firewall den ganzen Datenverkehr (Standardverhalten).</span><span class="sxs-lookup"><span data-stu-id="d565d-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="d565d-114">Threat Intel wird auch im Standardmodus (Warnung) ausgeführt, was bedeutet, dass schädlicher Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="d565d-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="d565d-115">Beispiel 2: Erstellen einer Firewall, die den sämtlichen HTTPS-Datenverkehr zulässt</span><span class="sxs-lookup"><span data-stu-id="d565d-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="d565d-116">In diesem Beispiel wird eine Firewall erstellt, die den sämtlichen HTTPS-Datenverkehr auf Port 443 zulässt.</span><span class="sxs-lookup"><span data-stu-id="d565d-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="d565d-117">Threat Intel wird im Standardmodus (Warnung) ausgeführt, was bedeutet, dass schädlicher Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="d565d-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="d565d-118">Beispiel 3: WERDENT - Datenverkehr umleiten, der auf 10.1.2.3:80 bis 10.2.3.4:8080 umgeleitet wird</span><span class="sxs-lookup"><span data-stu-id="d565d-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="d565d-119">In diesem Beispiel wurde eine Firewall erstellt, die die Ziel-IP und den Port aller Pakete übersetzte, die an 10.1.2.3:80 bis 10.2.3.4:8080 Threat Intel gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d565d-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="d565d-120">Beispiel 4: Erstellen einer Firewall ohne Regeln und mit Threat Intel im Warnungsmodus</span><span class="sxs-lookup"><span data-stu-id="d565d-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="d565d-121">In diesem Beispiel wird eine Firewall erstellt, die den ganzen Datenverkehr blockiert (Standardverhalten) und Threat Intel im Warnungsmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d565d-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="d565d-122">Dies bedeutet, dass Warnungsprotokolle für böswilligen Datenverkehr ausgegeben werden, bevor die anderen Regeln angewendet werden (in diesem Fall nur die Standardregel – Alle verweigern)</span><span class="sxs-lookup"><span data-stu-id="d565d-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="d565d-123">Beispiel 5: Erstellen einer Firewall, die den ganzen HTTP-Datenverkehr auf Port 8080 zulässt, aber von Threat Intel identifizierte schädliche Domänen blockiert</span><span class="sxs-lookup"><span data-stu-id="d565d-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="d565d-124">In diesem Beispiel wird eine Firewall erstellt, die den ganzen HTTP-Datenverkehr auf Port 8080 zulässt, es sei denn, dies wird von Threat Intel als böswillig betrachtet.</span><span class="sxs-lookup"><span data-stu-id="d565d-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="d565d-125">Bei der Ausführung im Benachrichtigungsmodus wird im Gegensatz zu Warnung der von Threat Intel als böswillig betrachtete Datenverkehr nicht nur protokolliert, sondern auch blockiert.</span><span class="sxs-lookup"><span data-stu-id="d565d-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="d565d-126">Beispiel 6: Erstellen einer Firewall ohne Regeln und mit Verfügbarkeitszonen</span><span class="sxs-lookup"><span data-stu-id="d565d-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="d565d-127">In diesem Beispiel wird eine Firewall mit allen verfügbaren Verfügbarkeitszonen erstellt.</span><span class="sxs-lookup"><span data-stu-id="d565d-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="d565d-128">Beispiel 7: Erstellen einer Firewall mit zwei oder mehr öffentlichen IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="d565d-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="d565d-129">In diesem Beispiel wird eine Firewall erstellt, die an das virtuelle Netzwerk "vnet" mit zwei öffentlichen IP-Adressen angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d565d-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="d565d-130">Beispiel 8: Erstellen einer Firewall, die es dem MSSQL-Datenverkehr zu bestimmten SQL ermöglicht</span><span class="sxs-lookup"><span data-stu-id="d565d-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="d565d-131">In diesem Beispiel wird eine Firewall erstellt, die es ermöglicht, dass der Datenverkehr von MSSQL über Standardport 1433 SQL Datenbank sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="d565d-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="d565d-132">Beispiel 9: Erstellen einer Firewall, die an einen virtuellen Hub angefügt ist</span><span class="sxs-lookup"><span data-stu-id="d565d-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="d565d-133">In diesem Beispiel wird eine Firewall erstellt, die an den virtuellen Hub "vHub" angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d565d-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="d565d-134">Der Firewall $fp eine Firewallrichtlinie angefügt.</span><span class="sxs-lookup"><span data-stu-id="d565d-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="d565d-135">Diese Firewall erlaubt/verweigert den Datenverkehr basierend auf den regeln, die in der Firewallrichtlinie für $fp.</span><span class="sxs-lookup"><span data-stu-id="d565d-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="d565d-136">Der virtuelle Hub und die Firewall sollten sich in denselben Regionen befinden.</span><span class="sxs-lookup"><span data-stu-id="d565d-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="d565d-137">Beispiel 10: Erstellen einer Firewall mit Einrichtung der Threat Intelligence-Whitelist</span><span class="sxs-lookup"><span data-stu-id="d565d-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="d565d-138">In diesem Beispiel wird eine Firewall erstellt, die "www.microsoft.com" und "8.8.8.8" aus Threat Intelligence auf whitelistt.</span><span class="sxs-lookup"><span data-stu-id="d565d-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="d565d-139">Beispiel 11: Erstellen einer Firewall mit angepasster Einrichtung des privaten Bereichs</span><span class="sxs-lookup"><span data-stu-id="d565d-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="d565d-140">In diesem Beispiel wird eine Firewall erstellt, die "99.99.99.0/24" und "66.66.0.0/16" als private IP-Bereiche behandelt und keinen Datenverkehr an diese Adressen verursacht.</span><span class="sxs-lookup"><span data-stu-id="d565d-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="d565d-141">Beispiel 12: Erstellen einer Firewall mit einem Verwaltungssubnetz und einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="d565d-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="d565d-142">In diesem Beispiel wird eine Firewall erstellt, die an das virtuelle Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d565d-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="d565d-143">Da keine Regeln angegeben wurden, blockiert die Firewall den ganzen Datenverkehr (Standardverhalten).</span><span class="sxs-lookup"><span data-stu-id="d565d-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="d565d-144">Threat Intel wird auch im Standardmodus (Warnung) ausgeführt, was bedeutet, dass schädlicher Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="d565d-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="d565d-145">Um Szenarien des "Erzwungenen Tunnelns" zu unterstützen, verwendet diese Firewall das Subnetz "AzureFirewallManagementSubnet" und die öffentliche Verwaltungs-IP-Adresse für den Verwaltungsdatenverkehr.</span><span class="sxs-lookup"><span data-stu-id="d565d-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="d565d-146">Beispiel 13: Erstellen einer Firewall mit einer Firewallrichtlinie, die an ein virtuelles Netzwerk angefügt ist</span><span class="sxs-lookup"><span data-stu-id="d565d-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="d565d-147">In diesem Beispiel wird eine Firewall erstellt, die an das virtuelle Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d565d-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="d565d-148">Die Regeln und Threat Intelligence, die auf die Firewall angewendet werden, werden aus der Firewallrichtlinie übernommen.</span><span class="sxs-lookup"><span data-stu-id="d565d-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="d565d-149">Beispiel 14: Erstellen einer Firewall mit EINEM DNS-Proxy und DNS-Servern</span><span class="sxs-lookup"><span data-stu-id="d565d-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="d565d-150">In diesem Beispiel wird eine Firewall erstellt, die an das virtuelle Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d565d-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="d565d-151">Der DNS-Proxy ist für diese Firewall aktiviert, und es werden zwei DNS-Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d565d-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="d565d-152">Außerdem ist "DNS-Proxy für Netzwerkregeln erforderlich" festgelegt. Wenn also Netzwerkregeln mit FQDNs vorhanden sind, wird auch für sie der DNS-Proxy verwendet.</span><span class="sxs-lookup"><span data-stu-id="d565d-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="d565d-153">Beispiel 15: Erstellen einer Firewall mit mehreren IPs.</span><span class="sxs-lookup"><span data-stu-id="d565d-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="d565d-154">Die Firewall kann dem virtuellen Hub zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d565d-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="d565d-155">In diesem Beispiel wird eine Firewall erstellt, die an den virtuellen Hub "Hub" in derselben Ressourcengruppe wie die Firewall angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d565d-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="d565d-156">Der Firewall werden zwei öffentliche IPs zugewiesen, die implizit erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d565d-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="d565d-157">16: Erstellen einer Firewall mit "Active FTP zulassen".</span><span class="sxs-lookup"><span data-stu-id="d565d-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="d565d-158">In diesem Beispiel wird eine Firewall mit der Kennzeichnung "Aktives FTP zulassen" erstellt.</span><span class="sxs-lookup"><span data-stu-id="d565d-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="d565d-159">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d565d-159">PARAMETERS</span></span>

### <span data-ttu-id="d565d-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="d565d-160">-AllowActiveFTP</span></span>
<span data-ttu-id="d565d-161">Lässt Active FTP für die Firewall zu.</span><span class="sxs-lookup"><span data-stu-id="d565d-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="d565d-162">Standardmäßig ist sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d565d-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="d565d-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d565d-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="d565d-164">Gibt die Sammlungen von Anwendungsregeln für die neue Firewall an.</span><span class="sxs-lookup"><span data-stu-id="d565d-164">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="d565d-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d565d-165">-AsJob</span></span>
<span data-ttu-id="d565d-166">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d565d-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d565d-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d565d-167">-DefaultProfile</span></span>
<span data-ttu-id="d565d-168">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d565d-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d565d-169">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="d565d-169">-DnsServer</span></span>
<span data-ttu-id="d565d-170">Die Liste der DNS-Server, die für die Dns-Auflösung verwendet werden sollen,</span><span class="sxs-lookup"><span data-stu-id="d565d-170">The list of DNS Servers to be used for DNS resolution,</span></span>

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

### <span data-ttu-id="d565d-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="d565d-171">-EnableDnsProxy</span></span>
<span data-ttu-id="d565d-172">Aktivieren Sie den DNS-Proxy.</span><span class="sxs-lookup"><span data-stu-id="d565d-172">Enable DNS Proxy.</span></span> <span data-ttu-id="d565d-173">Standardmäßig ist sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d565d-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="d565d-174">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d565d-174">-FirewallPolicyId</span></span>
<span data-ttu-id="d565d-175">Die an die Firewall angefügte Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d565d-175">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="d565d-176">-Force</span><span class="sxs-lookup"><span data-stu-id="d565d-176">-Force</span></span>
<span data-ttu-id="d565d-177">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="d565d-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d565d-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="d565d-178">-HubIPAddress</span></span>
<span data-ttu-id="d565d-179">Die ip-Adressen der Firewall, die an einen virtuellen Hub angefügt sind</span><span class="sxs-lookup"><span data-stu-id="d565d-179">The ip addresses for the firewall attached to a virtual hub</span></span>

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

### <span data-ttu-id="d565d-180">-Location</span><span class="sxs-lookup"><span data-stu-id="d565d-180">-Location</span></span>
<span data-ttu-id="d565d-181">Gibt die Region für die Firewall an.</span><span class="sxs-lookup"><span data-stu-id="d565d-181">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="d565d-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d565d-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="d565d-183">Eine oder mehrere öffentliche IP-Adressen, die für den Verwaltungsverkehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d565d-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="d565d-184">Die öffentlichen IP-Adressen müssen die Standard-SKU verwenden und derselben Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="d565d-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="d565d-185">-Name</span><span class="sxs-lookup"><span data-stu-id="d565d-185">-Name</span></span>
<span data-ttu-id="d565d-186">Gibt den Namen der Azure-Firewall an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d565d-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d565d-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d565d-187">-NatRuleCollection</span></span>
<span data-ttu-id="d565d-188">Die Liste der AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="d565d-188">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="d565d-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d565d-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="d565d-190">Die Liste der AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="d565d-190">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="d565d-191">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="d565d-191">-PrivateRange</span></span>
<span data-ttu-id="d565d-192">Die privaten IP-Bereiche, für die kein Datenverkehr vom SNAT verwendet wird</span><span class="sxs-lookup"><span data-stu-id="d565d-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="d565d-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d565d-193">-PublicIpAddress</span></span>
<span data-ttu-id="d565d-194">Mindestens eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d565d-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="d565d-195">Die öffentlichen IP-Adressen müssen die Standard-SKU verwenden und derselben Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="d565d-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="d565d-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="d565d-196">-PublicIpName</span></span>
<span data-ttu-id="d565d-197">Öffentlicher IP-Name.</span><span class="sxs-lookup"><span data-stu-id="d565d-197">Public Ip Name.</span></span> <span data-ttu-id="d565d-198">Die öffentliche IP muss die Standard-SKU verwenden und derselben Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="d565d-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="d565d-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d565d-199">-ResourceGroupName</span></span>
<span data-ttu-id="d565d-200">Gibt den Namen einer Ressourcengruppe an, die die Firewall enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="d565d-200">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="d565d-201">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d565d-201">-SkuName</span></span>
<span data-ttu-id="d565d-202">Der Name der SKU für die Firewall</span><span class="sxs-lookup"><span data-stu-id="d565d-202">The sku name for firewall</span></span>

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

### <span data-ttu-id="d565d-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d565d-203">-SkuTier</span></span>
<span data-ttu-id="d565d-204">Die SKU-Stufe für die Firewall</span><span class="sxs-lookup"><span data-stu-id="d565d-204">The sku tier for firewall</span></span>

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

### <span data-ttu-id="d565d-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="d565d-205">-Tag</span></span>
<span data-ttu-id="d565d-206">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d565d-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d565d-207">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d565d-207">For example:</span></span>

<span data-ttu-id="d565d-208">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d565d-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d565d-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="d565d-209">-ThreatIntelMode</span></span>
<span data-ttu-id="d565d-210">Gibt den Vorgangsmodus für Threat Intelligence an.</span><span class="sxs-lookup"><span data-stu-id="d565d-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="d565d-211">Der Standardmodus ist "Warnung", nicht "Aus".</span><span class="sxs-lookup"><span data-stu-id="d565d-211">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="d565d-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d565d-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="d565d-213">Die Whitelist für Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="d565d-213">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="d565d-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="d565d-214">-VirtualHubId</span></span>
<span data-ttu-id="d565d-215">Der virtuelle Hub, dem eine Firewall angefügt ist</span><span class="sxs-lookup"><span data-stu-id="d565d-215">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="d565d-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d565d-216">-VirtualNetwork</span></span>
<span data-ttu-id="d565d-217">Virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d565d-217">Virtual Network</span></span>

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

### <span data-ttu-id="d565d-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d565d-218">-VirtualNetworkName</span></span>
<span data-ttu-id="d565d-219">Gibt den Namen des virtuellen Netzwerks an, für das die Firewall bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d565d-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="d565d-220">Virtuelles Netzwerk und Firewall müssen derselben Ressourcengruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="d565d-220">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="d565d-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="d565d-221">-Zone</span></span>
<span data-ttu-id="d565d-222">Eine Liste der Verfügbarkeitszonen, in denen aufgeführt ist, woher die Firewall stammen muss.</span><span class="sxs-lookup"><span data-stu-id="d565d-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="d565d-223">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d565d-223">-Confirm</span></span>
<span data-ttu-id="d565d-224">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d565d-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d565d-225">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d565d-225">-WhatIf</span></span>
<span data-ttu-id="d565d-226">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d565d-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d565d-227">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d565d-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d565d-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d565d-228">CommonParameters</span></span>
<span data-ttu-id="d565d-229">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d565d-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d565d-230">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d565d-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d565d-231">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d565d-231">INPUTS</span></span>

### <span data-ttu-id="d565d-232">System.String</span><span class="sxs-lookup"><span data-stu-id="d565d-232">System.String</span></span>

### <span data-ttu-id="d565d-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d565d-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="d565d-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span><span class="sxs-lookup"><span data-stu-id="d565d-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="d565d-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d565d-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="d565d-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="d565d-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="d565d-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="d565d-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="d565d-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="d565d-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="d565d-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d565d-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d565d-240">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d565d-240">OUTPUTS</span></span>

### <span data-ttu-id="d565d-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d565d-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="d565d-242">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d565d-242">NOTES</span></span>

## <span data-ttu-id="d565d-243">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d565d-243">RELATED LINKS</span></span>

[<span data-ttu-id="d565d-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d565d-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d565d-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d565d-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="d565d-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d565d-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="d565d-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d565d-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="d565d-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d565d-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="d565d-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d565d-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
