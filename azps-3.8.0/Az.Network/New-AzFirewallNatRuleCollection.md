---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: b95be2fc6480b05c528944111e32b0f78c5bd8f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995063"
---
# <span data-ttu-id="7d8ef-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7d8ef-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="7d8ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8ef-103">Erstellt eine Sammlung von Firewall-NAT-Regeln.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="7d8ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d8ef-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d8ef-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d8ef-105">DESCRIPTION</span></span>
<span data-ttu-id="7d8ef-106">Das Cmdlet **New-AzFirewallNatRuleCollection** erstellt eine Sammlung von Firewall-NAT-Regeln.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="7d8ef-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d8ef-107">EXAMPLES</span></span>

### <span data-ttu-id="7d8ef-108">1: Erstellen einer Sammlung mit einer Regel</span><span class="sxs-lookup"><span data-stu-id="7d8ef-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="7d8ef-109">In diesem Beispiel wird eine Sammlung mit einer Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="7d8ef-110">Der gesamte Datenverkehr, der den in $Rule 1 angegebenen Bedingungen entspricht, wird übersetzte Adresse und Port DNAT'ed.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="7d8ef-111">2: Hinzufügen einer Regel zu einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="7d8ef-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="7d8ef-112">In diesem Beispiel wird eine neue NAT-Regelsammlung mit einer Regel erstellt und dann der Regelsammlung mithilfe der AddRule-Methode für das Rule Collection-Objekt eine zweite Regel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="7d8ef-113">Jeder Regelname in einer bestimmten Regelsammlung muss einen eindeutigen Namen haben und die Groß-/Kleinschreibung wird nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="7d8ef-114">3: Abrufen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="7d8ef-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="7d8ef-115">In diesem Beispiel wird eine neue NAT-Regelsammlung mit einer Regel erstellt, und dann wird die Regel nach Namen abgerufen, und die GetRuleByName-Methode wird für das Rule Collection-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="7d8ef-116">Der Regelname für Methoden-GetRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="7d8ef-117">4: Entfernen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="7d8ef-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="7d8ef-118">In diesem Beispiel wird eine neue NAT-Regelsammlung mit zwei Regeln erstellt, und dann wird die erste Regel aus der Regelsammlung entfernt, indem die RemoveRuleByName-Methode für das Rule Collection-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="7d8ef-119">Der Regelname für Methoden-RemoveRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="7d8ef-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d8ef-120">PARAMETERS</span></span>

### <span data-ttu-id="7d8ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8ef-121">-DefaultProfile</span></span>
<span data-ttu-id="7d8ef-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d8ef-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7d8ef-123">-Name</span></span>
<span data-ttu-id="7d8ef-124">Gibt den Namen dieser NAT-Regel an.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="7d8ef-125">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="7d8ef-126">-Priorität</span><span class="sxs-lookup"><span data-stu-id="7d8ef-126">-Priority</span></span>
<span data-ttu-id="7d8ef-127">Gibt die Priorität dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="7d8ef-128">Priority ist eine Zahl zwischen 100 und 65000.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="7d8ef-129">Je kleiner die Zahl, desto größer die Priorität.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="7d8ef-130">-Rule</span><span class="sxs-lookup"><span data-stu-id="7d8ef-130">-Rule</span></span>
<span data-ttu-id="7d8ef-131">Gibt die Liste der Regeln an, die unter dieser Sammlung gruppiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8ef-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d8ef-132">-Confirm</span></span>
<span data-ttu-id="7d8ef-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8ef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8ef-134">-WhatIf</span></span>
<span data-ttu-id="7d8ef-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d8ef-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d8ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8ef-137">CommonParameters</span></span>
<span data-ttu-id="7d8ef-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8ef-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d8ef-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8ef-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d8ef-140">INPUTS</span></span>

### <span data-ttu-id="7d8ef-141">Keine</span><span class="sxs-lookup"><span data-stu-id="7d8ef-141">None</span></span>

## <span data-ttu-id="7d8ef-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d8ef-142">OUTPUTS</span></span>

### <span data-ttu-id="7d8ef-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7d8ef-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="7d8ef-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d8ef-144">NOTES</span></span>

## <span data-ttu-id="7d8ef-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d8ef-145">RELATED LINKS</span></span>

[<span data-ttu-id="7d8ef-146">Neu – AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="7d8ef-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="7d8ef-147">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7d8ef-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="7d8ef-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7d8ef-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
