---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 1816b7407ec1d36f8eb5fd213484e22a9e89998c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848484"
---
# <span data-ttu-id="74f09-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="74f09-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="74f09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74f09-102">SYNOPSIS</span></span>
<span data-ttu-id="74f09-103">Fügt eine Umleitungs Konfiguration zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="74f09-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74f09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74f09-104">SYNTAX</span></span>

### <span data-ttu-id="74f09-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74f09-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74f09-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="74f09-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74f09-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="74f09-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74f09-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74f09-108">DESCRIPTION</span></span>
<span data-ttu-id="74f09-109">Das Cmdlet **Add-AzureRmApplicationGatewayRedirectConfiguration** fügt eine Umleitungs Konfiguration zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="74f09-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="74f09-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74f09-110">EXAMPLES</span></span>

### <span data-ttu-id="74f09-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74f09-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="74f09-112">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="74f09-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="74f09-113">Mit dem zweiten Befehl wird die Umleitungs Konfiguration dem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="74f09-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="74f09-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="74f09-114">PARAMETERS</span></span>

### <span data-ttu-id="74f09-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f09-115">-ApplicationGateway</span></span>
<span data-ttu-id="74f09-116">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f09-116">The applicationGateway</span></span>

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

### <span data-ttu-id="74f09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f09-117">-DefaultProfile</span></span>
<span data-ttu-id="74f09-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74f09-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74f09-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="74f09-119">-IncludePath</span></span>
<span data-ttu-id="74f09-120">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="74f09-120">Include path in the redirected url.</span></span>
<span data-ttu-id="74f09-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="74f09-121">Default is true.</span></span>

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

### <span data-ttu-id="74f09-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="74f09-122">-IncludeQueryString</span></span>
<span data-ttu-id="74f09-123">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="74f09-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="74f09-124">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="74f09-124">Default is true.</span></span>

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

### <span data-ttu-id="74f09-125">-Name</span><span class="sxs-lookup"><span data-stu-id="74f09-125">-Name</span></span>
<span data-ttu-id="74f09-126">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="74f09-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="74f09-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="74f09-127">-RedirectType</span></span>
<span data-ttu-id="74f09-128">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="74f09-128">The type of redirect</span></span>

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

### <span data-ttu-id="74f09-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="74f09-129">-TargetListener</span></span>
<span data-ttu-id="74f09-130">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="74f09-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="74f09-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="74f09-131">-TargetListenerID</span></span>
<span data-ttu-id="74f09-132">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="74f09-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="74f09-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="74f09-133">-TargetUrl</span></span>
<span data-ttu-id="74f09-134">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="74f09-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="74f09-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f09-135">CommonParameters</span></span>
<span data-ttu-id="74f09-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f09-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f09-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f09-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f09-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74f09-138">INPUTS</span></span>

### <span data-ttu-id="74f09-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f09-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74f09-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74f09-140">OUTPUTS</span></span>

### <span data-ttu-id="74f09-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f09-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74f09-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="74f09-142">NOTES</span></span>

## <span data-ttu-id="74f09-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74f09-143">RELATED LINKS</span></span>

