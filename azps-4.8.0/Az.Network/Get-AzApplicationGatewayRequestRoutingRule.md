---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167202"
---
# <span data-ttu-id="99741-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="99741-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="99741-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99741-102">SYNOPSIS</span></span>
<span data-ttu-id="99741-103">Ruft die Anforderungs Routingregel eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="99741-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="99741-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99741-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99741-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99741-105">DESCRIPTION</span></span>
<span data-ttu-id="99741-106">Das Cmdlet " **Get-AzApplicationGatewayRequestRoutingRule** " Ruft die Anforderungs Routingregel eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="99741-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="99741-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99741-107">EXAMPLES</span></span>

### <span data-ttu-id="99741-108">Beispiel 1: Abrufen einer bestimmten Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="99741-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="99741-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="99741-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="99741-110">Der zweite Befehl ruft die Anforderungs Routingregel mit dem Namen Rule01 aus dem Anwendungs Gateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="99741-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="99741-111">Beispiel 2: Abrufen einer Liste mit Anforderungs Routingregeln</span><span class="sxs-lookup"><span data-stu-id="99741-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="99741-112">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="99741-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="99741-113">Der zweite Befehl ruft eine Liste der Anforderungs Routingregeln aus dem Anwendungs Gateway ab, die in der Variablen mit dem Namen $AppGW gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="99741-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="99741-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="99741-114">PARAMETERS</span></span>

### <span data-ttu-id="99741-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99741-115">-ApplicationGateway</span></span>
<span data-ttu-id="99741-116">Gibt das Application Gateway-Objekt an, das die Anforderungs Routingregel enthält.</span><span class="sxs-lookup"><span data-stu-id="99741-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="99741-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99741-117">-DefaultProfile</span></span>
<span data-ttu-id="99741-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99741-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99741-119">-Name</span><span class="sxs-lookup"><span data-stu-id="99741-119">-Name</span></span>
<span data-ttu-id="99741-120">Gibt den Namen der Anforderungs Routingregel an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="99741-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="99741-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99741-121">CommonParameters</span></span>
<span data-ttu-id="99741-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99741-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99741-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99741-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99741-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99741-124">INPUTS</span></span>

### <span data-ttu-id="99741-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99741-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99741-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99741-126">OUTPUTS</span></span>

### <span data-ttu-id="99741-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="99741-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="99741-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="99741-128">NOTES</span></span>

## <span data-ttu-id="99741-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99741-129">RELATED LINKS</span></span>

[<span data-ttu-id="99741-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="99741-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="99741-131">Neu – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="99741-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="99741-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="99741-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="99741-133">Satz-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="99741-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


