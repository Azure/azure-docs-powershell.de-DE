---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: bf187375ba625e40c147f7862d9faf4e0706f844
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847015"
---
# <span data-ttu-id="907fc-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="907fc-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="907fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="907fc-102">SYNOPSIS</span></span>
<span data-ttu-id="907fc-103">Fügt eine Umleitungs Konfiguration zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="907fc-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="907fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="907fc-104">SYNTAX</span></span>

### <span data-ttu-id="907fc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="907fc-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="907fc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="907fc-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="907fc-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="907fc-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="907fc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="907fc-108">DESCRIPTION</span></span>
<span data-ttu-id="907fc-109">Das Cmdlet **Add-AzApplicationGatewayRedirectConfiguration** fügt eine Umleitungs Konfiguration zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="907fc-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="907fc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="907fc-110">EXAMPLES</span></span>

### <span data-ttu-id="907fc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="907fc-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="907fc-112">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="907fc-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="907fc-113">Mit dem zweiten Befehl wird die Umleitungs Konfiguration dem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="907fc-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="907fc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="907fc-114">PARAMETERS</span></span>

### <span data-ttu-id="907fc-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="907fc-115">-ApplicationGateway</span></span>
<span data-ttu-id="907fc-116">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="907fc-116">The applicationGateway</span></span>

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

### <span data-ttu-id="907fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907fc-117">-DefaultProfile</span></span>
<span data-ttu-id="907fc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="907fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="907fc-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="907fc-119">-IncludePath</span></span>
<span data-ttu-id="907fc-120">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="907fc-120">Include path in the redirected url.</span></span>
<span data-ttu-id="907fc-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="907fc-121">Default is true.</span></span>

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

### <span data-ttu-id="907fc-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="907fc-122">-IncludeQueryString</span></span>
<span data-ttu-id="907fc-123">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="907fc-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="907fc-124">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="907fc-124">Default is true.</span></span>

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

### <span data-ttu-id="907fc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="907fc-125">-Name</span></span>
<span data-ttu-id="907fc-126">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="907fc-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="907fc-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="907fc-127">-RedirectType</span></span>
<span data-ttu-id="907fc-128">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="907fc-128">The type of redirect</span></span>

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

### <span data-ttu-id="907fc-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="907fc-129">-TargetListener</span></span>
<span data-ttu-id="907fc-130">HTTP-Listener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="907fc-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="907fc-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="907fc-131">-TargetListenerID</span></span>
<span data-ttu-id="907fc-132">Die ID des HTTP-Listeners zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="907fc-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="907fc-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="907fc-133">-TargetUrl</span></span>
<span data-ttu-id="907fc-134">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="907fc-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="907fc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907fc-135">CommonParameters</span></span>
<span data-ttu-id="907fc-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907fc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907fc-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="907fc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907fc-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="907fc-138">INPUTS</span></span>

### <span data-ttu-id="907fc-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="907fc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="907fc-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="907fc-140">OUTPUTS</span></span>

### <span data-ttu-id="907fc-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="907fc-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="907fc-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="907fc-142">NOTES</span></span>

## <span data-ttu-id="907fc-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="907fc-143">RELATED LINKS</span></span>

[<span data-ttu-id="907fc-144">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="907fc-144">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="907fc-145">Neu – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="907fc-145">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="907fc-146">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="907fc-146">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="907fc-147">Satz-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="907fc-147">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
