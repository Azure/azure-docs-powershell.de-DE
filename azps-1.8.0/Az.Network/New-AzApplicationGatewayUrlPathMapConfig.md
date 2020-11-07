---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1e9a97d01fd42bae636d93311b41bc6150394d9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660578"
---
# <span data-ttu-id="7662a-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7662a-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7662a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7662a-102">SYNOPSIS</span></span>
<span data-ttu-id="7662a-103">Erstellt ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="7662a-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7662a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7662a-104">SYNTAX</span></span>

### <span data-ttu-id="7662a-105">BackendSetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="7662a-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7662a-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7662a-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7662a-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="7662a-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7662a-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7662a-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7662a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7662a-109">DESCRIPTION</span></span>
<span data-ttu-id="7662a-110">Das Cmdlet **New-AzApplicationGatewayUrlPathMapConfig** erstellt ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="7662a-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7662a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7662a-111">EXAMPLES</span></span>

### <span data-ttu-id="7662a-112">Beispiel 1: Erstellen eines Arrays von URL-Pfad Zuordnungen zu einem Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="7662a-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="7662a-113">Dieser Befehl erstellt ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="7662a-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7662a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7662a-114">PARAMETERS</span></span>

### <span data-ttu-id="7662a-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7662a-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="7662a-116">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7662a-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="7662a-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7662a-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="7662a-118">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="7662a-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="7662a-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7662a-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="7662a-120">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7662a-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="7662a-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7662a-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="7662a-122">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="7662a-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="7662a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7662a-123">-DefaultProfile</span></span>
<span data-ttu-id="7662a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7662a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7662a-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7662a-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="7662a-126">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7662a-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="7662a-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7662a-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="7662a-128">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7662a-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="7662a-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7662a-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="7662a-130">Standard Regelsatz für das Anwendungsgateway-Neuschreiben</span><span class="sxs-lookup"><span data-stu-id="7662a-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="7662a-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="7662a-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="7662a-132">ID des standardmäßigen Regelsatzes zum Umschreiben von Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="7662a-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="7662a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="7662a-133">-Name</span></span>
<span data-ttu-id="7662a-134">Gibt den vom Cmdlet erstellten URL-Pfad Zuordnungsnamen an.</span><span class="sxs-lookup"><span data-stu-id="7662a-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7662a-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="7662a-135">-PathRules</span></span>
<span data-ttu-id="7662a-136">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="7662a-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="7662a-137">Beachten Sie, dass die Pfadregeln in der Reihenfolge vertraulich sind, dass Sie in der angegebenen Reihenfolge angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7662a-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="7662a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7662a-138">CommonParameters</span></span>
<span data-ttu-id="7662a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7662a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7662a-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7662a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7662a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7662a-141">INPUTS</span></span>

### <span data-ttu-id="7662a-142">Keine</span><span class="sxs-lookup"><span data-stu-id="7662a-142">None</span></span>

## <span data-ttu-id="7662a-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7662a-143">OUTPUTS</span></span>

### <span data-ttu-id="7662a-144">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="7662a-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="7662a-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="7662a-145">NOTES</span></span>

## <span data-ttu-id="7662a-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7662a-146">RELATED LINKS</span></span>

[<span data-ttu-id="7662a-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7662a-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7662a-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7662a-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7662a-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7662a-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7662a-150">Satz-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7662a-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


