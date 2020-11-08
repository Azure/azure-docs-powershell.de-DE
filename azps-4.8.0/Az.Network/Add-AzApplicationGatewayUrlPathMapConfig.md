---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175114"
---
# <span data-ttu-id="9835f-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9835f-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="9835f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9835f-102">SYNOPSIS</span></span>
<span data-ttu-id="9835f-103">Fügt einem Back-End-Serverpool ein Array von URL-Pfad Zuordnungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="9835f-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9835f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9835f-104">SYNTAX</span></span>

### <span data-ttu-id="9835f-105">BackendSetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9835f-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9835f-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9835f-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9835f-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="9835f-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9835f-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9835f-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9835f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9835f-109">DESCRIPTION</span></span>
<span data-ttu-id="9835f-110">Mit dem Cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** wird ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9835f-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="9835f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9835f-111">EXAMPLES</span></span>

### <span data-ttu-id="9835f-112">Beispiel 1: Hinzufügen einer URL-Pfadzuordnung zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="9835f-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="9835f-113">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen appGwName ab und speichert es in $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="9835f-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="9835f-114">Der zweite Befehl ruft den Back-End-Adresspool ab und speichert ihn in $Pool Variablen.</span><span class="sxs-lookup"><span data-stu-id="9835f-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="9835f-115">Der dritte Befehl ruft Back-End-HTTP-Einstellungen ab und speichert Sie in $poolSettings-Variable.</span><span class="sxs-lookup"><span data-stu-id="9835f-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="9835f-116">Der vierte Befehl erstellt eine neue Pfadregel mit dem Namen rule01 und speichert Sie in $pathRule Variablen.</span><span class="sxs-lookup"><span data-stu-id="9835f-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="9835f-117">Der fünfte Befehl fügt dem Anwendungsgateway URL-Pfad Zuordnungskonfiguration mit dem Namen url01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="9835f-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="9835f-118">Der sechste Befehl aktualisiert das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="9835f-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="9835f-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="9835f-119">PARAMETERS</span></span>

### <span data-ttu-id="9835f-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9835f-120">-ApplicationGateway</span></span>
<span data-ttu-id="9835f-121">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9835f-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9835f-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="9835f-123">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9835f-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9835f-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="9835f-125">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="9835f-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9835f-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="9835f-127">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9835f-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="9835f-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="9835f-129">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="9835f-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9835f-130">-DefaultProfile</span></span>
<span data-ttu-id="9835f-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9835f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9835f-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9835f-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="9835f-133">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9835f-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9835f-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="9835f-135">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9835f-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9835f-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="9835f-137">Standard Regelsatz für das Anwendungsgateway-Neuschreiben</span><span class="sxs-lookup"><span data-stu-id="9835f-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="9835f-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="9835f-139">ID des standardmäßigen Regelsatzes zum Umschreiben von Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="9835f-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-140">-Name</span><span class="sxs-lookup"><span data-stu-id="9835f-140">-Name</span></span>
<span data-ttu-id="9835f-141">Gibt den URL-Pfad Zuordnungsnamen an, der vom Cmdlet zum Back-End-Serverpool hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9835f-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="9835f-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="9835f-142">-PathRules</span></span>
<span data-ttu-id="9835f-143">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="9835f-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="9835f-144">Die Pfadregeln sind Bestell sensibel, werden in der Reihenfolge angewendet, in der Sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9835f-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9835f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9835f-145">CommonParameters</span></span>
<span data-ttu-id="9835f-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9835f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9835f-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9835f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9835f-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9835f-148">INPUTS</span></span>

### <span data-ttu-id="9835f-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9835f-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9835f-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9835f-150">OUTPUTS</span></span>

### <span data-ttu-id="9835f-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9835f-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9835f-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="9835f-152">NOTES</span></span>

## <span data-ttu-id="9835f-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9835f-153">RELATED LINKS</span></span>

[<span data-ttu-id="9835f-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9835f-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9835f-155">Neu – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9835f-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9835f-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9835f-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9835f-157">Satz-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9835f-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


