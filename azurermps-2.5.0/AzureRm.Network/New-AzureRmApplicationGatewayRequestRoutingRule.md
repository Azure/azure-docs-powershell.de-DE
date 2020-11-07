---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 2f4b1abc5d6cd6d55eef3c45c01a2939842e32c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849959"
---
# <span data-ttu-id="e89c8-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e89c8-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e89c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e89c8-102">SYNOPSIS</span></span>
<span data-ttu-id="e89c8-103">Erstellt eine Anforderungs Routingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e89c8-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e89c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e89c8-104">SYNTAX</span></span>

### <span data-ttu-id="e89c8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e89c8-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e89c8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e89c8-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e89c8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e89c8-107">DESCRIPTION</span></span>
<span data-ttu-id="e89c8-108">**Das Cmdlet Add-AzureRmApplicationGatewayRequestRoutingRule** erstellt eine Anforderungs Routingregel für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e89c8-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="e89c8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e89c8-109">EXAMPLES</span></span>

### <span data-ttu-id="e89c8-110">Beispiel 1: Erstellen einer Anforderungs Routingregel für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="e89c8-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="e89c8-111">Dieser Befehl erstellt eine grundlegende Anforderungs Routingregel mit dem Namen Rule01 und speichert das Ergebnis in der Variablen mit dem Namen $Rule.</span><span class="sxs-lookup"><span data-stu-id="e89c8-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="e89c8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e89c8-112">PARAMETERS</span></span>

### <span data-ttu-id="e89c8-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e89c8-113">-BackendAddressPool</span></span>
<span data-ttu-id="e89c8-114">Gibt den Back-End-Adresspool als Objekt an, um die Anforderungs Routingregel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e89c8-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e89c8-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e89c8-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="e89c8-116">Gibt die ID des Back-End-Adresspools der zu erstellenden Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="e89c8-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="e89c8-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e89c8-117">-BackendHttpSettings</span></span>
<span data-ttu-id="e89c8-118">Gibt die HTTP-Back-End-Einstellungen als Objekt für die zu erstellende Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="e89c8-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e89c8-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e89c8-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e89c8-120">Gibt die ID des Back-End-HTTP-Einstellungen der zu erstellenden Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="e89c8-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="e89c8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89c8-121">-DefaultProfile</span></span>
<span data-ttu-id="e89c8-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e89c8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e89c8-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e89c8-123">-HttpListener</span></span>
<span data-ttu-id="e89c8-124">Gibt den Back-End-HTTP-Listener für die zu erstellende Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="e89c8-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e89c8-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="e89c8-125">-HttpListenerId</span></span>
<span data-ttu-id="e89c8-126">Gibt die Back-End-HTTP-Listener-ID für die zu erstellende Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="e89c8-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e89c8-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e89c8-127">-Name</span></span>
<span data-ttu-id="e89c8-128">Gibt den Namen der vom Cmdlet erstellten Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="e89c8-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e89c8-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e89c8-129">-RedirectConfiguration</span></span>
<span data-ttu-id="e89c8-130">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e89c8-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e89c8-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e89c8-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="e89c8-132">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e89c8-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e89c8-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e89c8-133">-RuleType</span></span>
<span data-ttu-id="e89c8-134">Gibt den Typ der Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="e89c8-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="e89c8-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e89c8-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="e89c8-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="e89c8-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="e89c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89c8-137">CommonParameters</span></span>
<span data-ttu-id="e89c8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e89c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89c8-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e89c8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89c8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e89c8-140">INPUTS</span></span>

### <span data-ttu-id="e89c8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e89c8-141">System.String</span></span>

## <span data-ttu-id="e89c8-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e89c8-142">OUTPUTS</span></span>

### <span data-ttu-id="e89c8-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e89c8-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e89c8-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e89c8-144">NOTES</span></span>

## <span data-ttu-id="e89c8-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e89c8-145">RELATED LINKS</span></span>

[<span data-ttu-id="e89c8-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e89c8-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e89c8-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e89c8-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e89c8-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e89c8-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e89c8-149">Satz-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e89c8-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


