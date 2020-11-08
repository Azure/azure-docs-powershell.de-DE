---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: b6bfe8b7064324dea353543e0e9debe77e4b2edd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004994"
---
# <span data-ttu-id="6cd10-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cd10-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="6cd10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cd10-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd10-103">Erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6cd10-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="6cd10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cd10-104">SYNTAX</span></span>

### <span data-ttu-id="6cd10-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6cd10-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cd10-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6cd10-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cd10-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="6cd10-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cd10-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cd10-108">DESCRIPTION</span></span>
<span data-ttu-id="6cd10-109">**Das Cmdlet New-AzApplicationGatewayRedirectConfiguration** erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6cd10-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="6cd10-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cd10-110">EXAMPLES</span></span>

### <span data-ttu-id="6cd10-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6cd10-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="6cd10-112">Dieser Befehl erstellt eine Umleitungs Konfiguration mit dem Namen Redirect01 und speichert das Ergebnis in der Variablen mit dem Namen $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="6cd10-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="6cd10-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cd10-113">PARAMETERS</span></span>

### <span data-ttu-id="6cd10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd10-114">-DefaultProfile</span></span>
<span data-ttu-id="6cd10-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cd10-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cd10-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="6cd10-116">-IncludePath</span></span>
<span data-ttu-id="6cd10-117">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="6cd10-117">Include path in the redirected url.</span></span>
<span data-ttu-id="6cd10-118">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="6cd10-118">Default is true.</span></span>

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

### <span data-ttu-id="6cd10-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="6cd10-119">-IncludeQueryString</span></span>
<span data-ttu-id="6cd10-120">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="6cd10-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="6cd10-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="6cd10-121">Default is true.</span></span>

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

### <span data-ttu-id="6cd10-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6cd10-122">-Name</span></span>
<span data-ttu-id="6cd10-123">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="6cd10-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="6cd10-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="6cd10-124">-RedirectType</span></span>
<span data-ttu-id="6cd10-125">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="6cd10-125">The type of redirect</span></span>

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

### <span data-ttu-id="6cd10-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="6cd10-126">-TargetListener</span></span>
<span data-ttu-id="6cd10-127">HTTP-Listener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="6cd10-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="6cd10-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="6cd10-128">-TargetListenerID</span></span>
<span data-ttu-id="6cd10-129">Die ID des HTTP-Listeners zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="6cd10-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="6cd10-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="6cd10-130">-TargetUrl</span></span>
<span data-ttu-id="6cd10-131">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="6cd10-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="6cd10-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd10-132">CommonParameters</span></span>
<span data-ttu-id="6cd10-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd10-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd10-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd10-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd10-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cd10-135">INPUTS</span></span>

### <span data-ttu-id="6cd10-136">Keine</span><span class="sxs-lookup"><span data-stu-id="6cd10-136">None</span></span>

## <span data-ttu-id="6cd10-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cd10-137">OUTPUTS</span></span>

### <span data-ttu-id="6cd10-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cd10-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="6cd10-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cd10-139">NOTES</span></span>

## <span data-ttu-id="6cd10-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cd10-140">RELATED LINKS</span></span>

[<span data-ttu-id="6cd10-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cd10-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="6cd10-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cd10-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="6cd10-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cd10-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="6cd10-144">Satz-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cd10-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
