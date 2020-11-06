---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: a4c1710ebbdfad1afb428bb09cccf27865c5e56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482274"
---
# <span data-ttu-id="5ce42-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5ce42-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="5ce42-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ce42-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce42-103">Entfernt eine Anforderungs Routingregel von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5ce42-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ce42-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ce42-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ce42-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ce42-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce42-106">Das Cmdlet **Remove-AzureRmApplicationGatewayRequestRoutingRule** entfernt eine Anforderungs Routingregel von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5ce42-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="5ce42-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ce42-107">EXAMPLES</span></span>

### <span data-ttu-id="5ce42-108">Beispiel 1: Entfernen einer Anforderungs Routingregel von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="5ce42-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="5ce42-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ce42-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5ce42-110">Der zweite Befehl entfernt die Anforderungs Routingregel mit dem Namen Rule02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5ce42-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="5ce42-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ce42-111">PARAMETERS</span></span>

### <span data-ttu-id="5ce42-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ce42-112">-ApplicationGateway</span></span>
<span data-ttu-id="5ce42-113">Gibt das Anwendungsgateway an, aus dem eine Anforderungs Routingregel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ce42-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="5ce42-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce42-114">-DefaultProfile</span></span>
<span data-ttu-id="5ce42-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ce42-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ce42-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5ce42-116">-Name</span></span>
<span data-ttu-id="5ce42-117">Gibt den Namen der Anforderungs Routingregel an, für die dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5ce42-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="5ce42-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce42-118">CommonParameters</span></span>
<span data-ttu-id="5ce42-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce42-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce42-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ce42-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce42-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ce42-121">INPUTS</span></span>

### <span data-ttu-id="5ce42-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ce42-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="5ce42-123">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ce42-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="5ce42-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ce42-124">OUTPUTS</span></span>

### <span data-ttu-id="5ce42-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5ce42-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="5ce42-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ce42-126">NOTES</span></span>

## <span data-ttu-id="5ce42-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ce42-127">RELATED LINKS</span></span>

[<span data-ttu-id="5ce42-128">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5ce42-128">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5ce42-129">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5ce42-129">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5ce42-130">Neu – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5ce42-130">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5ce42-131">Satz-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5ce42-131">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


