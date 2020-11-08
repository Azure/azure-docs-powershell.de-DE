---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 8fc8f6785e9b6eda55615fb1e2ececbaf9ab0349
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004993"
---
# <span data-ttu-id="2fc75-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2fc75-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2fc75-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fc75-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc75-103">Erstellt eine Anforderungs Routingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="2fc75-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="2fc75-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fc75-104">SYNTAX</span></span>

### <span data-ttu-id="2fc75-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc75-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fc75-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2fc75-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fc75-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fc75-107">DESCRIPTION</span></span>
<span data-ttu-id="2fc75-108">**Das Cmdlet Add-AzApplicationGatewayRequestRoutingRule** erstellt eine Anforderungs Routingregel für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2fc75-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="2fc75-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fc75-109">EXAMPLES</span></span>

### <span data-ttu-id="2fc75-110">Beispiel 1: Erstellen einer Anforderungs Routingregel für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="2fc75-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="2fc75-111">Dieser Befehl erstellt eine grundlegende Anforderungs Routingregel mit dem Namen Rule01 und speichert das Ergebnis in der Variablen mit dem Namen $Rule.</span><span class="sxs-lookup"><span data-stu-id="2fc75-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="2fc75-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fc75-112">PARAMETERS</span></span>

### <span data-ttu-id="2fc75-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2fc75-113">-BackendAddressPool</span></span>
<span data-ttu-id="2fc75-114">Gibt den Back-End-Adresspool als Objekt an, um die Anforderungs Routingregel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2fc75-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="2fc75-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2fc75-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="2fc75-116">Gibt die ID des Back-End-Adresspools der zu erstellenden Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="2fc75-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="2fc75-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2fc75-117">-BackendHttpSettings</span></span>
<span data-ttu-id="2fc75-118">Gibt die HTTP-Back-End-Einstellungen als Objekt für die zu erstellende Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="2fc75-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="2fc75-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2fc75-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="2fc75-120">Gibt die ID des Back-End-HTTP-Einstellungen der zu erstellenden Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="2fc75-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="2fc75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc75-121">-DefaultProfile</span></span>
<span data-ttu-id="2fc75-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2fc75-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fc75-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="2fc75-123">-HttpListener</span></span>
<span data-ttu-id="2fc75-124">Gibt den Back-End-HTTP-Listener für die zu erstellende Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="2fc75-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="2fc75-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="2fc75-125">-HttpListenerId</span></span>
<span data-ttu-id="2fc75-126">Gibt die Back-End-HTTP-Listener-ID für die zu erstellende Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="2fc75-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="2fc75-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2fc75-127">-Name</span></span>
<span data-ttu-id="2fc75-128">Gibt den Namen der vom Cmdlet erstellten Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="2fc75-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2fc75-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fc75-129">-RedirectConfiguration</span></span>
<span data-ttu-id="2fc75-130">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fc75-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2fc75-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2fc75-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="2fc75-132">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fc75-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2fc75-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2fc75-133">-RewriteRuleSet</span></span>
<span data-ttu-id="2fc75-134">Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2fc75-134">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2fc75-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="2fc75-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="2fc75-136">ID des Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2fc75-136">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2fc75-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="2fc75-137">-RuleType</span></span>
<span data-ttu-id="2fc75-138">Gibt den Typ der Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="2fc75-138">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="2fc75-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="2fc75-139">-UrlPathMap</span></span>
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

### <span data-ttu-id="2fc75-140">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="2fc75-140">-UrlPathMapId</span></span>
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

### <span data-ttu-id="2fc75-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc75-141">CommonParameters</span></span>
<span data-ttu-id="2fc75-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc75-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc75-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc75-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc75-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fc75-144">INPUTS</span></span>

### <span data-ttu-id="2fc75-145">Keine</span><span class="sxs-lookup"><span data-stu-id="2fc75-145">None</span></span>

## <span data-ttu-id="2fc75-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fc75-146">OUTPUTS</span></span>

### <span data-ttu-id="2fc75-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2fc75-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2fc75-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fc75-148">NOTES</span></span>

## <span data-ttu-id="2fc75-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fc75-149">RELATED LINKS</span></span>

[<span data-ttu-id="2fc75-150">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2fc75-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2fc75-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2fc75-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2fc75-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2fc75-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2fc75-153">Satz-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2fc75-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


