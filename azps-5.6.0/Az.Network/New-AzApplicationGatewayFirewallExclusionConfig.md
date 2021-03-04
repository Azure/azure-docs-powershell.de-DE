---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 029ba60169ee22d86d9e54661296f04bf2242713
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924715"
---
# <span data-ttu-id="b5efc-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="b5efc-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="b5efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5efc-102">SYNOPSIS</span></span>
<span data-ttu-id="b5efc-103">Erstellt eine neue Ausschlussregelliste für Anwendungsgateway waf</span><span class="sxs-lookup"><span data-stu-id="b5efc-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="b5efc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5efc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5efc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5efc-105">DESCRIPTION</span></span>
<span data-ttu-id="b5efc-106">Das **Cmdlet New-AzApplicationGatewayFirewallExclusionConfig** führt eine neue Ausschlussregelliste für das Anwendungsgateway waf aus.</span><span class="sxs-lookup"><span data-stu-id="b5efc-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="b5efc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5efc-107">EXAMPLES</span></span>

### <span data-ttu-id="b5efc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b5efc-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="b5efc-109">Mit diesem Befehl wird eine neue Ausschlussregel erstellt, in der die Konfiguration für die Variable "RequestHeaderNames" und der Operator "StartsWith" und "Selector" mit dem Namen xyz aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5efc-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="b5efc-110">Die Konfiguration der Ausschlussliste wird in $exclusion 1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b5efc-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="b5efc-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b5efc-111">PARAMETERS</span></span>

### <span data-ttu-id="b5efc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5efc-112">-DefaultProfile</span></span>
<span data-ttu-id="b5efc-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5efc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5efc-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="b5efc-114">-Operator</span></span>
<span data-ttu-id="b5efc-115">Wenn Variable eine Sammlung ist, verwenden Sie die Auswahl, um anzugeben, für welche Elemente in der Auflistung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="b5efc-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="b5efc-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="b5efc-116">-Selector</span></span>
<span data-ttu-id="b5efc-117">Wenn Variable eine Auflistung ist, wird der Operator verwendet, um anzugeben, für welche Elemente in der Auflistung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="b5efc-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="b5efc-118">-Variable</span><span class="sxs-lookup"><span data-stu-id="b5efc-118">-Variable</span></span>
<span data-ttu-id="b5efc-119">Die auszuschließende Variable.</span><span class="sxs-lookup"><span data-stu-id="b5efc-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="b5efc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5efc-120">CommonParameters</span></span>
<span data-ttu-id="b5efc-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5efc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5efc-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5efc-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5efc-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5efc-123">INPUTS</span></span>

### <span data-ttu-id="b5efc-124">Keine</span><span class="sxs-lookup"><span data-stu-id="b5efc-124">None</span></span>

## <span data-ttu-id="b5efc-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5efc-125">OUTPUTS</span></span>

### <span data-ttu-id="b5efc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="b5efc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="b5efc-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b5efc-127">NOTES</span></span>

## <span data-ttu-id="b5efc-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b5efc-128">RELATED LINKS</span></span>
