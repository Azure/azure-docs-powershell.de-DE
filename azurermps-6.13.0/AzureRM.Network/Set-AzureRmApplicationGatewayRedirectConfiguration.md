---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fe6c2ce03c238dadb53e8e0df88e4402d8f614d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477817"
---
# <span data-ttu-id="5a44c-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a44c-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="5a44c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a44c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a44c-103">Legt die Umleitungs Konfiguration für ein vorhandenes Anwendungs Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="5a44c-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a44c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a44c-104">SYNTAX</span></span>

### <span data-ttu-id="5a44c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a44c-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a44c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5a44c-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a44c-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="5a44c-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a44c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a44c-108">DESCRIPTION</span></span>
<span data-ttu-id="5a44c-109">**Das Cmdlet "Satz-AzureRmApplicationGatewayRequestRoutingRule"** ändert eine Umleitungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a44c-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="5a44c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a44c-110">EXAMPLES</span></span>

### <span data-ttu-id="5a44c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a44c-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="5a44c-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5a44c-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5a44c-113">Mit dem zweiten Befehl wird die Umleitungs Konfiguration für das Anwendungsgateway geändert, um den Typ permanent umzuleiten und eine Ziel-URL zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a44c-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="5a44c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a44c-114">PARAMETERS</span></span>

### <span data-ttu-id="5a44c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a44c-115">-ApplicationGateway</span></span>
<span data-ttu-id="5a44c-116">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a44c-116">The applicationGateway</span></span>

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

### <span data-ttu-id="5a44c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a44c-117">-DefaultProfile</span></span>
<span data-ttu-id="5a44c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a44c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a44c-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="5a44c-119">-IncludePath</span></span>
<span data-ttu-id="5a44c-120">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="5a44c-120">Include path in the redirected url.</span></span>
<span data-ttu-id="5a44c-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="5a44c-121">Default is true.</span></span>

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

### <span data-ttu-id="5a44c-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="5a44c-122">-IncludeQueryString</span></span>
<span data-ttu-id="5a44c-123">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="5a44c-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="5a44c-124">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="5a44c-124">Default is true.</span></span>

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

### <span data-ttu-id="5a44c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5a44c-125">-Name</span></span>
<span data-ttu-id="5a44c-126">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="5a44c-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="5a44c-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="5a44c-127">-RedirectType</span></span>
<span data-ttu-id="5a44c-128">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="5a44c-128">The type of redirect</span></span>

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

### <span data-ttu-id="5a44c-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="5a44c-129">-TargetListener</span></span>
<span data-ttu-id="5a44c-130">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="5a44c-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="5a44c-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="5a44c-131">-TargetListenerID</span></span>
<span data-ttu-id="5a44c-132">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="5a44c-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="5a44c-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="5a44c-133">-TargetUrl</span></span>
<span data-ttu-id="5a44c-134">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="5a44c-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="5a44c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a44c-135">CommonParameters</span></span>
<span data-ttu-id="5a44c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a44c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a44c-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a44c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a44c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a44c-138">INPUTS</span></span>

### <span data-ttu-id="5a44c-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a44c-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="5a44c-140">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5a44c-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="5a44c-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a44c-141">OUTPUTS</span></span>

### <span data-ttu-id="5a44c-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a44c-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a44c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a44c-143">NOTES</span></span>

## <span data-ttu-id="5a44c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a44c-144">RELATED LINKS</span></span>
