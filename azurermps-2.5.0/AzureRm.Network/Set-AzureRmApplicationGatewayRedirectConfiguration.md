---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: c851e075c4963477d8b8f6b18440780735c74f32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849943"
---
# <span data-ttu-id="e1e0f-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1e0f-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e1e0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e0f-103">Legt die Umleitungs Konfiguration für ein vorhandenes Anwendungs Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1e0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1e0f-104">SYNTAX</span></span>

### <span data-ttu-id="e1e0f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1e0f-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e0f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e1e0f-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e0f-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="e1e0f-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1e0f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1e0f-108">DESCRIPTION</span></span>
<span data-ttu-id="e1e0f-109">**Das Cmdlet "Satz-AzureRmApplicationGatewayRequestRoutingRule"** ändert eine Umleitungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="e1e0f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1e0f-110">EXAMPLES</span></span>

### <span data-ttu-id="e1e0f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1e0f-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="e1e0f-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e1e0f-113">Mit dem zweiten Befehl wird die Umleitungs Konfiguration für das Anwendungsgateway geändert, um den Typ permanent umzuleiten und eine Ziel-URL zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="e1e0f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1e0f-114">PARAMETERS</span></span>

### <span data-ttu-id="e1e0f-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1e0f-115">-ApplicationGateway</span></span>
<span data-ttu-id="e1e0f-116">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1e0f-116">The applicationGateway</span></span>

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

### <span data-ttu-id="e1e0f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e0f-117">-DefaultProfile</span></span>
<span data-ttu-id="e1e0f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1e0f-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="e1e0f-119">-IncludePath</span></span>
<span data-ttu-id="e1e0f-120">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-120">Include path in the redirected url.</span></span>
<span data-ttu-id="e1e0f-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-121">Default is true.</span></span>

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

### <span data-ttu-id="e1e0f-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="e1e0f-122">-IncludeQueryString</span></span>
<span data-ttu-id="e1e0f-123">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="e1e0f-124">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-124">Default is true.</span></span>

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

### <span data-ttu-id="e1e0f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e1e0f-125">-Name</span></span>
<span data-ttu-id="e1e0f-126">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e1e0f-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="e1e0f-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="e1e0f-127">-RedirectType</span></span>
<span data-ttu-id="e1e0f-128">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="e1e0f-128">The type of redirect</span></span>

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

### <span data-ttu-id="e1e0f-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="e1e0f-129">-TargetListener</span></span>
<span data-ttu-id="e1e0f-130">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="e1e0f-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="e1e0f-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="e1e0f-131">-TargetListenerID</span></span>
<span data-ttu-id="e1e0f-132">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="e1e0f-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="e1e0f-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="e1e0f-133">-TargetUrl</span></span>
<span data-ttu-id="e1e0f-134">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="e1e0f-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="e1e0f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e0f-135">CommonParameters</span></span>
<span data-ttu-id="e1e0f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e0f-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1e0f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e0f-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1e0f-138">INPUTS</span></span>

### <span data-ttu-id="e1e0f-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1e0f-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1e0f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1e0f-140">OUTPUTS</span></span>

### <span data-ttu-id="e1e0f-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1e0f-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1e0f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1e0f-142">NOTES</span></span>

## <span data-ttu-id="e1e0f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1e0f-143">RELATED LINKS</span></span>

