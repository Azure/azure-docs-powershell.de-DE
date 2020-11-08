---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166286"
---
# <span data-ttu-id="a8e2a-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8e2a-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="a8e2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e2a-103">Erstellt eine URL-Konfiguration für eine Rewrite-Regel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a8e2a-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="a8e2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8e2a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8e2a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8e2a-105">DESCRIPTION</span></span>
<span data-ttu-id="a8e2a-106">**Das AzApplicationGatewayRewriteRuleUrlConfiguration** -Cmdlet erstellt eine URL-Konfiguration für die Rewrite-Regel für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="a8e2a-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a8e2a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8e2a-107">EXAMPLES</span></span>

### <span data-ttu-id="a8e2a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8e2a-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="a8e2a-109">Mit diesem Befehl wird eine URL-Konfiguration für die Rewrite-Regel erstellt und das Ergebnis in der Variablen mit dem Namen $urlConfiguration gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a8e2a-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="a8e2a-110">Wenn Sie vorhandene UrlConfiguration aktualisieren möchten, können Sie dies tun, indem Sie ein neues UrlConfiguration-Element erstellen und der UrlConfiguration-Eigenschaft des Regel Aktions Satzes erneut schreiben den neuen UrlConfiguration zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a8e2a-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="a8e2a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8e2a-111">PARAMETERS</span></span>

### <span data-ttu-id="a8e2a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e2a-112">-DefaultProfile</span></span>
<span data-ttu-id="a8e2a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8e2a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8e2a-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="a8e2a-114">-ModifiedPath</span></span>
<span data-ttu-id="a8e2a-115">URL-Pfadwert.</span><span class="sxs-lookup"><span data-stu-id="a8e2a-115">Url path value.</span></span>

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

### <span data-ttu-id="a8e2a-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="a8e2a-116">-ModifiedQueryString</span></span>
<span data-ttu-id="a8e2a-117">URL-Abfragezeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="a8e2a-117">Url query string value.</span></span>

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

### <span data-ttu-id="a8e2a-118">-Umleiten</span><span class="sxs-lookup"><span data-stu-id="a8e2a-118">-Reroute</span></span>
<span data-ttu-id="a8e2a-119">Flag zum erneuten Auswerten der URL-Pfadzuordnung, die in pfadbasierten Anforderungs Routingregeln mithilfe des geänderten Pfads bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a8e2a-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="a8e2a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e2a-120">CommonParameters</span></span>
<span data-ttu-id="a8e2a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8e2a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e2a-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8e2a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e2a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8e2a-123">INPUTS</span></span>

### <span data-ttu-id="a8e2a-124">Keine</span><span class="sxs-lookup"><span data-stu-id="a8e2a-124">None</span></span>

## <span data-ttu-id="a8e2a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8e2a-125">OUTPUTS</span></span>

### <span data-ttu-id="a8e2a-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8e2a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="a8e2a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8e2a-127">NOTES</span></span>

## <span data-ttu-id="a8e2a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8e2a-128">RELATED LINKS</span></span>

[<span data-ttu-id="a8e2a-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8e2a-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a8e2a-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8e2a-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a8e2a-131">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8e2a-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a8e2a-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8e2a-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a8e2a-133">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8e2a-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a8e2a-134">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a8e2a-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a8e2a-135">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a8e2a-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)