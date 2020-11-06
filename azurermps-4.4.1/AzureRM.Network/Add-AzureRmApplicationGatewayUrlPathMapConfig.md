---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 821f31ba8f42ff8a7b94839aad344a2f144353d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501761"
---
# <span data-ttu-id="7e1d9-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e1d9-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7e1d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1d9-103">Fügt einem Back-End-Serverpool ein Array von URL-Pfad Zuordnungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e1d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e1d9-104">SYNTAX</span></span>

### <span data-ttu-id="7e1d9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e1d9-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e1d9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7e1d9-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e1d9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e1d9-107">DESCRIPTION</span></span>
<span data-ttu-id="7e1d9-108">Mit dem Cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** wird ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="7e1d9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e1d9-109">EXAMPLES</span></span>

## <span data-ttu-id="7e1d9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e1d9-110">PARAMETERS</span></span>

### <span data-ttu-id="7e1d9-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e1d9-111">-ApplicationGateway</span></span>
<span data-ttu-id="7e1d9-112">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="7e1d9-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7e1d9-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="7e1d9-114">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="7e1d9-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7e1d9-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="7e1d9-116">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="7e1d9-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7e1d9-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="7e1d9-118">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="7e1d9-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7e1d9-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="7e1d9-120">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="7e1d9-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e1d9-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="7e1d9-122">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7e1d9-122">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="7e1d9-123">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7e1d9-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="7e1d9-124">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e1d9-124">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="7e1d9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7e1d9-125">-Name</span></span>
<span data-ttu-id="7e1d9-126">Gibt den URL-Pfad Zuordnungsnamen an, der vom Cmdlet zum Back-End-Serverpool hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-126">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="7e1d9-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="7e1d9-127">-PathRules</span></span>
<span data-ttu-id="7e1d9-128">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="7e1d9-129">Die Pfadregeln sind Bestell sensibel, werden in der Reihenfolge angewendet, in der Sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-129">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="7e1d9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1d9-130">-DefaultProfile</span></span>
<span data-ttu-id="7e1d9-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e1d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1d9-132">CommonParameters</span></span>
<span data-ttu-id="7e1d9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1d9-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e1d9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1d9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e1d9-135">INPUTS</span></span>

### <span data-ttu-id="7e1d9-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e1d9-136">PSApplicationGateway</span></span>
<span data-ttu-id="7e1d9-137">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="7e1d9-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e1d9-138">OUTPUTS</span></span>

### <span data-ttu-id="7e1d9-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e1d9-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7e1d9-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e1d9-140">NOTES</span></span>

## <span data-ttu-id="7e1d9-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e1d9-141">RELATED LINKS</span></span>

[<span data-ttu-id="7e1d9-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e1d9-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7e1d9-143">Neu – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e1d9-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7e1d9-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e1d9-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7e1d9-145">Satz-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e1d9-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


