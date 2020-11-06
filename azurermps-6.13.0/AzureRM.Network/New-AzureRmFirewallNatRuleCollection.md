---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
ms.openlocfilehash: 12b45dd5fd62dabb2650f121f52a539962315513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480306"
---
# <span data-ttu-id="548bc-101">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="548bc-101">New-AzureRmFirewallNatRuleCollection</span></span>

## <span data-ttu-id="548bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="548bc-102">SYNOPSIS</span></span>
<span data-ttu-id="548bc-103">Erstellt eine Sammlung von Firewall-NAT-Regeln.</span><span class="sxs-lookup"><span data-stu-id="548bc-103">Creates a collection of Firewall NAT rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="548bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="548bc-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="548bc-105">DESCRIPTION</span></span>
<span data-ttu-id="548bc-106">Das Cmdlet **New-AzureRmFirewallNatRuleCollection** erstellt eine Sammlung von Firewall-NAT-Regeln.</span><span class="sxs-lookup"><span data-stu-id="548bc-106">The **New-AzureRmFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="548bc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="548bc-107">EXAMPLES</span></span>

### <span data-ttu-id="548bc-108">1: Erstellen einer Sammlung mit einer Regel</span><span class="sxs-lookup"><span data-stu-id="548bc-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="548bc-109">In diesem Beispiel wird eine Sammlung mit einer Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="548bc-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="548bc-110">Der gesamte Datenverkehr, der den in $Rule 1 angegebenen Bedingungen entspricht, wird übersetzte Adresse und Port DNAT'ed.</span><span class="sxs-lookup"><span data-stu-id="548bc-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="548bc-111">2: Hinzufügen einer Regel zu einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="548bc-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="548bc-112">In diesem Beispiel wird eine neue NAT-Regelsammlung mit einer Regel erstellt und dann der Regelsammlung mithilfe der AddRule-Methode für das Rule Collection-Objekt eine zweite Regel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="548bc-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="548bc-113">Jeder Regelname in einer bestimmten Regelsammlung muss einen eindeutigen Namen haben und die Groß-/Kleinschreibung wird nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="548bc-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="548bc-114">3: Abrufen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="548bc-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="548bc-115">In diesem Beispiel wird eine neue NAT-Regelsammlung mit einer Regel erstellt, und dann wird die Regel nach Namen abgerufen, und die GetRuleByName-Methode wird für das Rule Collection-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="548bc-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="548bc-116">Der Regelname für Methoden-GetRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="548bc-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="548bc-117">4: Entfernen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="548bc-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="548bc-118">In diesem Beispiel wird eine neue NAT-Regelsammlung mit zwei Regeln erstellt, und dann wird die erste Regel aus der Regelsammlung entfernt, indem die RemoveRuleByName-Methode für das Rule Collection-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="548bc-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="548bc-119">Der Regelname für Methoden-RemoveRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="548bc-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="548bc-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="548bc-120">PARAMETERS</span></span>

### <span data-ttu-id="548bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548bc-121">-DefaultProfile</span></span>
<span data-ttu-id="548bc-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="548bc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548bc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="548bc-123">-Name</span></span>
<span data-ttu-id="548bc-124">Gibt den Namen dieser NAT-Regel an.</span><span class="sxs-lookup"><span data-stu-id="548bc-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="548bc-125">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="548bc-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="548bc-126">-Priorität</span><span class="sxs-lookup"><span data-stu-id="548bc-126">-Priority</span></span>
<span data-ttu-id="548bc-127">Gibt die Priorität dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="548bc-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="548bc-128">Priority ist eine Zahl zwischen 100 und 65000.</span><span class="sxs-lookup"><span data-stu-id="548bc-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="548bc-129">Je kleiner die Zahl, desto größer die Priorität.</span><span class="sxs-lookup"><span data-stu-id="548bc-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="548bc-130">-Rule</span><span class="sxs-lookup"><span data-stu-id="548bc-130">-Rule</span></span>
<span data-ttu-id="548bc-131">Gibt die Liste der Regeln an, die unter dieser Sammlung gruppiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="548bc-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548bc-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="548bc-132">-Confirm</span></span>
<span data-ttu-id="548bc-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="548bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548bc-134">-WhatIf</span></span>
<span data-ttu-id="548bc-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="548bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548bc-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="548bc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548bc-137">CommonParameters</span></span>
<span data-ttu-id="548bc-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548bc-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548bc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548bc-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="548bc-140">INPUTS</span></span>

### <span data-ttu-id="548bc-141">Keine</span><span class="sxs-lookup"><span data-stu-id="548bc-141">None</span></span>
<span data-ttu-id="548bc-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="548bc-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="548bc-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="548bc-143">OUTPUTS</span></span>

### <span data-ttu-id="548bc-144">Microsoft. Azure. Commands. Network. Models. PSFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="548bc-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRuleCollection</span></span>

## <span data-ttu-id="548bc-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="548bc-145">NOTES</span></span>

## <span data-ttu-id="548bc-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="548bc-146">RELATED LINKS</span></span>

[<span data-ttu-id="548bc-147">Neu – AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="548bc-147">New-AzureRmFirewallNatRule</span></span>](./New-AzureRmFirewallNatRule.md)

[<span data-ttu-id="548bc-148">Neu – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="548bc-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="548bc-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="548bc-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
