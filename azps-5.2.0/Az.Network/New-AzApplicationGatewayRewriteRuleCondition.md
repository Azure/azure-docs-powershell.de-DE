---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358195"
---
# <span data-ttu-id="461e7-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="461e7-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="461e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="461e7-102">SYNOPSIS</span></span>
<span data-ttu-id="461e7-103">Fügt der Neuschreibung für ein Anwendungsgateway eine Bedingung hinzu.</span><span class="sxs-lookup"><span data-stu-id="461e7-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="461e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="461e7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="461e7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="461e7-105">DESCRIPTION</span></span>
<span data-ttu-id="461e7-106">**Das Cmdlet "AzApplicationGatewayRewriteRuleCondition"** erstellt eine Neuschreibregelbedingung für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="461e7-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="461e7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="461e7-107">EXAMPLES</span></span>

### <span data-ttu-id="461e7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="461e7-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="461e7-109">Dieser Befehl erstellt eine Bedingung in einer Neuschreibungsregel und speichert das Ergebnis in der Variablen namens $condition.</span><span class="sxs-lookup"><span data-stu-id="461e7-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="461e7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="461e7-110">PARAMETERS</span></span>

### <span data-ttu-id="461e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461e7-111">-DefaultProfile</span></span>
<span data-ttu-id="461e7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="461e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="461e7-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="461e7-113">-IgnoreCase</span></span>
<span data-ttu-id="461e7-114">Dieses Kennzeichen so festlegen, dass die Hülle des Musters ignoriert wird</span><span class="sxs-lookup"><span data-stu-id="461e7-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461e7-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="461e7-115">-Negate</span></span>
<span data-ttu-id="461e7-116">Dieses Kennzeichen festlegen, um die Bedingungsprüfung zu negieren</span><span class="sxs-lookup"><span data-stu-id="461e7-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461e7-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="461e7-117">-Pattern</span></span>
<span data-ttu-id="461e7-118">Muster, nach dem im Variablenkopf zu suchen ist</span><span class="sxs-lookup"><span data-stu-id="461e7-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461e7-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="461e7-119">-Variable</span></span>
<span data-ttu-id="461e7-120">Name der Kopfzeile, deren Bedingung festgelegt werden soll</span><span class="sxs-lookup"><span data-stu-id="461e7-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="461e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461e7-121">CommonParameters</span></span>
<span data-ttu-id="461e7-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="461e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="461e7-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="461e7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461e7-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="461e7-124">INPUTS</span></span>

### <span data-ttu-id="461e7-125">Keine</span><span class="sxs-lookup"><span data-stu-id="461e7-125">None</span></span>

## <span data-ttu-id="461e7-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="461e7-126">OUTPUTS</span></span>

### <span data-ttu-id="461e7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="461e7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="461e7-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="461e7-128">NOTES</span></span>

## <span data-ttu-id="461e7-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="461e7-129">RELATED LINKS</span></span>
[<span data-ttu-id="461e7-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="461e7-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="461e7-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="461e7-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="461e7-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="461e7-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="461e7-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="461e7-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="461e7-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="461e7-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="461e7-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="461e7-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="461e7-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="461e7-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
