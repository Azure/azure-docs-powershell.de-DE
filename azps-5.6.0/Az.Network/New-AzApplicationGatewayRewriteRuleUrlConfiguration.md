---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: e9b0b8cdbee1e4d5c488e51f537d18cca2ef681a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918707"
---
# <span data-ttu-id="8f496-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f496-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="8f496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f496-102">SYNOPSIS</span></span>
<span data-ttu-id="8f496-103">Erstellt eine Neuschreibregel-URL-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8f496-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="8f496-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f496-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f496-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f496-105">DESCRIPTION</span></span>
<span data-ttu-id="8f496-106">**Das AzApplicationGatewayRewriteRuleUrlConfiguration-Cmdlet** erstellt eine Neuschreibregel-URL-Konfiguration für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8f496-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="8f496-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f496-107">EXAMPLES</span></span>

### <span data-ttu-id="8f496-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f496-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="8f496-109">Mit diesem Befehl wird eine Neuschreibregel-URL-Konfiguration erstellt und das Ergebnis in der Variablen namens $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8f496-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="8f496-110">Wenn Sie eine vorhandene UrlConfiguration aktualisieren möchten, können Sie dazu eine neue UrlConfiguration erstellen und die neue UrlConfiguration der UrlConfiguration-Eigenschaft des Aktionssets "Regel neu schreiben" zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8f496-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="8f496-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8f496-111">PARAMETERS</span></span>

### <span data-ttu-id="8f496-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f496-112">-DefaultProfile</span></span>
<span data-ttu-id="8f496-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f496-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f496-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="8f496-114">-ModifiedPath</span></span>
<span data-ttu-id="8f496-115">Urlpfadwert.</span><span class="sxs-lookup"><span data-stu-id="8f496-115">Url path value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f496-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="8f496-116">-ModifiedQueryString</span></span>
<span data-ttu-id="8f496-117">Urlabfragezeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="8f496-117">Url query string value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f496-118">-Umleiten</span><span class="sxs-lookup"><span data-stu-id="8f496-118">-Reroute</span></span>
<span data-ttu-id="8f496-119">Kennzeichnen Sie, um die url path map erneut auszuwerten, die in pfadbasierten Anforderungsroutingregeln mit geändertem Pfad bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8f496-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f496-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f496-120">CommonParameters</span></span>
<span data-ttu-id="8f496-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f496-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f496-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f496-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f496-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f496-123">INPUTS</span></span>

### <span data-ttu-id="8f496-124">Keine</span><span class="sxs-lookup"><span data-stu-id="8f496-124">None</span></span>

## <span data-ttu-id="8f496-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f496-125">OUTPUTS</span></span>

### <span data-ttu-id="8f496-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f496-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="8f496-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8f496-127">NOTES</span></span>

## <span data-ttu-id="8f496-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8f496-128">RELATED LINKS</span></span>

[<span data-ttu-id="8f496-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8f496-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8f496-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8f496-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8f496-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8f496-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8f496-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8f496-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8f496-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8f496-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8f496-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8f496-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="8f496-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8f496-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)