---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5eb4fb0f036331fe68755a3a8ebddcd7e1b6e424
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843659"
---
# <span data-ttu-id="91f03-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91f03-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="91f03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91f03-102">SYNOPSIS</span></span>
<span data-ttu-id="91f03-103">Legt die Konfiguration für ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="91f03-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="91f03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91f03-104">SYNTAX</span></span>

### <span data-ttu-id="91f03-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="91f03-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91f03-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="91f03-106">SetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91f03-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91f03-107">DESCRIPTION</span></span>
<span data-ttu-id="91f03-108">Das Cmdlet " **Set-AzApplicationGatewayUrlPathMapConfig** " legt die Konfiguration für ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="91f03-108">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="91f03-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91f03-109">EXAMPLES</span></span>

### <span data-ttu-id="91f03-110">1:</span><span class="sxs-lookup"><span data-stu-id="91f03-110">1:</span></span>
```

```

## <span data-ttu-id="91f03-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="91f03-111">PARAMETERS</span></span>

### <span data-ttu-id="91f03-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91f03-112">-ApplicationGateway</span></span>
<span data-ttu-id="91f03-113">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration festlegt.</span><span class="sxs-lookup"><span data-stu-id="91f03-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="91f03-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="91f03-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="91f03-115">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="91f03-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="91f03-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="91f03-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="91f03-117">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="91f03-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="91f03-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="91f03-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="91f03-119">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="91f03-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="91f03-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="91f03-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="91f03-121">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="91f03-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="91f03-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f03-122">-DefaultProfile</span></span>
<span data-ttu-id="91f03-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91f03-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91f03-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="91f03-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="91f03-125">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="91f03-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="91f03-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="91f03-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="91f03-127">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="91f03-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="91f03-128">-Name</span><span class="sxs-lookup"><span data-stu-id="91f03-128">-Name</span></span>
<span data-ttu-id="91f03-129">Gibt den URL-Pfad Zuordnungsnamen an, für den dieses Cmdlet die Konfiguration festlegt.</span><span class="sxs-lookup"><span data-stu-id="91f03-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="91f03-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="91f03-130">-PathRules</span></span>
<span data-ttu-id="91f03-131">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="91f03-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="91f03-132">Beachten Sie, dass die Pfadregeln in der Reihenfolge vertraulich sind, dass Sie in der angegebenen Reihenfolge angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="91f03-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="91f03-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f03-133">CommonParameters</span></span>
<span data-ttu-id="91f03-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f03-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f03-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f03-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f03-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91f03-136">INPUTS</span></span>

### <span data-ttu-id="91f03-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91f03-137">PSApplicationGateway</span></span>
<span data-ttu-id="91f03-138">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="91f03-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="91f03-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91f03-139">OUTPUTS</span></span>

### <span data-ttu-id="91f03-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91f03-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="91f03-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="91f03-141">NOTES</span></span>

## <span data-ttu-id="91f03-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91f03-142">RELATED LINKS</span></span>

[<span data-ttu-id="91f03-143">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91f03-143">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="91f03-144">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91f03-144">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="91f03-145">Neu – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91f03-145">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="91f03-146">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91f03-146">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


