---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467351"
---
# <span data-ttu-id="40b60-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="40b60-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="40b60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b60-102">SYNOPSIS</span></span>
<span data-ttu-id="40b60-103">Erstellt einen Ausschluss der Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="40b60-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="40b60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40b60-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40b60-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40b60-105">DESCRIPTION</span></span>
<span data-ttu-id="40b60-106">Das **Cmdlet "New-AzApplicationGatewayFirewallPolicyExclusion"** enthält eine neue Ausschlussregelliste für die Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="40b60-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="40b60-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40b60-107">EXAMPLES</span></span>

### <span data-ttu-id="40b60-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40b60-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="40b60-109">Mit diesem Befehl wird ein neuer Ausschlusseintrag für die Variable "RequestHeaderNames" und den Operator "StartsWith" und die Auswahl namens xyz erstellt.</span><span class="sxs-lookup"><span data-stu-id="40b60-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="40b60-110">Der Ausschlusseintrag wird im $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="40b60-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="40b60-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40b60-111">PARAMETERS</span></span>

### <span data-ttu-id="40b60-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b60-112">-DefaultProfile</span></span>
<span data-ttu-id="40b60-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40b60-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b60-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="40b60-114">-MatchVariable</span></span>
<span data-ttu-id="40b60-115">Die auszuschließende Variable.</span><span class="sxs-lookup"><span data-stu-id="40b60-115">The variable to be excluded.</span></span>

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

### <span data-ttu-id="40b60-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="40b60-116">-Selector</span></span>
<span data-ttu-id="40b60-117">Wenn "Variable" eine Sammlung ist, wird der Operator verwendet, um anzugeben, für welche Elemente in der Sammlung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="40b60-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="40b60-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="40b60-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="40b60-119">Wenn eine Variable eine Sammlung ist, verwenden Sie den Selektor, um anzugeben, für welche Elemente in der Sammlung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="40b60-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="40b60-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b60-120">CommonParameters</span></span>
<span data-ttu-id="40b60-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b60-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b60-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40b60-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b60-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40b60-123">INPUTS</span></span>

### <span data-ttu-id="40b60-124">Keine</span><span class="sxs-lookup"><span data-stu-id="40b60-124">None</span></span>

## <span data-ttu-id="40b60-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40b60-125">OUTPUTS</span></span>

### <span data-ttu-id="40b60-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExklion</span><span class="sxs-lookup"><span data-stu-id="40b60-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="40b60-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40b60-127">NOTES</span></span>

## <span data-ttu-id="40b60-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40b60-128">RELATED LINKS</span></span>
