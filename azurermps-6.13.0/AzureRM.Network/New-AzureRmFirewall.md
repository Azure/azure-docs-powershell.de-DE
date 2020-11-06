---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504357"
---
# <span data-ttu-id="5b3c7-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="5b3c7-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="5b3c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b3c7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b3c7-103">Erstellt eine neue Firewall in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b3c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b3c7-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b3c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b3c7-105">DESCRIPTION</span></span>
<span data-ttu-id="5b3c7-106">Das Cmdlet **New-AzureRmFirewall** erstellt eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="5b3c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b3c7-107">EXAMPLES</span></span>

### <span data-ttu-id="5b3c7-108">1: Erstellen einer Firewall, die mit einem virtuellen Netzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="5b3c7-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="5b3c7-109">In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="5b3c7-110">Da keine Regeln angegeben wurden, blockiert die Firewall den gesamten Datenverkehr (Standardverhalten).</span><span class="sxs-lookup"><span data-stu-id="5b3c7-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="5b3c7-111">2: Erstellen einer Firewall, die den gesamten HTTPS-Datenverkehr zulässt</span><span class="sxs-lookup"><span data-stu-id="5b3c7-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="5b3c7-112">In diesem Beispiel wird eine Firewall erstellt, die den gesamten HTTPS-Datenverkehr auf Port 443 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="5b3c7-113">3: DNAT-Umleiten von Datenverkehr bestimmt zu 10.1.2.3:80 zu 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="5b3c7-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="5b3c7-114">In diesem Beispiel wurde eine Firewall erstellt, die die Ziel-IP und den Port aller Pakete übersetzte, die an 10.1.2.3:80 bis 10.2.3.4:8080 übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="5b3c7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b3c7-115">PARAMETERS</span></span>

### <span data-ttu-id="5b3c7-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5b3c7-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="5b3c7-117">Gibt die Sammlungen von Anwendungsregeln für die neue Firewall an.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-117">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b3c7-118">-AsJob</span></span>
<span data-ttu-id="5b3c7-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5b3c7-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b3c7-120">-DefaultProfile</span></span>
<span data-ttu-id="5b3c7-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b3c7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5b3c7-122">-Force</span></span>
<span data-ttu-id="5b3c7-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="5b3c7-124">-Location</span></span>
<span data-ttu-id="5b3c7-125">Gibt den Bereich für die Firewall an.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-125">Specifies the region for the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5b3c7-126">-Name</span></span>
<span data-ttu-id="5b3c7-127">Gibt den Namen der Azure-Firewall an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5b3c7-128">-NatRuleCollection</span></span>
<span data-ttu-id="5b3c7-129">Die Liste der AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="5b3c7-129">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5b3c7-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="5b3c7-131">Die Liste der AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="5b3c7-131">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="5b3c7-132">-PublicIpName</span></span>
<span data-ttu-id="5b3c7-133">Öffentlicher IP-Name.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-133">Public Ip Name.</span></span> <span data-ttu-id="5b3c7-134">Die öffentliche IP-Adresse muss die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b3c7-135">-ResourceGroupName</span></span>
<span data-ttu-id="5b3c7-136">Gibt den Namen einer Ressourcengruppe an, die die Firewall enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-136">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b3c7-137">-Tag</span></span>
<span data-ttu-id="5b3c7-138">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="5b3c7-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5b3c7-139">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5b3c7-139">For example:</span></span>

<span data-ttu-id="5b3c7-140">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="5b3c7-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5b3c7-141">-VirtualNetworkName</span></span>
<span data-ttu-id="5b3c7-142">Gibt den Namen des virtuellen Netzwerks an, für das die Firewall bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="5b3c7-143">Virtuelles Netzwerk und Firewall müssen derselben Ressourcengruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-143">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b3c7-144">-Confirm</span></span>
<span data-ttu-id="5b3c7-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b3c7-146">-WhatIf</span></span>
<span data-ttu-id="5b3c7-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b3c7-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3c7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3c7-149">CommonParameters</span></span>
<span data-ttu-id="5b3c7-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3c7-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b3c7-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3c7-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b3c7-152">INPUTS</span></span>

### <span data-ttu-id="5b3c7-153">Keine</span><span class="sxs-lookup"><span data-stu-id="5b3c7-153">None</span></span>
<span data-ttu-id="5b3c7-154">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b3c7-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b3c7-155">OUTPUTS</span></span>

### <span data-ttu-id="5b3c7-156">Microsoft. Azure. Commands. Network. Models. PSFirewall</span><span class="sxs-lookup"><span data-stu-id="5b3c7-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="5b3c7-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b3c7-157">NOTES</span></span>

## <span data-ttu-id="5b3c7-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b3c7-158">RELATED LINKS</span></span>

[<span data-ttu-id="5b3c7-159">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="5b3c7-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="5b3c7-160">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="5b3c7-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="5b3c7-161">Satz-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="5b3c7-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="5b3c7-162">Neu – AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5b3c7-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="5b3c7-163">Neu – AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5b3c7-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="5b3c7-164">Neu – AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5b3c7-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
