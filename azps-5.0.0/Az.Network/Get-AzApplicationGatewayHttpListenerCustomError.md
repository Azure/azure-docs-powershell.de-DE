---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180207"
---
# <span data-ttu-id="5b28e-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5b28e-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="5b28e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b28e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b28e-103">Ruft benutzerdefinierte Fehler (en) aus einem HTTP-Listener eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="5b28e-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="5b28e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b28e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b28e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b28e-105">DESCRIPTION</span></span>
<span data-ttu-id="5b28e-106">Das Cmdlet " **Get-AzApplicationGatewayCustomError** " Ruft benutzerdefinierte Fehler (en) aus einem HTTP-Listener eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="5b28e-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="5b28e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b28e-107">EXAMPLES</span></span>

### <span data-ttu-id="5b28e-108">Beispiel 1: Ruft einen benutzerdefinierten Fehler in einem HTTP-Listener ab</span><span class="sxs-lookup"><span data-stu-id="5b28e-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="5b28e-109">Dieser Befehl ruft den benutzerdefinierten Fehler des HTTP-Statuscodes 502 vom HTTP-Listener ab $Listener 01 ab und gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="5b28e-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="5b28e-110">Beispiel 2: Ruft die Liste aller benutzerdefinierten Fehler in einem HTTP-Listener ab</span><span class="sxs-lookup"><span data-stu-id="5b28e-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="5b28e-111">Dieser Befehl ruft die Liste aller benutzerdefinierten Fehler vom HTTP-Listener $Listener 01 ab und gibt diese zurück.</span><span class="sxs-lookup"><span data-stu-id="5b28e-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="5b28e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b28e-112">PARAMETERS</span></span>

### <span data-ttu-id="5b28e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b28e-113">-DefaultProfile</span></span>
<span data-ttu-id="5b28e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b28e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b28e-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="5b28e-115">-HttpListener</span></span>
<span data-ttu-id="5b28e-116">Der HTTP-Listener für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5b28e-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b28e-117">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="5b28e-117">-StatusCode</span></span>
<span data-ttu-id="5b28e-118">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="5b28e-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b28e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b28e-119">CommonParameters</span></span>
<span data-ttu-id="5b28e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b28e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b28e-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b28e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b28e-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b28e-122">INPUTS</span></span>

### <span data-ttu-id="5b28e-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5b28e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5b28e-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b28e-124">OUTPUTS</span></span>

### <span data-ttu-id="5b28e-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5b28e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="5b28e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b28e-126">NOTES</span></span>

## <span data-ttu-id="5b28e-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b28e-127">RELATED LINKS</span></span>

[<span data-ttu-id="5b28e-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5b28e-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="5b28e-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5b28e-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="5b28e-130">Satz-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5b28e-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
