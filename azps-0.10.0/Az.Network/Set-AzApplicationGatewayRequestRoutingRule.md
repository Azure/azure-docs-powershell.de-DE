---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c2c212d3cf80044ce7c81d9d4ebd318f6a1e93ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843676"
---
# <span data-ttu-id="46007-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46007-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="46007-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46007-102">SYNOPSIS</span></span>
<span data-ttu-id="46007-103">Ändert eine Anforderungs Routingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="46007-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="46007-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46007-104">SYNTAX</span></span>

### <span data-ttu-id="46007-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="46007-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46007-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="46007-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46007-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46007-107">DESCRIPTION</span></span>
<span data-ttu-id="46007-108">Das Cmdlet " **Satz-AzApplicationGatewayRequestRoutingRule** " ändert eine Anforderungs Routingregel.</span><span class="sxs-lookup"><span data-stu-id="46007-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="46007-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46007-109">EXAMPLES</span></span>

### <span data-ttu-id="46007-110">Beispiel 1: Aktualisieren einer Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="46007-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="46007-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="46007-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="46007-112">Mit dem zweiten Befehl wird die Anforderungs Routingregel für das Anwendungsgateway so geändert, dass die in der $Setting-Variable angegebenen http-Einstellungen für das Back-End verwendet werden, ein in der $Listener-Variable festgelegter http-Listener und ein in der $Pool-Variable festgelegter Back-End-Adresspool.</span><span class="sxs-lookup"><span data-stu-id="46007-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="46007-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="46007-113">PARAMETERS</span></span>

### <span data-ttu-id="46007-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46007-114">-ApplicationGateway</span></span>
<span data-ttu-id="46007-115">Gibt das Application Gateway-Objekt an, mit dem dieses Cmdlet eine Anforderungs Routingregel anordnet.</span><span class="sxs-lookup"><span data-stu-id="46007-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="46007-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="46007-116">-BackendAddressPool</span></span>
<span data-ttu-id="46007-117">Gibt den Back-End-Adresspool des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="46007-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="46007-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="46007-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="46007-119">Gibt die ID des Back-End-Adresspools des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="46007-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="46007-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="46007-120">-BackendHttpSettings</span></span>
<span data-ttu-id="46007-121">Gibt die http-Einstellungen des Application Gateway-Back-Ends an.</span><span class="sxs-lookup"><span data-stu-id="46007-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="46007-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="46007-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="46007-123">Gibt die ID des Back-End-HTTP-Einstellungen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="46007-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="46007-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46007-124">-DefaultProfile</span></span>
<span data-ttu-id="46007-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46007-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46007-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="46007-126">-HttpListener</span></span>
<span data-ttu-id="46007-127">Gibt den Application Gateway http-Listener an.</span><span class="sxs-lookup"><span data-stu-id="46007-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="46007-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="46007-128">-HttpListenerId</span></span>
<span data-ttu-id="46007-129">Gibt die HTTP-Listener-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="46007-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="46007-130">-Name</span><span class="sxs-lookup"><span data-stu-id="46007-130">-Name</span></span>
<span data-ttu-id="46007-131">Gibt den Namen der Anforderungs Routingregel an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="46007-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="46007-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="46007-132">-RedirectConfiguration</span></span>
<span data-ttu-id="46007-133">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="46007-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="46007-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="46007-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="46007-135">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="46007-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="46007-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="46007-136">-RuleType</span></span>
<span data-ttu-id="46007-137">Gibt den Typ der Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="46007-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="46007-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="46007-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="46007-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="46007-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="46007-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46007-140">CommonParameters</span></span>
<span data-ttu-id="46007-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46007-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46007-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46007-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46007-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46007-143">INPUTS</span></span>

### <span data-ttu-id="46007-144">System. String</span><span class="sxs-lookup"><span data-stu-id="46007-144">System.String</span></span>

## <span data-ttu-id="46007-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46007-145">OUTPUTS</span></span>

### <span data-ttu-id="46007-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46007-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="46007-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="46007-147">NOTES</span></span>

## <span data-ttu-id="46007-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46007-148">RELATED LINKS</span></span>

[<span data-ttu-id="46007-149">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46007-149">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="46007-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46007-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="46007-151">Neu – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46007-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="46007-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46007-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


