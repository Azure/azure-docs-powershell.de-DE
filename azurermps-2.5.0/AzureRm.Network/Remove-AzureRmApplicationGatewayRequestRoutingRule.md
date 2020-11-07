---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 859ef684424069bb5fc4c5b45de3e722f0921705
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848748"
---
# <span data-ttu-id="f9835-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9835-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f9835-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9835-102">SYNOPSIS</span></span>
<span data-ttu-id="f9835-103">Entfernt eine Anforderungs Routingregel von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f9835-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9835-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9835-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9835-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9835-105">DESCRIPTION</span></span>
<span data-ttu-id="f9835-106">Das Cmdlet **Remove-AzureRmApplicationGatewayRequestRoutingRule** entfernt eine Anforderungs Routingregel von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f9835-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="f9835-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9835-107">EXAMPLES</span></span>

### <span data-ttu-id="f9835-108">Beispiel 1: Entfernen einer Anforderungs Routingregel von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="f9835-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="f9835-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f9835-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f9835-110">Der zweite Befehl entfernt die Anforderungs Routingregel mit dem Namen Rule02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f9835-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f9835-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9835-111">PARAMETERS</span></span>

### <span data-ttu-id="f9835-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9835-112">-ApplicationGateway</span></span>
<span data-ttu-id="f9835-113">Gibt das Anwendungsgateway an, aus dem eine Anforderungs Routingregel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9835-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="f9835-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9835-114">-DefaultProfile</span></span>
<span data-ttu-id="f9835-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9835-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9835-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f9835-116">-Name</span></span>
<span data-ttu-id="f9835-117">Gibt den Namen der Anforderungs Routingregel an, für die dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f9835-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="f9835-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9835-118">CommonParameters</span></span>
<span data-ttu-id="f9835-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9835-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9835-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9835-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9835-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9835-121">INPUTS</span></span>

### <span data-ttu-id="f9835-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f9835-122">System.String</span></span>

## <span data-ttu-id="f9835-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9835-123">OUTPUTS</span></span>

### <span data-ttu-id="f9835-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9835-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f9835-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9835-125">NOTES</span></span>

## <span data-ttu-id="f9835-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9835-126">RELATED LINKS</span></span>

[<span data-ttu-id="f9835-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9835-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f9835-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9835-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f9835-129">Neu – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9835-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f9835-130">Satz-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9835-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


