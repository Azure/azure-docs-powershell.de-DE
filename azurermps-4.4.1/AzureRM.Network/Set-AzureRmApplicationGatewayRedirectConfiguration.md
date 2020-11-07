---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 23b27fc0b8b2a8d55a2af91d808b846e4de324a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662906"
---
# <span data-ttu-id="5ddaf-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ddaf-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="5ddaf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ddaf-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddaf-103">Legt die Umleitungs Konfiguration für ein vorhandenes Anwendungs Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ddaf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ddaf-104">SYNTAX</span></span>

### <span data-ttu-id="5ddaf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ddaf-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ddaf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5ddaf-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ddaf-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="5ddaf-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ddaf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ddaf-108">DESCRIPTION</span></span>
<span data-ttu-id="5ddaf-109">**Das Cmdlet "Satz-AzureRmApplicationGatewayRequestRoutingRule"** ändert eine Umleitungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="5ddaf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ddaf-110">EXAMPLES</span></span>

### <span data-ttu-id="5ddaf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5ddaf-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="5ddaf-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="5ddaf-113">Mit dem zweiten Befehl wird die Umleitungs Konfiguration für das Anwendungsgateway geändert, um den Typ permanent umzuleiten und eine Ziel-URL zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="5ddaf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ddaf-114">PARAMETERS</span></span>

### <span data-ttu-id="5ddaf-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ddaf-115">-ApplicationGateway</span></span>
<span data-ttu-id="5ddaf-116">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ddaf-116">The applicationGateway</span></span>

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

### <span data-ttu-id="5ddaf-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="5ddaf-117">-IncludePath</span></span>
<span data-ttu-id="5ddaf-118">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-118">Include path in the redirected url.</span></span>
<span data-ttu-id="5ddaf-119">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-119">Default is true.</span></span>

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

### <span data-ttu-id="5ddaf-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="5ddaf-120">-IncludeQueryString</span></span>
<span data-ttu-id="5ddaf-121">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="5ddaf-122">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-122">Default is true.</span></span>

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

### <span data-ttu-id="5ddaf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5ddaf-123">-Name</span></span>
<span data-ttu-id="5ddaf-124">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="5ddaf-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="5ddaf-125">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="5ddaf-125">-RedirectType</span></span>
<span data-ttu-id="5ddaf-126">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="5ddaf-126">The type of redirect</span></span>

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

### <span data-ttu-id="5ddaf-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="5ddaf-127">-TargetListener</span></span>
<span data-ttu-id="5ddaf-128">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="5ddaf-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="5ddaf-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="5ddaf-129">-TargetListenerID</span></span>
<span data-ttu-id="5ddaf-130">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="5ddaf-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="5ddaf-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="5ddaf-131">-TargetUrl</span></span>
<span data-ttu-id="5ddaf-132">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="5ddaf-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="5ddaf-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddaf-133">-DefaultProfile</span></span>
<span data-ttu-id="5ddaf-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ddaf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddaf-135">CommonParameters</span></span>
<span data-ttu-id="5ddaf-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ddaf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddaf-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ddaf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddaf-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ddaf-138">INPUTS</span></span>

### <span data-ttu-id="5ddaf-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ddaf-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ddaf-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ddaf-140">OUTPUTS</span></span>

### <span data-ttu-id="5ddaf-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ddaf-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ddaf-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ddaf-142">NOTES</span></span>

## <span data-ttu-id="5ddaf-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ddaf-143">RELATED LINKS</span></span>

