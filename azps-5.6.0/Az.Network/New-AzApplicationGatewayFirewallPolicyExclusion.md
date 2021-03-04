---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: 04cf39f9c0d8774ffb02688e4edf5804029df669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930011"
---
# <span data-ttu-id="c88f7-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="c88f7-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="c88f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c88f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c88f7-103">Erstellt einen Ausschluss für die Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c88f7-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="c88f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c88f7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c88f7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c88f7-105">DESCRIPTION</span></span>
<span data-ttu-id="c88f7-106">Das **Cmdlet New-AzApplicationGatewayFirewallPolicyExclusion** führt eine neue Ausschlussregelliste für eine Firewallrichtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="c88f7-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="c88f7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c88f7-107">EXAMPLES</span></span>

### <span data-ttu-id="c88f7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c88f7-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="c88f7-109">Mit diesem Befehl wird ein neuer Ausschlusseintrag für die Variable "RequestHeaderNames" und den Operator "StartsWith" und "Selector" mit dem Namen xyz erstellt.</span><span class="sxs-lookup"><span data-stu-id="c88f7-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="c88f7-110">Der Ausschlusseintrag wird in $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="c88f7-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="c88f7-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c88f7-111">PARAMETERS</span></span>

### <span data-ttu-id="c88f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88f7-112">-DefaultProfile</span></span>
<span data-ttu-id="c88f7-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c88f7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c88f7-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="c88f7-114">-MatchVariable</span></span>
<span data-ttu-id="c88f7-115">Die auszuschließende Variable.</span><span class="sxs-lookup"><span data-stu-id="c88f7-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88f7-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="c88f7-116">-Selector</span></span>
<span data-ttu-id="c88f7-117">Wenn Variable eine Auflistung ist, wird der Operator verwendet, um anzugeben, für welche Elemente in der Auflistung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="c88f7-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="c88f7-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="c88f7-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="c88f7-119">Wenn Variable eine Sammlung ist, verwenden Sie die Auswahl, um anzugeben, für welche Elemente in der Auflistung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="c88f7-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88f7-120">CommonParameters</span></span>
<span data-ttu-id="c88f7-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c88f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88f7-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c88f7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88f7-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c88f7-123">INPUTS</span></span>

### <span data-ttu-id="c88f7-124">Keine</span><span class="sxs-lookup"><span data-stu-id="c88f7-124">None</span></span>

## <span data-ttu-id="c88f7-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c88f7-125">OUTPUTS</span></span>

### <span data-ttu-id="c88f7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="c88f7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="c88f7-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c88f7-127">NOTES</span></span>

## <span data-ttu-id="c88f7-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c88f7-128">RELATED LINKS</span></span>
