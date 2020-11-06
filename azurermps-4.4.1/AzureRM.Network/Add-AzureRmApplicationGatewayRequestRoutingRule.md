---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f72fb4eb80475b421ca4a893a598d8686dde64c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501766"
---
# <span data-ttu-id="73433-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73433-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="73433-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73433-102">SYNOPSIS</span></span>
<span data-ttu-id="73433-103">Fügt eine Anforderungs Routingregel zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="73433-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73433-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73433-104">SYNTAX</span></span>

### <span data-ttu-id="73433-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="73433-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73433-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="73433-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73433-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73433-107">DESCRIPTION</span></span>
<span data-ttu-id="73433-108">Mit dem Cmdlet **Add-AzureRmApplicationGatewayRequestRoutingRule** wird eine Anforderungs Routingregel zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="73433-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="73433-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73433-109">EXAMPLES</span></span>

### <span data-ttu-id="73433-110">Beispiel 1: Hinzufügen einer Anforderungs Routingregel zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="73433-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="73433-111">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="73433-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="73433-112">Mit dem zweiten Befehl wird die Anforderungs Routingregel dem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="73433-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="73433-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="73433-113">PARAMETERS</span></span>

### <span data-ttu-id="73433-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73433-114">-ApplicationGateway</span></span>
<span data-ttu-id="73433-115">Gibt ein Anwendungsgateway an, dem dieses Cmdlet eine Anforderungs Routingregel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="73433-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="73433-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73433-116">-BackendAddressPool</span></span>
<span data-ttu-id="73433-117">Gibt ein Back-End-Adresspool Objekt des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="73433-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="73433-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="73433-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="73433-119">Gibt eine ID des Back-End-Adresspools des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="73433-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="73433-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="73433-120">-BackendHttpSettings</span></span>
<span data-ttu-id="73433-121">Gibt ein Back-End-HTTP-Einstellungsobjekt für ein Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="73433-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="73433-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="73433-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="73433-123">Gibt eine HTTP-Back-End-Einstellungen-ID für ein Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="73433-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="73433-124">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="73433-124">-HttpListener</span></span>
<span data-ttu-id="73433-125">Gibt das Application Gateway http-Listener-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="73433-125">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="73433-126">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="73433-126">-HttpListenerId</span></span>
<span data-ttu-id="73433-127">Gibt die HTTP-Listener-ID des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="73433-127">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="73433-128">-Name</span><span class="sxs-lookup"><span data-stu-id="73433-128">-Name</span></span>
<span data-ttu-id="73433-129">Gibt den Namen der Anforderungs Routingregel an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="73433-129">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="73433-130">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="73433-130">-RedirectConfiguration</span></span>
<span data-ttu-id="73433-131">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="73433-131">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="73433-132">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="73433-132">-RedirectConfigurationId</span></span>
<span data-ttu-id="73433-133">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="73433-133">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="73433-134">-RuleType</span><span class="sxs-lookup"><span data-stu-id="73433-134">-RuleType</span></span>
<span data-ttu-id="73433-135">Gibt den Typ der Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="73433-135">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="73433-136">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="73433-136">-UrlPathMap</span></span>
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

### <span data-ttu-id="73433-137">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="73433-137">-UrlPathMapId</span></span>
<span data-ttu-id="73433-138">Gibt die URL-Pfad Zuordnungs-ID für die Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="73433-138">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="73433-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73433-139">-DefaultProfile</span></span>
<span data-ttu-id="73433-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73433-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73433-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73433-141">CommonParameters</span></span>
<span data-ttu-id="73433-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73433-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73433-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73433-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73433-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73433-144">INPUTS</span></span>

### <span data-ttu-id="73433-145">System. String</span><span class="sxs-lookup"><span data-stu-id="73433-145">System.String</span></span>

## <span data-ttu-id="73433-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73433-146">OUTPUTS</span></span>

### <span data-ttu-id="73433-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73433-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73433-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="73433-148">NOTES</span></span>

## <span data-ttu-id="73433-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73433-149">RELATED LINKS</span></span>

[<span data-ttu-id="73433-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73433-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="73433-151">Neu – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73433-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="73433-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73433-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="73433-153">Satz-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73433-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


