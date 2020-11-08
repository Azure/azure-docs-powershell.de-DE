---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174601"
---
# <span data-ttu-id="4035c-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4035c-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="4035c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4035c-102">SYNOPSIS</span></span>
<span data-ttu-id="4035c-103">Erstellt einen Ausschluss für die Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4035c-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="4035c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4035c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4035c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4035c-105">DESCRIPTION</span></span>
<span data-ttu-id="4035c-106">Das Cmdlet " **New-AzApplicationGatewayFirewallPolicyExclusion** " eine neue Ausschlussregel Liste für die Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4035c-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="4035c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4035c-107">EXAMPLES</span></span>

### <span data-ttu-id="4035c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4035c-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="4035c-109">Dieser Befehl erstellt einen neuen ausschlusseintrag für die Variable mit dem Namen RequestHeaderNames und dem Operator mit dem Namen StartsWith und Selector mit dem Namen XYZ.</span><span class="sxs-lookup"><span data-stu-id="4035c-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="4035c-110">Der ausschlusseintrag wird in $exclusionEntry gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4035c-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="4035c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4035c-111">PARAMETERS</span></span>

### <span data-ttu-id="4035c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4035c-112">-DefaultProfile</span></span>
<span data-ttu-id="4035c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4035c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4035c-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="4035c-114">-MatchVariable</span></span>
<span data-ttu-id="4035c-115">Die Variable, die ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4035c-115">The variable to be excluded.</span></span>

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

### <span data-ttu-id="4035c-116">-Auswahl</span><span class="sxs-lookup"><span data-stu-id="4035c-116">-Selector</span></span>
<span data-ttu-id="4035c-117">Wenn Variable eine Auflistung ist, wird mit dem Operator angegeben, für welche Elemente in der Sammlung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="4035c-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="4035c-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="4035c-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="4035c-119">Wenn Variable eine Sammlung ist, verwenden Sie die Auswahl, um anzugeben, für welche Elemente in der Sammlung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="4035c-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="4035c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4035c-120">CommonParameters</span></span>
<span data-ttu-id="4035c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4035c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4035c-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4035c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4035c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4035c-123">INPUTS</span></span>

### <span data-ttu-id="4035c-124">Keine</span><span class="sxs-lookup"><span data-stu-id="4035c-124">None</span></span>

## <span data-ttu-id="4035c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4035c-125">OUTPUTS</span></span>

### <span data-ttu-id="4035c-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4035c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="4035c-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="4035c-127">NOTES</span></span>

## <span data-ttu-id="4035c-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4035c-128">RELATED LINKS</span></span>
