---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 3e70aa93db8a230308687ce8b03d05d80ab3ab1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175060"
---
# <span data-ttu-id="8a912-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8a912-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="8a912-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a912-102">SYNOPSIS</span></span>
<span data-ttu-id="8a912-103">Erstellt eine Sammlung von Firewall-Anwendungsregeln.</span><span class="sxs-lookup"><span data-stu-id="8a912-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="8a912-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a912-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a912-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a912-105">DESCRIPTION</span></span>
<span data-ttu-id="8a912-106">Das Cmdlet **New-AzFirewallApplicationRuleCollection** erstellt eine Sammlung von Firewall-Anwendungsregeln.</span><span class="sxs-lookup"><span data-stu-id="8a912-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="8a912-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a912-107">EXAMPLES</span></span>

### <span data-ttu-id="8a912-108">Beispiel 1: Erstellen einer Sammlung mit einer Regel</span><span class="sxs-lookup"><span data-stu-id="8a912-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="8a912-109">In diesem Beispiel wird eine Sammlung mit einer Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a912-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="8a912-110">Der gesamte Datenverkehr, der den in $Rule 1 angegebenen Bedingungen entspricht, ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="8a912-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="8a912-111">Die erste Regel gilt für den gesamten HTTPS-Datenverkehr auf Port 443 von 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="8a912-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="8a912-112">Wenn es eine andere Anwendung Regelsammlung mit höherer Priorität (kleinerer Zahl) gibt, die auch dem in $Rule 1 angegebenen Datenverkehr entspricht, wird stattdessen die Aktion der Regelsammlung mit höherer Priorität wirksam.</span><span class="sxs-lookup"><span data-stu-id="8a912-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="8a912-113">Beispiel 2: Hinzufügen einer Regel zu einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="8a912-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="8a912-114">In diesem Beispiel wird eine neue Anwendungsregel Sammlung mit einer Regel erstellt und dann der Regelsammlung mithilfe der AddRule-Methode für das Rule Collection-Objekt eine zweite Regel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8a912-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="8a912-115">Jeder Regelname in einer bestimmten Regelsammlung muss einen eindeutigen Namen haben und die Groß-/Kleinschreibung wird nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="8a912-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="8a912-116">Beispiel 3: Abrufen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="8a912-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="8a912-117">In diesem Beispiel wird eine neue Anwendungsregel Sammlung mit einer Regel erstellt, und dann wird die Regel nach Namen abgerufen, und die GetRuleByName-Methode wird für das Rule Collection-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8a912-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="8a912-118">Der Regelname für Methoden-GetRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="8a912-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="8a912-119">Beispiel 4: Entfernen einer Regel aus einer Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="8a912-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="8a912-120">In diesem Beispiel wird eine neue Anwendungsregel Sammlung mit zwei Regeln erstellt, und dann wird die erste Regel aus der Regelsammlung entfernt, indem die Methode RemoveRuleByName für das Rule Collection-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8a912-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="8a912-121">Der Regelname für Methoden-RemoveRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="8a912-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="8a912-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a912-122">PARAMETERS</span></span>

### <span data-ttu-id="8a912-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="8a912-123">-ActionType</span></span>
<span data-ttu-id="8a912-124">Die Aktion der Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="8a912-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="8a912-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a912-125">-DefaultProfile</span></span>
<span data-ttu-id="8a912-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a912-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a912-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8a912-127">-Name</span></span>
<span data-ttu-id="8a912-128">Gibt den Namen dieser Anwendungsregel an.</span><span class="sxs-lookup"><span data-stu-id="8a912-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="8a912-129">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8a912-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="8a912-130">-Priorität</span><span class="sxs-lookup"><span data-stu-id="8a912-130">-Priority</span></span>
<span data-ttu-id="8a912-131">Gibt die Priorität dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="8a912-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="8a912-132">Priority ist eine Zahl zwischen 100 und 65000.</span><span class="sxs-lookup"><span data-stu-id="8a912-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="8a912-133">Je kleiner die Zahl, desto größer die Priorität.</span><span class="sxs-lookup"><span data-stu-id="8a912-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="8a912-134">-Rule</span><span class="sxs-lookup"><span data-stu-id="8a912-134">-Rule</span></span>
<span data-ttu-id="8a912-135">Gibt die Liste der Regeln an, die unter dieser Sammlung gruppiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a912-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a912-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a912-136">-Confirm</span></span>
<span data-ttu-id="8a912-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a912-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a912-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a912-138">-WhatIf</span></span>
<span data-ttu-id="8a912-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a912-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a912-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a912-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a912-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a912-141">CommonParameters</span></span>
<span data-ttu-id="8a912-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a912-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a912-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a912-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a912-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a912-144">INPUTS</span></span>

### <span data-ttu-id="8a912-145">Keine</span><span class="sxs-lookup"><span data-stu-id="8a912-145">None</span></span>

## <span data-ttu-id="8a912-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a912-146">OUTPUTS</span></span>

### <span data-ttu-id="8a912-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8a912-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="8a912-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a912-148">NOTES</span></span>

## <span data-ttu-id="8a912-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a912-149">RELATED LINKS</span></span>

[<span data-ttu-id="8a912-150">Neu – AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="8a912-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="8a912-151">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8a912-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="8a912-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8a912-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
