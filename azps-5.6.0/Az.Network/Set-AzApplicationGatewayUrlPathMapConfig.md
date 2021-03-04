---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cc2a30e5a5633dcda345184bef121befe710ad8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918683"
---
# <span data-ttu-id="d12ac-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d12ac-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d12ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d12ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d12ac-103">Legt die Konfiguration für ein Array von URL-Pfadzuordnungen für einen Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="d12ac-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d12ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d12ac-104">SYNTAX</span></span>

### <span data-ttu-id="d12ac-105">Back-EndSetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d12ac-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d12ac-106">Back-EndSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d12ac-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12ac-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="d12ac-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12ac-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d12ac-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d12ac-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d12ac-109">DESCRIPTION</span></span>
<span data-ttu-id="d12ac-110">Das **Cmdlet Set-AzApplicationGatewayUrlPathMapConfig** legt die Konfiguration für ein Array von URL-Pfadzuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="d12ac-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d12ac-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d12ac-111">EXAMPLES</span></span>

### <span data-ttu-id="d12ac-112">Beispiel 1: Aktualisieren einer URL-Pfadzuordnung</span><span class="sxs-lookup"><span data-stu-id="d12ac-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="d12ac-113">Der erste Befehl ruft das Anwendungsgateway mit dem Namen "appGwName" ab und speichert das Ergebnis in der $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="d12ac-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="d12ac-114">Mit dem zweiten Befehl wird die URL-Pfadzuordnung mit dem Namen "map01" im Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d12ac-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="d12ac-115">Mit dem dritten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d12ac-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="d12ac-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d12ac-116">PARAMETERS</span></span>

### <span data-ttu-id="d12ac-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d12ac-117">-ApplicationGateway</span></span>
<span data-ttu-id="d12ac-118">Gibt das Anwendungsgateway an, auf das dieses Cmdlet eine URL-Pfadzuordnungskonfiguration legt.</span><span class="sxs-lookup"><span data-stu-id="d12ac-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="d12ac-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d12ac-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="d12ac-120">Gibt den standardmäßigen Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *Parameter pathRules* angegebenen Regeln übereinstimmen sollte.</span><span class="sxs-lookup"><span data-stu-id="d12ac-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d12ac-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d12ac-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="d12ac-122">Gibt die standardmäßige Back-End-Adresspool-ID an.</span><span class="sxs-lookup"><span data-stu-id="d12ac-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="d12ac-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d12ac-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="d12ac-124">Gibt die standardmäßigen Back-End-HTTP-Einstellungen an, die für den Fall verwendet werden sollen, dass keine der im *Parameter pathRules* angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d12ac-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d12ac-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d12ac-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="d12ac-126">Gibt die standardmäßige HTTP-Einstellungs-ID für das Back-End an.</span><span class="sxs-lookup"><span data-stu-id="d12ac-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="d12ac-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12ac-127">-DefaultProfile</span></span>
<span data-ttu-id="d12ac-128">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d12ac-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d12ac-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d12ac-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="d12ac-130">Standardmäßige RedirectConfiguration für Das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="d12ac-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d12ac-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d12ac-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="d12ac-132">ID des Standardmäßigen RedirectConfiguration-Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="d12ac-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d12ac-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d12ac-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="d12ac-134">Standardregelsatz für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="d12ac-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="d12ac-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="d12ac-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="d12ac-136">ID des Standardmäßigen Neuschreibregelsatzs für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="d12ac-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="d12ac-137">-Name</span><span class="sxs-lookup"><span data-stu-id="d12ac-137">-Name</span></span>
<span data-ttu-id="d12ac-138">Gibt den Namen der URL-Pfadzuordnung an, für den dieses Cmdlet die Konfiguration festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="d12ac-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="d12ac-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="d12ac-139">-PathRules</span></span>
<span data-ttu-id="d12ac-140">Gibt eine Liste mit Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="d12ac-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="d12ac-141">Beachten Sie, dass die Pfadregeln für die Reihenfolge vertraulich sind. Sie werden in der Reihenfolge angewendet, in der sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d12ac-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="d12ac-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12ac-142">CommonParameters</span></span>
<span data-ttu-id="d12ac-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12ac-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12ac-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d12ac-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12ac-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d12ac-145">INPUTS</span></span>

### <span data-ttu-id="d12ac-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d12ac-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d12ac-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d12ac-147">OUTPUTS</span></span>

### <span data-ttu-id="d12ac-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d12ac-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d12ac-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d12ac-149">NOTES</span></span>

## <span data-ttu-id="d12ac-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d12ac-150">RELATED LINKS</span></span>

[<span data-ttu-id="d12ac-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d12ac-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d12ac-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d12ac-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d12ac-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d12ac-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d12ac-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d12ac-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


