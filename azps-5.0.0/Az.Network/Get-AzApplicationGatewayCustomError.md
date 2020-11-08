---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178553"
---
# <span data-ttu-id="3507f-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3507f-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3507f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3507f-102">SYNOPSIS</span></span>
<span data-ttu-id="3507f-103">Ruft benutzerdefinierte Fehler (e) von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="3507f-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="3507f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3507f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3507f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3507f-105">DESCRIPTION</span></span>
<span data-ttu-id="3507f-106">Das Cmdlet " **Get-AzApplicationGatewayCustomError** " Ruft benutzerdefinierte Fehler (e) von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="3507f-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="3507f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3507f-107">EXAMPLES</span></span>

### <span data-ttu-id="3507f-108">Beispiel 1: Ruft einen benutzerdefinierten Fehler in einem Anwendungsgateway ab</span><span class="sxs-lookup"><span data-stu-id="3507f-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="3507f-109">Dieser Befehl ruft den benutzerdefinierten Fehler des HTTP-Statuscodes 502 aus dem Application Gateway $appgw ab und gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="3507f-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="3507f-110">Beispiel 2: Ruft die Liste aller benutzerdefinierten Fehler in einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="3507f-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="3507f-111">Dieser Befehl ruft die Liste aller benutzerdefinierten Fehler aus dem Application Gateway $appgw ab und gibt diese zurück.</span><span class="sxs-lookup"><span data-stu-id="3507f-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="3507f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3507f-112">PARAMETERS</span></span>

### <span data-ttu-id="3507f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3507f-113">-ApplicationGateway</span></span>
<span data-ttu-id="3507f-114">Das Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="3507f-114">The Application Gateway</span></span>

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

### <span data-ttu-id="3507f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3507f-115">-DefaultProfile</span></span>
<span data-ttu-id="3507f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3507f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3507f-117">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="3507f-117">-StatusCode</span></span>
<span data-ttu-id="3507f-118">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="3507f-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3507f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3507f-119">CommonParameters</span></span>
<span data-ttu-id="3507f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3507f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3507f-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3507f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3507f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3507f-122">INPUTS</span></span>

### <span data-ttu-id="3507f-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3507f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3507f-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3507f-124">OUTPUTS</span></span>

### <span data-ttu-id="3507f-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3507f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3507f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="3507f-126">NOTES</span></span>

## <span data-ttu-id="3507f-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3507f-127">RELATED LINKS</span></span>

[<span data-ttu-id="3507f-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3507f-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3507f-129">Neu – AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3507f-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3507f-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3507f-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3507f-131">Satz-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3507f-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
