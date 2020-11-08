---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179830"
---
# <span data-ttu-id="d4034-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d4034-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d4034-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4034-102">SYNOPSIS</span></span>
<span data-ttu-id="d4034-103">Legt die Konfiguration für ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="d4034-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d4034-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4034-104">SYNTAX</span></span>

### <span data-ttu-id="d4034-105">BackendSetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4034-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4034-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d4034-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4034-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="d4034-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4034-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d4034-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4034-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4034-109">DESCRIPTION</span></span>
<span data-ttu-id="d4034-110">Das Cmdlet " **Set-AzApplicationGatewayUrlPathMapConfig** " legt die Konfiguration für ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="d4034-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d4034-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4034-111">EXAMPLES</span></span>

### <span data-ttu-id="d4034-112">Beispiel 1: Aktualisieren einer URL-Pfadzuordnung</span><span class="sxs-lookup"><span data-stu-id="d4034-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="d4034-113">Der erste Befehl ruft das Anwendungsgateway mit dem Namen appGwName ab und speichert das Ergebnis in der $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="d4034-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="d4034-114">Der zweite Befehl aktualisiert die URL-Pfadzuordnung mit dem Namen map01 im Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d4034-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="d4034-115">Der dritte Befehl aktualisiert das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d4034-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="d4034-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4034-116">PARAMETERS</span></span>

### <span data-ttu-id="d4034-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4034-117">-ApplicationGateway</span></span>
<span data-ttu-id="d4034-118">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration festlegt.</span><span class="sxs-lookup"><span data-stu-id="d4034-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="d4034-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d4034-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="d4034-120">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d4034-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d4034-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d4034-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="d4034-122">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="d4034-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="d4034-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d4034-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="d4034-124">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d4034-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d4034-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d4034-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="d4034-126">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="d4034-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="d4034-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4034-127">-DefaultProfile</span></span>
<span data-ttu-id="d4034-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4034-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4034-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4034-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="d4034-130">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d4034-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d4034-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d4034-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="d4034-132">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4034-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d4034-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4034-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="d4034-134">Standard Regelsatz für das Anwendungsgateway-Neuschreiben</span><span class="sxs-lookup"><span data-stu-id="d4034-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="d4034-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="d4034-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="d4034-136">ID des standardmäßigen Regelsatzes zum Umschreiben von Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="d4034-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="d4034-137">-Name</span><span class="sxs-lookup"><span data-stu-id="d4034-137">-Name</span></span>
<span data-ttu-id="d4034-138">Gibt den URL-Pfad Zuordnungsnamen an, für den dieses Cmdlet die Konfiguration festlegt.</span><span class="sxs-lookup"><span data-stu-id="d4034-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="d4034-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="d4034-139">-PathRules</span></span>
<span data-ttu-id="d4034-140">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="d4034-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="d4034-141">Beachten Sie, dass die Pfadregeln in der Reihenfolge vertraulich sind, dass Sie in der angegebenen Reihenfolge angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4034-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="d4034-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4034-142">CommonParameters</span></span>
<span data-ttu-id="d4034-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4034-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4034-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4034-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4034-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4034-145">INPUTS</span></span>

### <span data-ttu-id="d4034-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4034-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d4034-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4034-147">OUTPUTS</span></span>

### <span data-ttu-id="d4034-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4034-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d4034-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4034-149">NOTES</span></span>

## <span data-ttu-id="d4034-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4034-150">RELATED LINKS</span></span>

[<span data-ttu-id="d4034-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d4034-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d4034-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d4034-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d4034-153">Neu – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d4034-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d4034-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d4034-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


