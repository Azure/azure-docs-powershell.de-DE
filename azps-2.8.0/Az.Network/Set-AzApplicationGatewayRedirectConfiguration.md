---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 746d1bb37bd49acfdc0a353c9985508f50514073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821251"
---
# <span data-ttu-id="be3bf-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="be3bf-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="be3bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="be3bf-103">Legt die Umleitungs Konfiguration für ein vorhandenes Anwendungs Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="be3bf-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="be3bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be3bf-104">SYNTAX</span></span>

### <span data-ttu-id="be3bf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="be3bf-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be3bf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="be3bf-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be3bf-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="be3bf-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be3bf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be3bf-108">DESCRIPTION</span></span>
<span data-ttu-id="be3bf-109">**Das Cmdlet "Satz-AzApplicationGatewayRequestRoutingRule"** ändert eine Umleitungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="be3bf-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="be3bf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be3bf-110">EXAMPLES</span></span>

### <span data-ttu-id="be3bf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be3bf-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="be3bf-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="be3bf-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="be3bf-113">Mit dem zweiten Befehl wird die Umleitungs Konfiguration für das Anwendungsgateway geändert, um den Typ permanent umzuleiten und eine Ziel-URL zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="be3bf-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="be3bf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="be3bf-114">PARAMETERS</span></span>

### <span data-ttu-id="be3bf-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be3bf-115">-ApplicationGateway</span></span>
<span data-ttu-id="be3bf-116">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="be3bf-116">The applicationGateway</span></span>

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

### <span data-ttu-id="be3bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be3bf-117">-DefaultProfile</span></span>
<span data-ttu-id="be3bf-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be3bf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3bf-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="be3bf-119">-IncludePath</span></span>
<span data-ttu-id="be3bf-120">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="be3bf-120">Include path in the redirected url.</span></span>
<span data-ttu-id="be3bf-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="be3bf-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3bf-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="be3bf-122">-IncludeQueryString</span></span>
<span data-ttu-id="be3bf-123">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="be3bf-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="be3bf-124">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="be3bf-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3bf-125">-Name</span><span class="sxs-lookup"><span data-stu-id="be3bf-125">-Name</span></span>
<span data-ttu-id="be3bf-126">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="be3bf-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="be3bf-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="be3bf-127">-RedirectType</span></span>
<span data-ttu-id="be3bf-128">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="be3bf-128">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3bf-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="be3bf-129">-TargetListener</span></span>
<span data-ttu-id="be3bf-130">HTTP-Listener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="be3bf-130">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3bf-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="be3bf-131">-TargetListenerID</span></span>
<span data-ttu-id="be3bf-132">Die ID des HTTP-Listeners zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="be3bf-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="be3bf-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="be3bf-133">-TargetUrl</span></span>
<span data-ttu-id="be3bf-134">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="be3bf-134">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be3bf-135">CommonParameters</span></span>
<span data-ttu-id="be3bf-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be3bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be3bf-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be3bf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be3bf-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be3bf-138">INPUTS</span></span>

### <span data-ttu-id="be3bf-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be3bf-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="be3bf-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be3bf-140">OUTPUTS</span></span>

### <span data-ttu-id="be3bf-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be3bf-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="be3bf-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="be3bf-142">NOTES</span></span>

## <span data-ttu-id="be3bf-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be3bf-143">RELATED LINKS</span></span>

[<span data-ttu-id="be3bf-144">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="be3bf-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="be3bf-145">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="be3bf-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="be3bf-146">Neu – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="be3bf-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="be3bf-147">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="be3bf-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
