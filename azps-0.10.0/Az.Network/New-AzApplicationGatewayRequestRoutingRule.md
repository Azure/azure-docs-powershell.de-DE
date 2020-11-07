---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ec85b643294f65aceefae2d4a52e9a5d48f15191
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841403"
---
# <span data-ttu-id="d15a5-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d15a5-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d15a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d15a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d15a5-103">Erstellt eine Anforderungs Routingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d15a5-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="d15a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d15a5-104">SYNTAX</span></span>

### <span data-ttu-id="d15a5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d15a5-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d15a5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d15a5-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d15a5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d15a5-107">DESCRIPTION</span></span>
<span data-ttu-id="d15a5-108">**Das Cmdlet Add-AzApplicationGatewayRequestRoutingRule** erstellt eine Anforderungs Routingregel für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d15a5-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="d15a5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d15a5-109">EXAMPLES</span></span>

### <span data-ttu-id="d15a5-110">Beispiel 1: Erstellen einer Anforderungs Routingregel für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="d15a5-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="d15a5-111">Dieser Befehl erstellt eine grundlegende Anforderungs Routingregel mit dem Namen Rule01 und speichert das Ergebnis in der Variablen mit dem Namen $Rule.</span><span class="sxs-lookup"><span data-stu-id="d15a5-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="d15a5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d15a5-112">PARAMETERS</span></span>

### <span data-ttu-id="d15a5-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d15a5-113">-BackendAddressPool</span></span>
<span data-ttu-id="d15a5-114">Gibt den Back-End-Adresspool als Objekt an, um die Anforderungs Routingregel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d15a5-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="d15a5-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d15a5-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="d15a5-116">Gibt die ID des Back-End-Adresspools der zu erstellenden Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="d15a5-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="d15a5-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d15a5-117">-BackendHttpSettings</span></span>
<span data-ttu-id="d15a5-118">Gibt die HTTP-Back-End-Einstellungen als Objekt für die zu erstellende Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="d15a5-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="d15a5-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d15a5-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="d15a5-120">Gibt die ID des Back-End-HTTP-Einstellungen der zu erstellenden Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="d15a5-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="d15a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15a5-121">-DefaultProfile</span></span>
<span data-ttu-id="d15a5-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d15a5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d15a5-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="d15a5-123">-HttpListener</span></span>
<span data-ttu-id="d15a5-124">Gibt den Back-End-HTTP-Listener für die zu erstellende Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="d15a5-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="d15a5-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="d15a5-125">-HttpListenerId</span></span>
<span data-ttu-id="d15a5-126">Gibt die Back-End-HTTP-Listener-ID für die zu erstellende Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="d15a5-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="d15a5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d15a5-127">-Name</span></span>
<span data-ttu-id="d15a5-128">Gibt den Namen der vom Cmdlet erstellten Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="d15a5-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d15a5-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15a5-129">-RedirectConfiguration</span></span>
<span data-ttu-id="d15a5-130">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15a5-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="d15a5-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d15a5-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="d15a5-132">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15a5-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="d15a5-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="d15a5-133">-RuleType</span></span>
<span data-ttu-id="d15a5-134">Gibt den Typ der Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="d15a5-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="d15a5-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="d15a5-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="d15a5-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="d15a5-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="d15a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15a5-137">CommonParameters</span></span>
<span data-ttu-id="d15a5-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d15a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15a5-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15a5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15a5-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d15a5-140">INPUTS</span></span>

### <span data-ttu-id="d15a5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d15a5-141">System.String</span></span>

## <span data-ttu-id="d15a5-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d15a5-142">OUTPUTS</span></span>

### <span data-ttu-id="d15a5-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d15a5-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d15a5-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d15a5-144">NOTES</span></span>

## <span data-ttu-id="d15a5-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d15a5-145">RELATED LINKS</span></span>

[<span data-ttu-id="d15a5-146">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d15a5-146">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d15a5-147">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d15a5-147">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d15a5-148">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d15a5-148">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d15a5-149">Satz-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d15a5-149">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


