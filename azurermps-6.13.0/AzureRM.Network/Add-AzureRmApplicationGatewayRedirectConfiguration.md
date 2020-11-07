---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 01f7daf47fa62e346dc7323ee5978f81f5797e29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665152"
---
# <span data-ttu-id="0d8e0-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d8e0-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="0d8e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8e0-103">Fügt eine Umleitungs Konfiguration zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d8e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d8e0-104">SYNTAX</span></span>

### <span data-ttu-id="0d8e0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d8e0-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d8e0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0d8e0-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d8e0-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="0d8e0-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d8e0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d8e0-108">DESCRIPTION</span></span>
<span data-ttu-id="0d8e0-109">Das Cmdlet **Add-AzureRmApplicationGatewayRedirectConfiguration** fügt eine Umleitungs Konfiguration zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="0d8e0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d8e0-110">EXAMPLES</span></span>

### <span data-ttu-id="0d8e0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d8e0-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="0d8e0-112">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0d8e0-113">Mit dem zweiten Befehl wird die Umleitungs Konfiguration dem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="0d8e0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d8e0-114">PARAMETERS</span></span>

### <span data-ttu-id="0d8e0-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d8e0-115">-ApplicationGateway</span></span>
<span data-ttu-id="0d8e0-116">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d8e0-116">The applicationGateway</span></span>

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

### <span data-ttu-id="0d8e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8e0-117">-DefaultProfile</span></span>
<span data-ttu-id="0d8e0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d8e0-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="0d8e0-119">-IncludePath</span></span>
<span data-ttu-id="0d8e0-120">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-120">Include path in the redirected url.</span></span>
<span data-ttu-id="0d8e0-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-121">Default is true.</span></span>

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

### <span data-ttu-id="0d8e0-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="0d8e0-122">-IncludeQueryString</span></span>
<span data-ttu-id="0d8e0-123">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="0d8e0-124">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-124">Default is true.</span></span>

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

### <span data-ttu-id="0d8e0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0d8e0-125">-Name</span></span>
<span data-ttu-id="0d8e0-126">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="0d8e0-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="0d8e0-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="0d8e0-127">-RedirectType</span></span>
<span data-ttu-id="0d8e0-128">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="0d8e0-128">The type of redirect</span></span>

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

### <span data-ttu-id="0d8e0-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="0d8e0-129">-TargetListener</span></span>
<span data-ttu-id="0d8e0-130">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="0d8e0-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="0d8e0-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="0d8e0-131">-TargetListenerID</span></span>
<span data-ttu-id="0d8e0-132">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="0d8e0-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="0d8e0-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="0d8e0-133">-TargetUrl</span></span>
<span data-ttu-id="0d8e0-134">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="0d8e0-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="0d8e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8e0-135">CommonParameters</span></span>
<span data-ttu-id="0d8e0-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d8e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8e0-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d8e0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8e0-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d8e0-138">INPUTS</span></span>

### <span data-ttu-id="0d8e0-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d8e0-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="0d8e0-140">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d8e0-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="0d8e0-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d8e0-141">OUTPUTS</span></span>

### <span data-ttu-id="0d8e0-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d8e0-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0d8e0-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d8e0-143">NOTES</span></span>

## <span data-ttu-id="0d8e0-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d8e0-144">RELATED LINKS</span></span>
