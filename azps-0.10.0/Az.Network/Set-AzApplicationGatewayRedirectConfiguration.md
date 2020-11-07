---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 9e9dbd8cef57c4621e009cf0a086616a252eae67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843679"
---
# <span data-ttu-id="65012-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="65012-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="65012-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65012-102">SYNOPSIS</span></span>
<span data-ttu-id="65012-103">Legt die Umleitungs Konfiguration für ein vorhandenes Anwendungs Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="65012-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="65012-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65012-104">SYNTAX</span></span>

### <span data-ttu-id="65012-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="65012-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65012-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="65012-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65012-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="65012-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65012-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65012-108">DESCRIPTION</span></span>
<span data-ttu-id="65012-109">**Das Cmdlet "Satz-AzApplicationGatewayRequestRoutingRule"** ändert eine Umleitungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="65012-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="65012-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65012-110">EXAMPLES</span></span>

### <span data-ttu-id="65012-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65012-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="65012-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="65012-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="65012-113">Mit dem zweiten Befehl wird die Umleitungs Konfiguration für das Anwendungsgateway geändert, um den Typ permanent umzuleiten und eine Ziel-URL zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="65012-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="65012-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="65012-114">PARAMETERS</span></span>

### <span data-ttu-id="65012-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65012-115">-ApplicationGateway</span></span>
<span data-ttu-id="65012-116">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="65012-116">The applicationGateway</span></span>

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

### <span data-ttu-id="65012-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65012-117">-DefaultProfile</span></span>
<span data-ttu-id="65012-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65012-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65012-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="65012-119">-IncludePath</span></span>
<span data-ttu-id="65012-120">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="65012-120">Include path in the redirected url.</span></span>
<span data-ttu-id="65012-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="65012-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65012-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="65012-122">-IncludeQueryString</span></span>
<span data-ttu-id="65012-123">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="65012-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="65012-124">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="65012-124">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65012-125">-Name</span><span class="sxs-lookup"><span data-stu-id="65012-125">-Name</span></span>
<span data-ttu-id="65012-126">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="65012-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="65012-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="65012-127">-RedirectType</span></span>
<span data-ttu-id="65012-128">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="65012-128">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65012-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="65012-129">-TargetListener</span></span>
<span data-ttu-id="65012-130">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="65012-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="65012-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="65012-131">-TargetListenerID</span></span>
<span data-ttu-id="65012-132">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="65012-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="65012-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="65012-133">-TargetUrl</span></span>
<span data-ttu-id="65012-134">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="65012-134">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65012-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65012-135">CommonParameters</span></span>
<span data-ttu-id="65012-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65012-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65012-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65012-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65012-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65012-138">INPUTS</span></span>

### <span data-ttu-id="65012-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65012-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65012-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65012-140">OUTPUTS</span></span>

### <span data-ttu-id="65012-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65012-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65012-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="65012-142">NOTES</span></span>

## <span data-ttu-id="65012-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65012-143">RELATED LINKS</span></span>

