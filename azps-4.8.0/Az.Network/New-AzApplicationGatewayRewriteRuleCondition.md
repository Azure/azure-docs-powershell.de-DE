---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009121"
---
# <span data-ttu-id="7b626-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="7b626-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="7b626-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b626-102">SYNOPSIS</span></span>
<span data-ttu-id="7b626-103">Fügt dem RewriteRule für ein Anwendungsgateway eine Bedingung hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b626-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="7b626-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b626-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b626-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b626-105">DESCRIPTION</span></span>
<span data-ttu-id="7b626-106">**Das AzApplicationGatewayRewriteRuleCondition** -Cmdlet erstellt eine Rewrite-Regelbedingung für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="7b626-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="7b626-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b626-107">EXAMPLES</span></span>

### <span data-ttu-id="7b626-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7b626-108">Example 1</span></span>
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
<span data-ttu-id="7b626-109">Dieser Befehl erstellt eine Bedingung in einer Rewrite-Regel und speichert das Ergebnis in der Variablen mit dem Namen $Condition.</span><span class="sxs-lookup"><span data-stu-id="7b626-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="7b626-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b626-110">PARAMETERS</span></span>

### <span data-ttu-id="7b626-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b626-111">-DefaultProfile</span></span>
<span data-ttu-id="7b626-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b626-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b626-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="7b626-113">-IgnoreCase</span></span>
<span data-ttu-id="7b626-114">Dieses Flag so einstellen, dass Groß-/Kleinschreibung auf dem Muster ignoriert wird</span><span class="sxs-lookup"><span data-stu-id="7b626-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="7b626-115">-Negieren</span><span class="sxs-lookup"><span data-stu-id="7b626-115">-Negate</span></span>
<span data-ttu-id="7b626-116">Setzen Sie dieses Flag, um die Bedingungsüberprüfung zu negieren</span><span class="sxs-lookup"><span data-stu-id="7b626-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="7b626-117">-Muster</span><span class="sxs-lookup"><span data-stu-id="7b626-117">-Pattern</span></span>
<span data-ttu-id="7b626-118">Muster, nach dem in der Variablen Kopfzeile gesucht werden soll</span><span class="sxs-lookup"><span data-stu-id="7b626-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="7b626-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="7b626-119">-Variable</span></span>
<span data-ttu-id="7b626-120">Name der Kopfzeile, auf die die Bedingung gesetzt werden soll</span><span class="sxs-lookup"><span data-stu-id="7b626-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="7b626-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b626-121">CommonParameters</span></span>
<span data-ttu-id="7b626-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b626-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7b626-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b626-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b626-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b626-124">INPUTS</span></span>

### <span data-ttu-id="7b626-125">Keine</span><span class="sxs-lookup"><span data-stu-id="7b626-125">None</span></span>

## <span data-ttu-id="7b626-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b626-126">OUTPUTS</span></span>

### <span data-ttu-id="7b626-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="7b626-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="7b626-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b626-128">NOTES</span></span>

## <span data-ttu-id="7b626-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b626-129">RELATED LINKS</span></span>
[<span data-ttu-id="7b626-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b626-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7b626-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b626-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7b626-132">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b626-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7b626-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b626-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7b626-134">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b626-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7b626-135">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7b626-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="7b626-136">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7b626-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
