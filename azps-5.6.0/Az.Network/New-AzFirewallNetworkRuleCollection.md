---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 3ccce01d969f6d6601d4db7383aab505923a7063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935603"
---
# <span data-ttu-id="98bb0-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="98bb0-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="98bb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="98bb0-103">Erstellt eine Azure Firewall Network Collection of Network rules.</span><span class="sxs-lookup"><span data-stu-id="98bb0-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="98bb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98bb0-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98bb0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="98bb0-106">Das **Cmdlet New-AzFirewallNetworkRuleCollection** erstellt eine Sammlung von Firewallnetzwerkregeln.</span><span class="sxs-lookup"><span data-stu-id="98bb0-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="98bb0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98bb0-107">EXAMPLES</span></span>

### <span data-ttu-id="98bb0-108">Beispiel 1: Erstellen einer Netzwerksammlung mit zwei Regeln</span><span class="sxs-lookup"><span data-stu-id="98bb0-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="98bb0-109">In diesem Beispiel wird eine Sammlung erstellt, die allen Datenverkehr zu lässt, der einer der beiden Regeln entspricht.</span><span class="sxs-lookup"><span data-stu-id="98bb0-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="98bb0-110">Die erste Regel gilt für den ganzen UDP-Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="98bb0-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="98bb0-111">Die zweite Regel gilt für DEN TCP-Datenverkehr von 10.0.0.0 bis 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="98bb0-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="98bb0-112">Wenn es eine andere Netzwerkregelsammlung mit höherer Priorität (kleinere Zahl) gibt, die auch dem in $rule 1 oder $rule 2 identifizierten Datenverkehr entspricht, wird stattdessen die Aktion der Regelsammlung mit höherer Priorität wirksam.</span><span class="sxs-lookup"><span data-stu-id="98bb0-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="98bb0-113">Beispiel 2: Hinzufügen einer Regel zu einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="98bb0-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="98bb0-114">In diesem Beispiel wird eine neue Netzwerkregelsammlung mit einer Regel erstellt, und dann wird der Regelsammlung mithilfe von Methoden-AddRule für das Regelsammlungsobjekt eine zweite Regel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bb0-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="98bb0-115">Jeder Regelname in einer bestimmten Regelsammlung muss einen eindeutigen Namen haben und die Groß-/Kleinschreibung nicht beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="98bb0-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="98bb0-116">Beispiel 3: Erhalten einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="98bb0-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="98bb0-117">In diesem Beispiel wird eine neue Netzwerkregelsammlung mit einer Regel erstellt, und dann wird die Regel nach Name und aufruft die -Methode GetRuleByName für das Regelsammlungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="98bb0-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="98bb0-118">Der Regelname für die Methode GetRuleByName ist groß-/kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="98bb0-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="98bb0-119">Beispiel 4: Entfernen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="98bb0-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="98bb0-120">In diesem Beispiel wird eine neue Netzwerkregelsammlung mit zwei Regeln erstellt und dann die erste Regel aus der Regelsammlung entfernt, indem die Methode RemoveRuleByName für das Regelsammlungsobjekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="98bb0-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="98bb0-121">Der Regelname für die Methode RemoveRuleByName ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="98bb0-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="98bb0-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="98bb0-122">PARAMETERS</span></span>

### <span data-ttu-id="98bb0-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="98bb0-123">-ActionType</span></span>
<span data-ttu-id="98bb0-124">Gibt die Aktion an, die für die Bedingungen für den Datenverkehrsabgleich dieser Regel zu ergreifen ist.</span><span class="sxs-lookup"><span data-stu-id="98bb0-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="98bb0-125">Akzeptierte Aktionen sind "Zulassen" oder "Verweigern".</span><span class="sxs-lookup"><span data-stu-id="98bb0-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bb0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98bb0-126">-DefaultProfile</span></span>
<span data-ttu-id="98bb0-127">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98bb0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98bb0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="98bb0-128">-Name</span></span>
<span data-ttu-id="98bb0-129">Gibt den Namen dieser Netzwerkregelsammlung an.</span><span class="sxs-lookup"><span data-stu-id="98bb0-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="98bb0-130">Der Name muss für alle Netzwerkregelsammlungen eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="98bb0-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="98bb0-131">-Priorität</span><span class="sxs-lookup"><span data-stu-id="98bb0-131">-Priority</span></span>
<span data-ttu-id="98bb0-132">Gibt die Priorität dieser Regelsammlung an.</span><span class="sxs-lookup"><span data-stu-id="98bb0-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="98bb0-133">Priorität ist eine Zahl zwischen 100 und 65000.</span><span class="sxs-lookup"><span data-stu-id="98bb0-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="98bb0-134">Je kleiner die Zahl, desto höher die Priorität.</span><span class="sxs-lookup"><span data-stu-id="98bb0-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bb0-135">-Regel</span><span class="sxs-lookup"><span data-stu-id="98bb0-135">-Rule</span></span>
<span data-ttu-id="98bb0-136">Gibt die Liste der Regeln an, die unter dieser Auflistung zu gruppieren sind.</span><span class="sxs-lookup"><span data-stu-id="98bb0-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bb0-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="98bb0-137">-Confirm</span></span>
<span data-ttu-id="98bb0-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98bb0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98bb0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98bb0-139">-WhatIf</span></span>
<span data-ttu-id="98bb0-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98bb0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98bb0-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98bb0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98bb0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98bb0-142">CommonParameters</span></span>
<span data-ttu-id="98bb0-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98bb0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98bb0-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98bb0-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98bb0-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98bb0-145">INPUTS</span></span>

### <span data-ttu-id="98bb0-146">Keine</span><span class="sxs-lookup"><span data-stu-id="98bb0-146">None</span></span>

## <span data-ttu-id="98bb0-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98bb0-147">OUTPUTS</span></span>

### <span data-ttu-id="98bb0-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="98bb0-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="98bb0-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="98bb0-149">NOTES</span></span>

## <span data-ttu-id="98bb0-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="98bb0-150">RELATED LINKS</span></span>

[<span data-ttu-id="98bb0-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="98bb0-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="98bb0-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="98bb0-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="98bb0-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="98bb0-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
