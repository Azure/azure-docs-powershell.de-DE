---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379320"
---
# <span data-ttu-id="a24fa-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a24fa-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="a24fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a24fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a24fa-103">Erstellt eine Neuschreibung der Regel-URL-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a24fa-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="a24fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a24fa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a24fa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a24fa-105">DESCRIPTION</span></span>
<span data-ttu-id="a24fa-106">**Das Cmdlet "AzApplicationGatewayRewriteRuleUrlConfiguration"** erstellt eine Neuschreibung der Regel-URL-Konfiguration für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a24fa-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a24fa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a24fa-107">EXAMPLES</span></span>

### <span data-ttu-id="a24fa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a24fa-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="a24fa-109">Dieser Befehl erstellt eine Neuschreibung der Regel-URL-Konfiguration und speichert das Ergebnis in der Variablen namens $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a24fa-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="a24fa-110">Wenn Sie eine vorhandene UrlConfiguration aktualisieren möchten, können Sie dies tun, indem Sie eine neue UrlConfiguration erstellen und die neue "UrlConfiguration" der Eigenschaft "UrlConfiguration" des Aktionssets "Regel neu schreiben" zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a24fa-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="a24fa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a24fa-111">PARAMETERS</span></span>

### <span data-ttu-id="a24fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24fa-112">-DefaultProfile</span></span>
<span data-ttu-id="a24fa-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a24fa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a24fa-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="a24fa-114">-ModifiedPath</span></span>
<span data-ttu-id="a24fa-115">URL path value.</span><span class="sxs-lookup"><span data-stu-id="a24fa-115">Url path value.</span></span>

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

### <span data-ttu-id="a24fa-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="a24fa-116">-ModifiedQueryString</span></span>
<span data-ttu-id="a24fa-117">Wert der URL-Abfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a24fa-117">Url query string value.</span></span>

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

### <span data-ttu-id="a24fa-118">-Reroute</span><span class="sxs-lookup"><span data-stu-id="a24fa-118">-Reroute</span></span>
<span data-ttu-id="a24fa-119">Flag zum erneuten Auswerten der URL-Pfadzuordnung, die in pfadbasierten Anforderungsroutingregeln unter Verwendung des geänderten Pfads bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a24fa-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="a24fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24fa-120">CommonParameters</span></span>
<span data-ttu-id="a24fa-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24fa-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a24fa-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24fa-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a24fa-123">INPUTS</span></span>

### <span data-ttu-id="a24fa-124">Keine</span><span class="sxs-lookup"><span data-stu-id="a24fa-124">None</span></span>

## <span data-ttu-id="a24fa-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a24fa-125">OUTPUTS</span></span>

### <span data-ttu-id="a24fa-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a24fa-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="a24fa-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a24fa-127">NOTES</span></span>

## <span data-ttu-id="a24fa-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a24fa-128">RELATED LINKS</span></span>

[<span data-ttu-id="a24fa-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a24fa-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a24fa-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a24fa-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a24fa-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a24fa-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a24fa-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a24fa-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a24fa-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a24fa-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a24fa-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a24fa-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a24fa-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a24fa-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)