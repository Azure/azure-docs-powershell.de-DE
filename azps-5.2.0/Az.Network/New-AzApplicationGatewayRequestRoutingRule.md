---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95f3e4b11d9253a232fc119faf39a4fa51fab60a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358237"
---
# <span data-ttu-id="00ae5-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="00ae5-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="00ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="00ae5-103">Erstellt eine Anforderungsroutingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="00ae5-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="00ae5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00ae5-104">SYNTAX</span></span>

### <span data-ttu-id="00ae5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="00ae5-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00ae5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="00ae5-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ae5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00ae5-107">DESCRIPTION</span></span>
<span data-ttu-id="00ae5-108">**Das Cmdlet "Add-AzApplicationGatewayRequestRoutingRule"** erstellt eine Anforderungsroutingregel für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="00ae5-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="00ae5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00ae5-109">EXAMPLES</span></span>

### <span data-ttu-id="00ae5-110">Beispiel 1: Erstellen einer Anforderungsroutingregel für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="00ae5-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="00ae5-111">Dieser Befehl erstellt eine einfache Anforderungsroutingregel namens "Regel01" und speichert das Ergebnis in der Variablen namens $Rule.</span><span class="sxs-lookup"><span data-stu-id="00ae5-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="00ae5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00ae5-112">PARAMETERS</span></span>

### <span data-ttu-id="00ae5-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="00ae5-113">-BackendAddressPool</span></span>
<span data-ttu-id="00ae5-114">Gibt den Back-End-Adresspool als Objekt an, der von der Anforderungsroutingregel erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00ae5-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-115">-Back-EndAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="00ae5-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="00ae5-116">Gibt die Back-End-Adresspool-ID der zu erstellenden Anforderungsroutingregel an.</span><span class="sxs-lookup"><span data-stu-id="00ae5-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-117">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00ae5-117">-BackendHttpSettings</span></span>
<span data-ttu-id="00ae5-118">Gibt die Back-End-HTTP-Einstellungen als Objekt an, das von der Anforderungsroutingregel erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00ae5-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-119">-Back-EndHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="00ae5-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="00ae5-120">Gibt die Back-End-HTTP-Einstellungs-ID der zu erstellenden Anforderungsroutingregel an.</span><span class="sxs-lookup"><span data-stu-id="00ae5-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ae5-121">-DefaultProfile</span></span>
<span data-ttu-id="00ae5-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00ae5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00ae5-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="00ae5-123">-HttpListener</span></span>
<span data-ttu-id="00ae5-124">Gibt den Back-End-HTTP-Listener für die zu erstellende Anforderungsroutingregel an.</span><span class="sxs-lookup"><span data-stu-id="00ae5-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="00ae5-125">-HttpListenerId</span></span>
<span data-ttu-id="00ae5-126">Gibt die Back-End-HTTP-Listener-ID für die zu erstellende Anforderungsroutingregel an.</span><span class="sxs-lookup"><span data-stu-id="00ae5-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="00ae5-127">-Name</span></span>
<span data-ttu-id="00ae5-128">Gibt den Namen der Anforderungsroutingregel an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="00ae5-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="00ae5-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="00ae5-129">-Priority</span></span>
<span data-ttu-id="00ae5-130">Die Priorität der Regel</span><span class="sxs-lookup"><span data-stu-id="00ae5-130">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="00ae5-131">-RedirectConfiguration</span></span>
<span data-ttu-id="00ae5-132">Anwendungsgateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="00ae5-132">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="00ae5-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="00ae5-134">ID des Anwendungsgateways RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="00ae5-134">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00ae5-135">-RewriteRuleSet</span></span>
<span data-ttu-id="00ae5-136">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00ae5-136">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="00ae5-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="00ae5-138">ID des Anwendungsgateways "RewriteRuleSet"</span><span class="sxs-lookup"><span data-stu-id="00ae5-138">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="00ae5-139">-RuleType</span></span>
<span data-ttu-id="00ae5-140">Gibt den Typ der Anforderungsroutingregel an.</span><span class="sxs-lookup"><span data-stu-id="00ae5-140">Specifies type of the request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="00ae5-141">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="00ae5-142">-UrlPathMapId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ae5-143">CommonParameters</span></span>
<span data-ttu-id="00ae5-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ae5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ae5-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00ae5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ae5-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00ae5-146">INPUTS</span></span>

### <span data-ttu-id="00ae5-147">Keine</span><span class="sxs-lookup"><span data-stu-id="00ae5-147">None</span></span>

## <span data-ttu-id="00ae5-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00ae5-148">OUTPUTS</span></span>

### <span data-ttu-id="00ae5-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="00ae5-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="00ae5-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="00ae5-150">NOTES</span></span>

## <span data-ttu-id="00ae5-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="00ae5-151">RELATED LINKS</span></span>

[<span data-ttu-id="00ae5-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="00ae5-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="00ae5-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="00ae5-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="00ae5-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="00ae5-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="00ae5-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="00ae5-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


