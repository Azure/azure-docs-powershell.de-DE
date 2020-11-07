---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 0df6ae98692b7497448b0d3f15e88f1a18a87ae8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660954"
---
# <span data-ttu-id="c67b2-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c67b2-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c67b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c67b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c67b2-103">Fügt einen benutzerdefinierten Fehler zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="c67b2-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="c67b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c67b2-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c67b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c67b2-105">DESCRIPTION</span></span>
<span data-ttu-id="c67b2-106">Mit dem Cmdlet **Add-AzApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c67b2-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="c67b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c67b2-107">EXAMPLES</span></span>

### <span data-ttu-id="c67b2-108">Beispiel 1: Hinzufügen von benutzerdefiniertem Fehler zu Application Gateway Level</span><span class="sxs-lookup"><span data-stu-id="c67b2-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="c67b2-109">Dieser Befehl fügt dem Application Gateway $appgw einen benutzerdefinierten Fehler des HTTP-Statuscodes 502 hinzu und gibt das aktualisierte Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="c67b2-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="c67b2-110">Beispiel 2: Hinzufügen eines benutzerdefinierten Fehlers zu Application Gateway Listener-Ebene</span><span class="sxs-lookup"><span data-stu-id="c67b2-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
PS C:\> $resourceGroup = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $listenerName = "listenerName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $rg
PS C:\> $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
PS C:\> $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="c67b2-111">Mit diesem Befehl wird dem Application Gateway-$appgw auf der Listener-Ebene ein benutzerdefinierter Fehler des HTTP-Statuscodes 502 hinzugefügt, und das aktualisierte Gateway wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c67b2-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="c67b2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c67b2-112">PARAMETERS</span></span>

### <span data-ttu-id="c67b2-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c67b2-113">-ApplicationGateway</span></span>
<span data-ttu-id="c67b2-114">Das Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="c67b2-114">The Application Gateway</span></span>

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

### <span data-ttu-id="c67b2-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="c67b2-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="c67b2-116">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="c67b2-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c67b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c67b2-117">-DefaultProfile</span></span>
<span data-ttu-id="c67b2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c67b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c67b2-119">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="c67b2-119">-StatusCode</span></span>
<span data-ttu-id="c67b2-120">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="c67b2-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c67b2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c67b2-121">CommonParameters</span></span>
<span data-ttu-id="c67b2-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c67b2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c67b2-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c67b2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c67b2-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c67b2-124">INPUTS</span></span>

### <span data-ttu-id="c67b2-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c67b2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c67b2-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c67b2-126">OUTPUTS</span></span>

### <span data-ttu-id="c67b2-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c67b2-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c67b2-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c67b2-128">NOTES</span></span>

## <span data-ttu-id="c67b2-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c67b2-129">RELATED LINKS</span></span>

[<span data-ttu-id="c67b2-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c67b2-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c67b2-131">Neu – AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c67b2-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c67b2-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c67b2-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c67b2-133">Satz-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c67b2-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
