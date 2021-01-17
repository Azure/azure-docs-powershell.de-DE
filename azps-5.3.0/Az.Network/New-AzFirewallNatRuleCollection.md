---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 4ba57fd922319eb2be6ba001c723b3e668bce59e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469032"
---
# <span data-ttu-id="a5df6-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a5df6-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="a5df6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5df6-102">SYNOPSIS</span></span>
<span data-ttu-id="a5df6-103">Erstellt eine Sammlung von Firewall-NAT-Regeln.</span><span class="sxs-lookup"><span data-stu-id="a5df6-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="a5df6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5df6-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5df6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5df6-105">DESCRIPTION</span></span>
<span data-ttu-id="a5df6-106">Das **Cmdlet "New-AzFirewallNatRuleCollection"** erstellt eine Sammlung von Firewall-NAT-Regeln.</span><span class="sxs-lookup"><span data-stu-id="a5df6-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="a5df6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5df6-107">EXAMPLES</span></span>

### <span data-ttu-id="a5df6-108">Beispiel 1: Erstellen einer Sammlung mit einer Regel</span><span class="sxs-lookup"><span data-stu-id="a5df6-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="a5df6-109">In diesem Beispiel wird eine Sammlung mit einer Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5df6-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="a5df6-110">Alle Datenverkehrsverkehre, die den in $rule 1 genannten Bedingungen entspricht, werden als übersetzte Adresse und Portierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5df6-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="a5df6-111">Beispiel 2: Hinzufügen einer Regel zu einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="a5df6-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="a5df6-112">In diesem Beispiel wird eine neue NAT-Regelsammlung mit einer Regel erstellt, und anschließend wird der Regelsammlung eine zweite Regel hinzugefügt, indem die Methode "AddRule" für das Regelsammlungsobjekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5df6-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="a5df6-113">Jeder Regelname in einer bestimmten Regelsammlung muss einen eindeutigen Namen haben und die Groß-/Kleinschreibung wird nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a5df6-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="a5df6-114">Beispiel 3: Erhalten einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="a5df6-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="a5df6-115">Dieses Beispiel erstellt eine neue NAT-Regelsammlung mit einer Regel und ruft dann die Regel nach Name ab, indem die Methode "GetRuleByName" für das Regelsammlungsobjekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="a5df6-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="a5df6-116">Beim Regelnamen für die Methode "GetRuleByName" wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a5df6-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="a5df6-117">Beispiel 4: Entfernen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="a5df6-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="a5df6-118">Dieses Beispiel erstellt eine neue NAT-Regelsammlung mit zwei Regeln und entfernt dann die erste Regel aus der Regelsammlung durch Aufrufen der Methode "RemoveRuleByName" für das Regelsammlungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a5df6-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="a5df6-119">Beim Regelnamen für die Methode "RemoveRuleByName" wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a5df6-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="a5df6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5df6-120">PARAMETERS</span></span>

### <span data-ttu-id="a5df6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5df6-121">-DefaultProfile</span></span>
<span data-ttu-id="a5df6-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5df6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5df6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a5df6-123">-Name</span></span>
<span data-ttu-id="a5df6-124">Gibt den Namen dieser NAT-Regel an.</span><span class="sxs-lookup"><span data-stu-id="a5df6-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="a5df6-125">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a5df6-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="a5df6-126">-Priority</span><span class="sxs-lookup"><span data-stu-id="a5df6-126">-Priority</span></span>
<span data-ttu-id="a5df6-127">Gibt die Priorität dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="a5df6-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="a5df6-128">Priorität ist eine Zahl zwischen 100 und 65000.</span><span class="sxs-lookup"><span data-stu-id="a5df6-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="a5df6-129">Je kleiner die Zahl, desto größer die Priorität.</span><span class="sxs-lookup"><span data-stu-id="a5df6-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="a5df6-130">-Rule</span><span class="sxs-lookup"><span data-stu-id="a5df6-130">-Rule</span></span>
<span data-ttu-id="a5df6-131">Gibt die Liste der Regeln an, die in dieser Sammlung gruppieren werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a5df6-131">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="a5df6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5df6-132">-Confirm</span></span>
<span data-ttu-id="a5df6-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5df6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5df6-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a5df6-134">-WhatIf</span></span>
<span data-ttu-id="a5df6-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5df6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5df6-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5df6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5df6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5df6-137">CommonParameters</span></span>
<span data-ttu-id="a5df6-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5df6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5df6-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5df6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5df6-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5df6-140">INPUTS</span></span>

### <span data-ttu-id="a5df6-141">Keine</span><span class="sxs-lookup"><span data-stu-id="a5df6-141">None</span></span>

## <span data-ttu-id="a5df6-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5df6-142">OUTPUTS</span></span>

### <span data-ttu-id="a5df6-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a5df6-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="a5df6-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a5df6-144">NOTES</span></span>

## <span data-ttu-id="a5df6-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a5df6-145">RELATED LINKS</span></span>

[<span data-ttu-id="a5df6-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="a5df6-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="a5df6-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a5df6-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a5df6-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a5df6-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
