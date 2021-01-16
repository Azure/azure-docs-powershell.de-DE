---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299272"
---
# <span data-ttu-id="fb738-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fb738-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="fb738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb738-102">SYNOPSIS</span></span>
<span data-ttu-id="fb738-103">Erstellen einer neuen Nat-Regelsammlung für die Azure-Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fb738-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="fb738-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb738-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb738-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb738-105">DESCRIPTION</span></span>
<span data-ttu-id="fb738-106">Das **Cmdlet "New-AzFirewallPolicyNatRuleCollection"** erstellt eine Nat-Regelsammlung für eine Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="fb738-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="fb738-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fb738-107">EXAMPLES</span></span>

### <span data-ttu-id="fb738-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fb738-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="fb738-109">In diesem Beispiel wird eine Nat-Regel-Auflistung mit einer Netzwerkregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="fb738-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="fb738-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb738-110">PARAMETERS</span></span>

### <span data-ttu-id="fb738-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="fb738-111">-ActionType</span></span>
<span data-ttu-id="fb738-112">Der Typ der Regelaktion</span><span class="sxs-lookup"><span data-stu-id="fb738-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb738-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb738-113">-DefaultProfile</span></span>
<span data-ttu-id="fb738-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb738-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb738-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fb738-115">-Name</span></span>
<span data-ttu-id="fb738-116">Der Name der Netzwerkregelsammlung</span><span class="sxs-lookup"><span data-stu-id="fb738-116">The name of the Network Rule Collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb738-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="fb738-117">-Priority</span></span>
<span data-ttu-id="fb738-118">Die Priorität der Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="fb738-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb738-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="fb738-119">-Rule</span></span>
<span data-ttu-id="fb738-120">Liste der Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="fb738-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb738-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="fb738-121">-TranslatedAddress</span></span>
<span data-ttu-id="fb738-122">Die übersetzte Adresse für diese NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="fb738-122">The translated address for this NAT rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb738-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="fb738-123">-TranslatedPort</span></span>
<span data-ttu-id="fb738-124">Der übersetzte Port für diese NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="fb738-124">The translated port for this NAT rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb738-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb738-125">-Confirm</span></span>
<span data-ttu-id="fb738-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb738-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb738-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fb738-127">-WhatIf</span></span>
<span data-ttu-id="fb738-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb738-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb738-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb738-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb738-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb738-130">CommonParameters</span></span>
<span data-ttu-id="fb738-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb738-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb738-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb738-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb738-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fb738-133">INPUTS</span></span>

### <span data-ttu-id="fb738-134">Keine</span><span class="sxs-lookup"><span data-stu-id="fb738-134">None</span></span>

## <span data-ttu-id="fb738-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fb738-135">OUTPUTS</span></span>

### <span data-ttu-id="fb738-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fb738-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="fb738-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fb738-137">NOTES</span></span>

## <span data-ttu-id="fb738-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fb738-138">RELATED LINKS</span></span>
