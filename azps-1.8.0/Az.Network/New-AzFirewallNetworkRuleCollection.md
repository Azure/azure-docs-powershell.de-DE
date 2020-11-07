---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: af0a81cf915cd853bfc8ca957d706cdb45d96180
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660540"
---
# <span data-ttu-id="6c0ed-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="6c0ed-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="6c0ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c0ed-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0ed-103">Erstellt eine Azure Firewall-Netzwerksammlung von Netzwerkregeln.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="6c0ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c0ed-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c0ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c0ed-105">DESCRIPTION</span></span>
<span data-ttu-id="6c0ed-106">Das Cmdlet **New-AzFirewallNetworkRuleCollection** erstellt eine Sammlung von Firewall-Netzwerkregeln.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="6c0ed-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c0ed-107">EXAMPLES</span></span>

### <span data-ttu-id="6c0ed-108">1: Erstellen einer Netzwerksammlung mit zwei Regeln</span><span class="sxs-lookup"><span data-stu-id="6c0ed-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="6c0ed-109">In diesem Beispiel wird eine Sammlung erstellt, die den gesamten Datenverkehr zulässt, der einer der beiden Regeln entspricht.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="6c0ed-110">Die erste Regel gilt für den gesamten UDP-Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="6c0ed-111">Die zweite Regel ist der TCP-Datenverkehr von 10.0.0.0 zu 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="6c0ed-112">Wenn eine andere Netzwerkregel Sammlung mit höherer Priorität (geringere Zahl) vorhanden ist, die auch dem in $Rule 1 oder $Rule 2 angegebenen Datenverkehr entspricht, wird stattdessen die Aktion der Regelsammlung mit höherer Priorität wirksam.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="6c0ed-113">2: Hinzufügen einer Regel zu einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="6c0ed-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="6c0ed-114">In diesem Beispiel wird eine neue Netzwerkregel Sammlung mit einer Regel erstellt, und anschließend wird der Regelsammlung mithilfe der AddRule-Methode für das Rule Collection-Objekt eine zweite Regel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="6c0ed-115">Jeder Regelname in einer bestimmten Regelsammlung muss einen eindeutigen Namen haben und die Groß-/Kleinschreibung wird nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="6c0ed-116">3: Abrufen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="6c0ed-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="6c0ed-117">In diesem Beispiel wird eine neue Netzwerkregel Sammlung mit einer Regel erstellt, und dann wird die Regel nach Namen abgerufen, und die GetRuleByName-Methode wird für das Rule Collection-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="6c0ed-118">Der Regelname für Methoden-GetRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="6c0ed-119">4: Entfernen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="6c0ed-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="6c0ed-120">In diesem Beispiel wird eine neue Netzwerkregel Sammlung mit zwei Regeln erstellt, und dann wird die erste Regel aus der Regelsammlung entfernt, indem die RemoveRuleByName-Methode für das Rule Collection-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="6c0ed-121">Der Regelname für Methoden-RemoveRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="6c0ed-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c0ed-122">PARAMETERS</span></span>

### <span data-ttu-id="6c0ed-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="6c0ed-123">-ActionType</span></span>
<span data-ttu-id="6c0ed-124">Gibt die Aktion an, die für Datenverkehrs Übereinstimmungsbedingungen dieser Regel ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="6c0ed-125">Akzeptierte Aktionen sind "zulassen" oder "ablehnen".</span><span class="sxs-lookup"><span data-stu-id="6c0ed-125">Accepted actions are "Allow" or "Deny".</span></span>

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

### <span data-ttu-id="6c0ed-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0ed-126">-DefaultProfile</span></span>
<span data-ttu-id="6c0ed-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c0ed-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6c0ed-128">-Name</span></span>
<span data-ttu-id="6c0ed-129">Gibt den Namen dieser Netzwerkregel Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="6c0ed-130">Der Name muss für alle Netzwerkregel Sammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="6c0ed-131">-Priorität</span><span class="sxs-lookup"><span data-stu-id="6c0ed-131">-Priority</span></span>
<span data-ttu-id="6c0ed-132">Gibt die Priorität dieser Regelsammlung an.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="6c0ed-133">Priority ist eine Zahl zwischen 100 und 65000.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="6c0ed-134">Je kleiner die Zahl, desto höher die Priorität.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-134">The smaller the number, the higher the priority.</span></span>

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

### <span data-ttu-id="6c0ed-135">-Rule</span><span class="sxs-lookup"><span data-stu-id="6c0ed-135">-Rule</span></span>
<span data-ttu-id="6c0ed-136">Gibt die Liste der Regeln an, die unter dieser Sammlung gruppiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-136">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="6c0ed-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c0ed-137">-Confirm</span></span>
<span data-ttu-id="6c0ed-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0ed-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0ed-139">-WhatIf</span></span>
<span data-ttu-id="6c0ed-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0ed-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0ed-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0ed-142">CommonParameters</span></span>
<span data-ttu-id="6c0ed-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0ed-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c0ed-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0ed-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c0ed-145">INPUTS</span></span>

### <span data-ttu-id="6c0ed-146">Keine</span><span class="sxs-lookup"><span data-stu-id="6c0ed-146">None</span></span>

## <span data-ttu-id="6c0ed-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c0ed-147">OUTPUTS</span></span>

### <span data-ttu-id="6c0ed-148">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="6c0ed-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="6c0ed-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c0ed-149">NOTES</span></span>

## <span data-ttu-id="6c0ed-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c0ed-150">RELATED LINKS</span></span>

[<span data-ttu-id="6c0ed-151">Neu – AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6c0ed-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="6c0ed-152">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6c0ed-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="6c0ed-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6c0ed-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
