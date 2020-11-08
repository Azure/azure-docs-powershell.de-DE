---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165235"
---
# <span data-ttu-id="40376-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="40376-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="40376-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40376-102">SYNOPSIS</span></span>
<span data-ttu-id="40376-103">Erstellt eine neue benutzerdefinierte Regel für die Firewall-Richtlinie des Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="40376-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="40376-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40376-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40376-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40376-105">DESCRIPTION</span></span>
<span data-ttu-id="40376-106">Mit der **neuen AzApplicationGatewayFirewallCustomRule** wird eine benutzerdefinierte Regel für die Firewall-Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="40376-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="40376-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40376-107">EXAMPLES</span></span>

### <span data-ttu-id="40376-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40376-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="40376-109">Der Befehl erstellt eine neue benutzerdefinierte Regel mit dem Namen Beispiel-Regel, Priorität 1 und dem Regeltyp wird MatchRule mit einer Bedingung, die in der Bedingungsvariablen definiert ist, wird die Aktion den Allow.</span><span class="sxs-lookup"><span data-stu-id="40376-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="40376-110">Die neue benutzerdefinierte Übereinstimmungsregel wird in $CustomRule gespeichert.</span><span class="sxs-lookup"><span data-stu-id="40376-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="40376-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="40376-111">PARAMETERS</span></span>

### <span data-ttu-id="40376-112">– Aktion</span><span class="sxs-lookup"><span data-stu-id="40376-112">-Action</span></span>
<span data-ttu-id="40376-113">Art der Aktionen.</span><span class="sxs-lookup"><span data-stu-id="40376-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40376-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40376-114">-DefaultProfile</span></span>
<span data-ttu-id="40376-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="40376-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40376-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="40376-116">-MatchCondition</span></span>
<span data-ttu-id="40376-117">Liste der Übereinstimmungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="40376-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40376-118">-Name</span><span class="sxs-lookup"><span data-stu-id="40376-118">-Name</span></span>
<span data-ttu-id="40376-119">Der Name der Regel.</span><span class="sxs-lookup"><span data-stu-id="40376-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="40376-120">-Priorität</span><span class="sxs-lookup"><span data-stu-id="40376-120">-Priority</span></span>
<span data-ttu-id="40376-121">Beschreibt die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="40376-121">Describes priority of the rule.</span></span>
<span data-ttu-id="40376-122">Regeln mit einem niedrigeren Wert werden vor Regeln mit einem höheren Wert ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="40376-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40376-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="40376-123">-RuleType</span></span>
<span data-ttu-id="40376-124">Beschreibt den Typ der Regel.</span><span class="sxs-lookup"><span data-stu-id="40376-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40376-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40376-125">CommonParameters</span></span>
<span data-ttu-id="40376-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40376-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40376-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40376-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40376-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40376-128">INPUTS</span></span>

### <span data-ttu-id="40376-129">Keine</span><span class="sxs-lookup"><span data-stu-id="40376-129">None</span></span>

## <span data-ttu-id="40376-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40376-130">OUTPUTS</span></span>

### <span data-ttu-id="40376-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="40376-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="40376-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="40376-132">NOTES</span></span>

## <span data-ttu-id="40376-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40376-133">RELATED LINKS</span></span>
