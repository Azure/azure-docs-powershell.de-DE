---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd99eac2ecd36039685dde53730f250754318bc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822936"
---
# <span data-ttu-id="93123-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="93123-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="93123-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93123-102">SYNOPSIS</span></span>
<span data-ttu-id="93123-103">Entfernt eine Anforderungs Routingregel von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="93123-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="93123-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93123-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93123-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93123-105">DESCRIPTION</span></span>
<span data-ttu-id="93123-106">Das Cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** entfernt eine Anforderungs Routingregel von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="93123-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="93123-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93123-107">EXAMPLES</span></span>

### <span data-ttu-id="93123-108">Beispiel 1: Entfernen einer Anforderungs Routingregel von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="93123-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="93123-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="93123-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="93123-110">Der zweite Befehl entfernt die Anforderungs Routingregel mit dem Namen Rule02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="93123-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="93123-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="93123-111">PARAMETERS</span></span>

### <span data-ttu-id="93123-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93123-112">-ApplicationGateway</span></span>
<span data-ttu-id="93123-113">Gibt das Anwendungsgateway an, aus dem eine Anforderungs Routingregel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="93123-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="93123-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93123-114">-DefaultProfile</span></span>
<span data-ttu-id="93123-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93123-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93123-116">-Name</span><span class="sxs-lookup"><span data-stu-id="93123-116">-Name</span></span>
<span data-ttu-id="93123-117">Gibt den Namen der Anforderungs Routingregel an, für die dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="93123-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="93123-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93123-118">CommonParameters</span></span>
<span data-ttu-id="93123-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93123-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93123-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93123-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93123-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93123-121">INPUTS</span></span>

### <span data-ttu-id="93123-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93123-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93123-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93123-123">OUTPUTS</span></span>

### <span data-ttu-id="93123-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="93123-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="93123-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="93123-125">NOTES</span></span>

## <span data-ttu-id="93123-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93123-126">RELATED LINKS</span></span>

[<span data-ttu-id="93123-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="93123-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="93123-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="93123-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="93123-129">Neu – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="93123-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="93123-130">Satz-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="93123-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


