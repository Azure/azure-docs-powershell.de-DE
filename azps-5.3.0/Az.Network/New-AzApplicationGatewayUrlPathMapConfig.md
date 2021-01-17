---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459979"
---
# <span data-ttu-id="81208-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81208-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="81208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81208-102">SYNOPSIS</span></span>
<span data-ttu-id="81208-103">Erstellt ein Array von URL-Pfadzuordnungen zu einem Back-End-Server-Pool.</span><span class="sxs-lookup"><span data-stu-id="81208-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="81208-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81208-104">SYNTAX</span></span>

### <span data-ttu-id="81208-105">Back-EndByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="81208-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81208-106">Back-EndByResourceId</span><span class="sxs-lookup"><span data-stu-id="81208-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81208-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="81208-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81208-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="81208-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81208-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81208-109">DESCRIPTION</span></span>
<span data-ttu-id="81208-110">Das **Cmdlet "New-AzApplicationGatewayUrlPathMapConfig"** erstellt ein Array von URL-Pfadzuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="81208-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="81208-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81208-111">EXAMPLES</span></span>

### <span data-ttu-id="81208-112">Beispiel 1: Erstellen eines Arrays mit URL-Pfadzuordnungen zu einem Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="81208-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="81208-113">Dieser Befehl erstellt ein Array von URL-Pfadzuordnungen zu einem Back-End-Server-Pool.</span><span class="sxs-lookup"><span data-stu-id="81208-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="81208-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81208-114">PARAMETERS</span></span>

### <span data-ttu-id="81208-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81208-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="81208-116">Gibt den standardmäßigen Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im Parameter *"pathRules" angegebenen Regeln* zustimmt.</span><span class="sxs-lookup"><span data-stu-id="81208-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="81208-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="81208-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="81208-118">Gibt die standardmäßige Back-End-Adresspool-ID an.</span><span class="sxs-lookup"><span data-stu-id="81208-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="81208-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="81208-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="81208-120">Gibt die standardmäßigen BACK-End-HTTP-Einstellungen an, die für den Fall verwendet werden sollen, dass keine der im Parameter *"pathRules" angegebenen Regeln* zustimmt.</span><span class="sxs-lookup"><span data-stu-id="81208-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="81208-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="81208-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="81208-122">Gibt die standardmäßige HTTP-Einstellungs-ID des Backends an.</span><span class="sxs-lookup"><span data-stu-id="81208-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="81208-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81208-123">-DefaultProfile</span></span>
<span data-ttu-id="81208-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81208-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81208-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="81208-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="81208-126">Standardmäßige Umleitungskonfiguration des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="81208-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="81208-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="81208-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="81208-128">ID des standardmäßigen Anwendungsgateways "RedirectConfiguration"</span><span class="sxs-lookup"><span data-stu-id="81208-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="81208-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81208-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="81208-130">Anwendungsgateway, Standardregelsatz für neu schreiben</span><span class="sxs-lookup"><span data-stu-id="81208-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="81208-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="81208-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="81208-132">ID des Standardmäßigen Regelsets für Neuschreibung des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="81208-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="81208-133">-Name</span><span class="sxs-lookup"><span data-stu-id="81208-133">-Name</span></span>
<span data-ttu-id="81208-134">Gibt den Namen der URL-Pfadzuordnung an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="81208-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="81208-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="81208-135">-PathRules</span></span>
<span data-ttu-id="81208-136">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="81208-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="81208-137">Beachten Sie, dass bei den Pfadregeln die Reihenfolge beachtet wird. Sie werden in der Reihenfolge ihrer Angabe angewendet.</span><span class="sxs-lookup"><span data-stu-id="81208-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="81208-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81208-138">CommonParameters</span></span>
<span data-ttu-id="81208-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81208-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81208-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81208-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81208-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81208-141">INPUTS</span></span>

### <span data-ttu-id="81208-142">Keine</span><span class="sxs-lookup"><span data-stu-id="81208-142">None</span></span>

## <span data-ttu-id="81208-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81208-143">OUTPUTS</span></span>

### <span data-ttu-id="81208-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="81208-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="81208-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="81208-145">NOTES</span></span>

## <span data-ttu-id="81208-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="81208-146">RELATED LINKS</span></span>

[<span data-ttu-id="81208-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81208-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="81208-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81208-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="81208-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81208-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="81208-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81208-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


