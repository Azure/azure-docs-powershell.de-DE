---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: eedf03e2468be36fadc519fc2e6b931c82433fc0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841847"
---
# <span data-ttu-id="f022b-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f022b-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="f022b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f022b-102">SYNOPSIS</span></span>
<span data-ttu-id="f022b-103">Fügt einem Back-End-Serverpool ein Array von URL-Pfad Zuordnungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="f022b-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f022b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f022b-104">SYNTAX</span></span>

### <span data-ttu-id="f022b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f022b-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f022b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f022b-106">SetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f022b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f022b-107">DESCRIPTION</span></span>
<span data-ttu-id="f022b-108">Mit dem Cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** wird ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f022b-108">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="f022b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f022b-109">EXAMPLES</span></span>

### <span data-ttu-id="f022b-110">1:</span><span class="sxs-lookup"><span data-stu-id="f022b-110">1:</span></span>
```

```

## <span data-ttu-id="f022b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f022b-111">PARAMETERS</span></span>

### <span data-ttu-id="f022b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f022b-112">-ApplicationGateway</span></span>
<span data-ttu-id="f022b-113">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="f022b-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="f022b-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f022b-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="f022b-115">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f022b-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="f022b-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f022b-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="f022b-117">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="f022b-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="f022b-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f022b-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="f022b-119">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f022b-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="f022b-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f022b-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="f022b-121">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="f022b-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="f022b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f022b-122">-DefaultProfile</span></span>
<span data-ttu-id="f022b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f022b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f022b-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f022b-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="f022b-125">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f022b-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="f022b-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f022b-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="f022b-127">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f022b-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="f022b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f022b-128">-Name</span></span>
<span data-ttu-id="f022b-129">Gibt den URL-Pfad Zuordnungsnamen an, der vom Cmdlet zum Back-End-Serverpool hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f022b-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="f022b-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="f022b-130">-PathRules</span></span>
<span data-ttu-id="f022b-131">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="f022b-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="f022b-132">Die Pfadregeln sind Bestell sensibel, werden in der Reihenfolge angewendet, in der Sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f022b-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="f022b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f022b-133">CommonParameters</span></span>
<span data-ttu-id="f022b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f022b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f022b-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f022b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f022b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f022b-136">INPUTS</span></span>

### <span data-ttu-id="f022b-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f022b-137">PSApplicationGateway</span></span>
<span data-ttu-id="f022b-138">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f022b-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f022b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f022b-139">OUTPUTS</span></span>

### <span data-ttu-id="f022b-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f022b-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f022b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f022b-141">NOTES</span></span>

## <span data-ttu-id="f022b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f022b-142">RELATED LINKS</span></span>

[<span data-ttu-id="f022b-143">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f022b-143">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f022b-144">Neu – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f022b-144">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f022b-145">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f022b-145">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f022b-146">Satz-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f022b-146">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


