---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 949de1a2016ffbecb96a8f10a34435cedd284ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503050"
---
# <span data-ttu-id="e643a-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e643a-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e643a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e643a-102">SYNOPSIS</span></span>
<span data-ttu-id="e643a-103">Legt die Konfiguration für ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="e643a-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e643a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e643a-104">SYNTAX</span></span>

### <span data-ttu-id="e643a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e643a-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e643a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e643a-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e643a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e643a-107">DESCRIPTION</span></span>
<span data-ttu-id="e643a-108">Das Cmdlet " **Set-AzureRmApplicationGatewayUrlPathMapConfig** " legt die Konfiguration für ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="e643a-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e643a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e643a-109">EXAMPLES</span></span>

## <span data-ttu-id="e643a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e643a-110">PARAMETERS</span></span>

### <span data-ttu-id="e643a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e643a-111">-ApplicationGateway</span></span>
<span data-ttu-id="e643a-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration festlegt.</span><span class="sxs-lookup"><span data-stu-id="e643a-112">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="e643a-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e643a-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="e643a-114">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e643a-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e643a-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e643a-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="e643a-116">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="e643a-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="e643a-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e643a-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="e643a-118">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e643a-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e643a-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e643a-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="e643a-120">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="e643a-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="e643a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e643a-121">-DefaultProfile</span></span>
<span data-ttu-id="e643a-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e643a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e643a-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e643a-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="e643a-124">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e643a-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e643a-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e643a-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="e643a-126">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e643a-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e643a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e643a-127">-Name</span></span>
<span data-ttu-id="e643a-128">Gibt den URL-Pfad Zuordnungsnamen an, für den dieses Cmdlet die Konfiguration festlegt.</span><span class="sxs-lookup"><span data-stu-id="e643a-128">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="e643a-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="e643a-129">-PathRules</span></span>
<span data-ttu-id="e643a-130">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="e643a-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="e643a-131">Beachten Sie, dass die Pfadregeln in der Reihenfolge vertraulich sind, dass Sie in der angegebenen Reihenfolge angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e643a-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="e643a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e643a-132">CommonParameters</span></span>
<span data-ttu-id="e643a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e643a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e643a-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e643a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e643a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e643a-135">INPUTS</span></span>

### <span data-ttu-id="e643a-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e643a-136">PSApplicationGateway</span></span>
<span data-ttu-id="e643a-137">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e643a-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e643a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e643a-138">OUTPUTS</span></span>

### <span data-ttu-id="e643a-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e643a-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e643a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="e643a-140">NOTES</span></span>

## <span data-ttu-id="e643a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e643a-141">RELATED LINKS</span></span>

[<span data-ttu-id="e643a-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e643a-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e643a-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e643a-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e643a-144">Neu – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e643a-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e643a-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e643a-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


