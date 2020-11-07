---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 1b6e5c2c2a28333e51c74d9621a3fd607f6a652d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849264"
---
# <span data-ttu-id="e706a-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e706a-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e706a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e706a-102">SYNOPSIS</span></span>
<span data-ttu-id="e706a-103">Fügt einem Back-End-Serverpool ein Array von URL-Pfad Zuordnungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="e706a-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e706a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e706a-104">SYNTAX</span></span>

### <span data-ttu-id="e706a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e706a-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e706a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e706a-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e706a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e706a-107">DESCRIPTION</span></span>
<span data-ttu-id="e706a-108">Mit dem Cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** wird ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e706a-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="e706a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e706a-109">EXAMPLES</span></span>

### <span data-ttu-id="e706a-110">1:</span><span class="sxs-lookup"><span data-stu-id="e706a-110">1:</span></span>
```

```

## <span data-ttu-id="e706a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e706a-111">PARAMETERS</span></span>

### <span data-ttu-id="e706a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e706a-112">-ApplicationGateway</span></span>
<span data-ttu-id="e706a-113">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e706a-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="e706a-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e706a-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="e706a-115">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e706a-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e706a-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e706a-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="e706a-117">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="e706a-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="e706a-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e706a-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="e706a-119">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e706a-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e706a-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e706a-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="e706a-121">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="e706a-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="e706a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e706a-122">-DefaultProfile</span></span>
<span data-ttu-id="e706a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e706a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e706a-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e706a-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="e706a-125">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e706a-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e706a-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e706a-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="e706a-127">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e706a-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e706a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e706a-128">-Name</span></span>
<span data-ttu-id="e706a-129">Gibt den URL-Pfad Zuordnungsnamen an, der vom Cmdlet zum Back-End-Serverpool hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e706a-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="e706a-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="e706a-130">-PathRules</span></span>
<span data-ttu-id="e706a-131">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="e706a-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="e706a-132">Die Pfadregeln sind Bestell sensibel, werden in der Reihenfolge angewendet, in der Sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="e706a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e706a-133">CommonParameters</span></span>
<span data-ttu-id="e706a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e706a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e706a-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e706a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e706a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e706a-136">INPUTS</span></span>

### <span data-ttu-id="e706a-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e706a-137">PSApplicationGateway</span></span>
<span data-ttu-id="e706a-138">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e706a-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e706a-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e706a-139">OUTPUTS</span></span>

### <span data-ttu-id="e706a-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e706a-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e706a-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="e706a-141">NOTES</span></span>

## <span data-ttu-id="e706a-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e706a-142">RELATED LINKS</span></span>

[<span data-ttu-id="e706a-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e706a-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e706a-144">Neu – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e706a-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e706a-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e706a-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e706a-146">Satz-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e706a-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


