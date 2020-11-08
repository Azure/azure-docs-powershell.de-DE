---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009087"
---
# <span data-ttu-id="6de19-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6de19-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6de19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6de19-102">SYNOPSIS</span></span>
<span data-ttu-id="6de19-103">Entfernt eine Anforderungs Routingregel von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6de19-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="6de19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6de19-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6de19-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6de19-105">DESCRIPTION</span></span>
<span data-ttu-id="6de19-106">Das Cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** entfernt eine Anforderungs Routingregel von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6de19-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="6de19-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6de19-107">EXAMPLES</span></span>

### <span data-ttu-id="6de19-108">Beispiel 1: Entfernen einer Anforderungs Routingregel von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="6de19-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="6de19-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6de19-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6de19-110">Der zweite Befehl entfernt die Anforderungs Routingregel mit dem Namen Rule02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="6de19-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="6de19-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6de19-111">PARAMETERS</span></span>

### <span data-ttu-id="6de19-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6de19-112">-ApplicationGateway</span></span>
<span data-ttu-id="6de19-113">Gibt das Anwendungsgateway an, aus dem eine Anforderungs Routingregel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6de19-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="6de19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de19-114">-DefaultProfile</span></span>
<span data-ttu-id="6de19-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6de19-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de19-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6de19-116">-Name</span></span>
<span data-ttu-id="6de19-117">Gibt den Namen der Anforderungs Routingregel an, für die dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6de19-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="6de19-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de19-118">CommonParameters</span></span>
<span data-ttu-id="6de19-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de19-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de19-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de19-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de19-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6de19-121">INPUTS</span></span>

### <span data-ttu-id="6de19-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6de19-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6de19-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6de19-123">OUTPUTS</span></span>

### <span data-ttu-id="6de19-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6de19-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6de19-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="6de19-125">NOTES</span></span>

## <span data-ttu-id="6de19-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6de19-126">RELATED LINKS</span></span>

[<span data-ttu-id="6de19-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6de19-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6de19-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6de19-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6de19-129">Neu – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6de19-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6de19-130">Satz-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6de19-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


