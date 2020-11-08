---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178317"
---
# <span data-ttu-id="d2bf5-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2bf5-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d2bf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="d2bf5-103">Entfernt einen Front-End-Port von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d2bf5-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="d2bf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2bf5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2bf5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="d2bf5-106">Mit dem Cmdlet **Remove-AzApplicationGatewayFrontendPort** wird ein Front-End-Port aus einem Azure Application Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="d2bf5-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="d2bf5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="d2bf5-108">Beispiel: Entfernen eines Front-End-Ports von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="d2bf5-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="d2bf5-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert das Gateway in $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="d2bf5-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="d2bf5-110">Der zweite Befehl entfernt den Port mit dem Namen FrontEndPort02 aus dem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d2bf5-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="d2bf5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2bf5-111">PARAMETERS</span></span>

### <span data-ttu-id="d2bf5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2bf5-112">-ApplicationGateway</span></span>
<span data-ttu-id="d2bf5-113">Gibt das Anwendungsgateway an, aus dem ein Front-End-Port entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2bf5-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="d2bf5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2bf5-114">-DefaultProfile</span></span>
<span data-ttu-id="d2bf5-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2bf5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2bf5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d2bf5-116">-Name</span></span>
<span data-ttu-id="d2bf5-117">Gibt den Namen des zu entfernenden Frontend-Ports an.</span><span class="sxs-lookup"><span data-stu-id="d2bf5-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="d2bf5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2bf5-118">CommonParameters</span></span>
<span data-ttu-id="d2bf5-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2bf5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2bf5-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2bf5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2bf5-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2bf5-121">INPUTS</span></span>

### <span data-ttu-id="d2bf5-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2bf5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d2bf5-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2bf5-123">OUTPUTS</span></span>

### <span data-ttu-id="d2bf5-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2bf5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d2bf5-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2bf5-125">NOTES</span></span>

## <span data-ttu-id="d2bf5-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2bf5-126">RELATED LINKS</span></span>

[<span data-ttu-id="d2bf5-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2bf5-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d2bf5-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2bf5-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d2bf5-129">Neu – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2bf5-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d2bf5-130">Satz-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2bf5-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


