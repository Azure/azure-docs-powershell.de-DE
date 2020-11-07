---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: e3b52040090ace745f58e8c3dd56ac59bb5d9b73
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849092"
---
# <span data-ttu-id="c7ed6-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c7ed6-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c7ed6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ed6-103">Ändert eine Anforderungs Routingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7ed6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7ed6-104">SYNTAX</span></span>

### <span data-ttu-id="c7ed6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7ed6-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7ed6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c7ed6-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7ed6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7ed6-107">DESCRIPTION</span></span>
<span data-ttu-id="c7ed6-108">Das Cmdlet " **Satz-AzureRmApplicationGatewayRequestRoutingRule** " ändert eine Anforderungs Routingregel.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="c7ed6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7ed6-109">EXAMPLES</span></span>

### <span data-ttu-id="c7ed6-110">Beispiel 1: Aktualisieren einer Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="c7ed6-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c7ed6-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="c7ed6-112">Mit dem zweiten Befehl wird die Anforderungs Routingregel für das Anwendungsgateway so geändert, dass die in der $Setting-Variable angegebenen http-Einstellungen für das Back-End verwendet werden, ein in der $Listener-Variable festgelegter http-Listener und ein in der $Pool-Variable festgelegter Back-End-Adresspool.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="c7ed6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7ed6-113">PARAMETERS</span></span>

### <span data-ttu-id="c7ed6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7ed6-114">-ApplicationGateway</span></span>
<span data-ttu-id="c7ed6-115">Gibt das Application Gateway-Objekt an, mit dem dieses Cmdlet eine Anforderungs Routingregel anordnet.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c7ed6-116">-BackendAddressPool</span></span>
<span data-ttu-id="c7ed6-117">Gibt den Back-End-Adresspool des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-117">Specifies the application gateway back-end address pool.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c7ed6-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c7ed6-119">Gibt die ID des Back-End-Adresspools des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-119">Specifies the application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c7ed6-120">-BackendHttpSettings</span></span>
<span data-ttu-id="c7ed6-121">Gibt die http-Einstellungen des Application Gateway-Back-Ends an.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-121">Specifies the application gateway backend HTTP settings.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c7ed6-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c7ed6-123">Gibt die ID des Back-End-HTTP-Einstellungen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ed6-124">-DefaultProfile</span></span>
<span data-ttu-id="c7ed6-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c7ed6-126">-HttpListener</span></span>
<span data-ttu-id="c7ed6-127">Gibt den Application Gateway http-Listener an.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-127">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="c7ed6-128">-HttpListenerId</span></span>
<span data-ttu-id="c7ed6-129">Gibt die HTTP-Listener-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-129">Specifies the application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c7ed6-130">-Name</span></span>
<span data-ttu-id="c7ed6-131">Gibt den Namen der Anforderungs Routingregel an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ed6-132">-RedirectConfiguration</span></span>
<span data-ttu-id="c7ed6-133">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ed6-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c7ed6-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="c7ed6-135">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ed6-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c7ed6-136">-RuleType</span></span>
<span data-ttu-id="c7ed6-137">Gibt den Typ der Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c7ed6-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="c7ed6-139">-UrlPathMapId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ed6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ed6-140">CommonParameters</span></span>
<span data-ttu-id="c7ed6-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7ed6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ed6-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7ed6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ed6-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7ed6-143">INPUTS</span></span>

### <span data-ttu-id="c7ed6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c7ed6-144">System.String</span></span>

## <span data-ttu-id="c7ed6-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7ed6-145">OUTPUTS</span></span>

### <span data-ttu-id="c7ed6-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7ed6-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7ed6-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7ed6-147">NOTES</span></span>

## <span data-ttu-id="c7ed6-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7ed6-148">RELATED LINKS</span></span>

[<span data-ttu-id="c7ed6-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c7ed6-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c7ed6-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c7ed6-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c7ed6-151">Neu – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c7ed6-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c7ed6-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c7ed6-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


