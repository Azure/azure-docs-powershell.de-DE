---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 7ca1d4f8ee4ab3e83badecd7856fcee35f5b9a23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849944"
---
# <span data-ttu-id="cc8bd-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc8bd-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="cc8bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="cc8bd-103">Legt die Konfiguration für ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc8bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc8bd-104">SYNTAX</span></span>

### <span data-ttu-id="cc8bd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc8bd-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc8bd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cc8bd-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc8bd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc8bd-107">DESCRIPTION</span></span>
<span data-ttu-id="cc8bd-108">Das Cmdlet " **Set-AzureRmApplicationGatewayUrlPathMapConfig** " legt die Konfiguration für ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="cc8bd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc8bd-109">EXAMPLES</span></span>

### <span data-ttu-id="cc8bd-110">1:</span><span class="sxs-lookup"><span data-stu-id="cc8bd-110">1:</span></span>
```

```

## <span data-ttu-id="cc8bd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc8bd-111">PARAMETERS</span></span>

### <span data-ttu-id="cc8bd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc8bd-112">-ApplicationGateway</span></span>
<span data-ttu-id="cc8bd-113">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration festlegt.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="cc8bd-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cc8bd-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="cc8bd-115">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="cc8bd-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cc8bd-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="cc8bd-117">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="cc8bd-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cc8bd-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="cc8bd-119">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="cc8bd-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="cc8bd-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="cc8bd-121">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="cc8bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc8bd-122">-DefaultProfile</span></span>
<span data-ttu-id="cc8bd-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc8bd-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc8bd-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="cc8bd-125">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="cc8bd-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="cc8bd-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cc8bd-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="cc8bd-127">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc8bd-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="cc8bd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="cc8bd-128">-Name</span></span>
<span data-ttu-id="cc8bd-129">Gibt den URL-Pfad Zuordnungsnamen an, für den dieses Cmdlet die Konfiguration festlegt.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="cc8bd-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="cc8bd-130">-PathRules</span></span>
<span data-ttu-id="cc8bd-131">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="cc8bd-132">Beachten Sie, dass die Pfadregeln in der Reihenfolge vertraulich sind, dass Sie in der angegebenen Reihenfolge angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8bd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc8bd-133">CommonParameters</span></span>
<span data-ttu-id="cc8bd-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc8bd-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc8bd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc8bd-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc8bd-136">INPUTS</span></span>

### <span data-ttu-id="cc8bd-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc8bd-137">PSApplicationGateway</span></span>
<span data-ttu-id="cc8bd-138">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc8bd-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="cc8bd-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc8bd-139">OUTPUTS</span></span>

### <span data-ttu-id="cc8bd-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc8bd-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cc8bd-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc8bd-141">NOTES</span></span>

## <span data-ttu-id="cc8bd-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc8bd-142">RELATED LINKS</span></span>

[<span data-ttu-id="cc8bd-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc8bd-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cc8bd-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc8bd-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cc8bd-145">Neu – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc8bd-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cc8bd-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc8bd-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


