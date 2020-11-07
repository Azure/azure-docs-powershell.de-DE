---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821600"
---
# <span data-ttu-id="144ec-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="144ec-101">New-AzFirewall</span></span>

## <span data-ttu-id="144ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="144ec-102">SYNOPSIS</span></span>
<span data-ttu-id="144ec-103">Erstellt eine neue Firewall in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="144ec-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="144ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="144ec-104">SYNTAX</span></span>

### <span data-ttu-id="144ec-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="144ec-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="144ec-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="144ec-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="144ec-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="144ec-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="144ec-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="144ec-108">DESCRIPTION</span></span>
<span data-ttu-id="144ec-109">Das Cmdlet **New-AzFirewall** erstellt eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="144ec-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="144ec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="144ec-110">EXAMPLES</span></span>

### <span data-ttu-id="144ec-111">1: Erstellen einer Firewall, die mit einem virtuellen Netzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="144ec-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="144ec-112">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="144ec-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="144ec-113">Da keine Regeln angegeben wurden, blockiert die Firewall den gesamten Datenverkehr (Standardverhalten).</span><span class="sxs-lookup"><span data-stu-id="144ec-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="144ec-114">Threat Intel wird auch im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="144ec-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="144ec-115">2: Erstellen einer Firewall, die den gesamten HTTPS-Datenverkehr zulässt</span><span class="sxs-lookup"><span data-stu-id="144ec-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="144ec-116">In diesem Beispiel wird eine Firewall erstellt, die den gesamten HTTPS-Datenverkehr auf Port 443 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="144ec-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="144ec-117">Threat Intel wird im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="144ec-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="144ec-118">3: DNAT-Umleiten von Datenverkehr bestimmt zu 10.1.2.3:80 zu 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="144ec-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="144ec-119">In diesem Beispiel wurde eine Firewall erstellt, die die Ziel-IP-Adresse und den Port aller Pakete übersetzte, die zu 10.1.2.3:80 zu 10.2.3.4:8080 Threat Intel in diesem Beispiel deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="144ec-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="144ec-120">4: Erstellen einer Firewall ohne Regeln und mit Threat Intel im Warnungsmodus</span><span class="sxs-lookup"><span data-stu-id="144ec-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="144ec-121">In diesem Beispiel wird eine Firewall erstellt, die den gesamten Datenverkehr (Standardverhalten) blockiert und im Warnungsmodus eine Bedrohung für Intel ausführt.</span><span class="sxs-lookup"><span data-stu-id="144ec-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="144ec-122">Dies bedeutet, dass Warnungsprotokolle für böswilligen Datenverkehr ausgegeben werden, bevor die anderen Regeln angewendet werden (in diesem Fall nur die Standardregel – alle verweigern).</span><span class="sxs-lookup"><span data-stu-id="144ec-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="144ec-123">5: Erstellen einer Firewall, die den gesamten HTTP-Datenverkehr auf Port 8080 zulässt, blockiert aber bösartige Domänen, die von Threat Intel identifiziert werden</span><span class="sxs-lookup"><span data-stu-id="144ec-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="144ec-124">In diesem Beispiel wird eine Firewall erstellt, die den gesamten HTTP-Datenverkehr auf Port 8080 zulässt, es sei denn, Sie wird von Intel als bösartig eingestuft.</span><span class="sxs-lookup"><span data-stu-id="144ec-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="144ec-125">Bei der Ausführung im Modus "verweigern", im Gegensatz zu "Warnung", wird der Datenverkehr, der als böswillige Bedrohung angesehen wird, nicht nur protokolliert, sondern auch blockiert.</span><span class="sxs-lookup"><span data-stu-id="144ec-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="144ec-126">6: Erstellen einer Firewall ohne Regeln und mit Verfügbarkeits Zonen</span><span class="sxs-lookup"><span data-stu-id="144ec-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="144ec-127">In diesem Beispiel wird eine Firewall mit allen verfügbaren Verfügbarkeits Zonen erstellt.</span><span class="sxs-lookup"><span data-stu-id="144ec-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="144ec-128">7: Erstellen einer Firewall mit zwei oder mehr öffentlichen IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="144ec-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="144ec-129">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" mit zwei öffentlichen IP-Adressen verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="144ec-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="144ec-130">8: Erstellen einer Firewall, die MSSQL-Datenverkehr zu einer bestimmten SQL-Datenbank ermöglicht</span><span class="sxs-lookup"><span data-stu-id="144ec-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="144ec-131">In diesem Beispiel wird eine Firewall erstellt, die den MSSQL-Datenverkehr auf dem Standard Port 1433 in die SQL-Datenbank SQL1.Database.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="144ec-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="144ec-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="144ec-132">PARAMETERS</span></span>

### <span data-ttu-id="144ec-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="144ec-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="144ec-134">Gibt die Sammlungen von Anwendungsregeln für die neue Firewall an.</span><span class="sxs-lookup"><span data-stu-id="144ec-134">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="144ec-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="144ec-135">-AsJob</span></span>
<span data-ttu-id="144ec-136">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="144ec-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="144ec-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144ec-137">-DefaultProfile</span></span>
<span data-ttu-id="144ec-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="144ec-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="144ec-139">-Force</span><span class="sxs-lookup"><span data-stu-id="144ec-139">-Force</span></span>
<span data-ttu-id="144ec-140">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="144ec-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="144ec-141">-Standort</span><span class="sxs-lookup"><span data-stu-id="144ec-141">-Location</span></span>
<span data-ttu-id="144ec-142">Gibt den Bereich für die Firewall an.</span><span class="sxs-lookup"><span data-stu-id="144ec-142">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="144ec-143">-Name</span><span class="sxs-lookup"><span data-stu-id="144ec-143">-Name</span></span>
<span data-ttu-id="144ec-144">Gibt den Namen der Azure-Firewall an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="144ec-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="144ec-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="144ec-145">-NatRuleCollection</span></span>
<span data-ttu-id="144ec-146">Die Liste der AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="144ec-146">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="144ec-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="144ec-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="144ec-148">Die Liste der AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="144ec-148">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="144ec-149">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="144ec-149">-PublicIpAddress</span></span>
<span data-ttu-id="144ec-150">Eine oder mehrere öffentliche IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="144ec-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="144ec-151">Die öffentlichen IP-Adressen müssen die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="144ec-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="144ec-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="144ec-152">-PublicIpName</span></span>
<span data-ttu-id="144ec-153">Öffentlicher IP-Name.</span><span class="sxs-lookup"><span data-stu-id="144ec-153">Public Ip Name.</span></span> <span data-ttu-id="144ec-154">Die öffentliche IP-Adresse muss die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="144ec-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="144ec-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="144ec-155">-ResourceGroupName</span></span>
<span data-ttu-id="144ec-156">Gibt den Namen einer Ressourcengruppe an, die die Firewall enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="144ec-156">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="144ec-157">-Zone</span><span class="sxs-lookup"><span data-stu-id="144ec-157">-Zone</span></span>
<span data-ttu-id="144ec-158">Eine Liste der Verfügbarkeits Zonen, die angibt, woher die Firewall stammen muss.</span><span class="sxs-lookup"><span data-stu-id="144ec-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="144ec-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="144ec-159">-Tag</span></span>
<span data-ttu-id="144ec-160">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="144ec-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="144ec-161">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="144ec-161">For example:</span></span>

<span data-ttu-id="144ec-162">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="144ec-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="144ec-163">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="144ec-163">-ThreatIntelMode</span></span>
<span data-ttu-id="144ec-164">Gibt den Vorgangsmodus für Threat Intelligence an.</span><span class="sxs-lookup"><span data-stu-id="144ec-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="144ec-165">Der Standardmodus ist "Alert", nicht "aus".</span><span class="sxs-lookup"><span data-stu-id="144ec-165">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="144ec-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="144ec-166">-VirtualNetwork</span></span>
<span data-ttu-id="144ec-167">Virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="144ec-167">Virtual Network</span></span>

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

### <span data-ttu-id="144ec-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="144ec-168">-VirtualNetworkName</span></span>
<span data-ttu-id="144ec-169">Gibt den Namen des virtuellen Netzwerks an, für das die Firewall bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="144ec-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="144ec-170">Virtuelles Netzwerk und Firewall müssen derselben Ressourcengruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="144ec-170">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="144ec-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="144ec-171">-Confirm</span></span>
<span data-ttu-id="144ec-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="144ec-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="144ec-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="144ec-173">-WhatIf</span></span>
<span data-ttu-id="144ec-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="144ec-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="144ec-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="144ec-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="144ec-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144ec-176">CommonParameters</span></span>
<span data-ttu-id="144ec-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="144ec-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144ec-178">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="144ec-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144ec-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="144ec-179">INPUTS</span></span>

### <span data-ttu-id="144ec-180">System. String</span><span class="sxs-lookup"><span data-stu-id="144ec-180">System.String</span></span>

### <span data-ttu-id="144ec-181">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="144ec-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="144ec-182">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="144ec-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="144ec-183">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="144ec-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="144ec-184">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="144ec-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="144ec-185">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="144ec-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="144ec-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="144ec-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="144ec-187">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="144ec-187">OUTPUTS</span></span>

### <span data-ttu-id="144ec-188">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="144ec-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="144ec-189">Notizen</span><span class="sxs-lookup"><span data-stu-id="144ec-189">NOTES</span></span>

## <span data-ttu-id="144ec-190">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="144ec-190">RELATED LINKS</span></span>

[<span data-ttu-id="144ec-191">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="144ec-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="144ec-192">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="144ec-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="144ec-193">Satz-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="144ec-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="144ec-194">Neu – AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="144ec-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="144ec-195">Neu – AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="144ec-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="144ec-196">Neu – AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="144ec-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
