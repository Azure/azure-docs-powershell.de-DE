---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: de019ffd1bc3be0e66cef6e8a15912f18b05f770
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850740"
---
# <span data-ttu-id="5b014-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b014-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="5b014-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b014-102">SYNOPSIS</span></span>
<span data-ttu-id="5b014-103">Ruft die Anforderungs Routingregel eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="5b014-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b014-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b014-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b014-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b014-105">DESCRIPTION</span></span>
<span data-ttu-id="5b014-106">Das Cmdlet " **Get-AzureRmApplicationGatewayRequestRoutingRule** " Ruft die Anforderungs Routingregel eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="5b014-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="5b014-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b014-107">EXAMPLES</span></span>

### <span data-ttu-id="5b014-108">Beispiel 1: Abrufen einer bestimmten Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="5b014-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="5b014-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5b014-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5b014-110">Der zweite Befehl ruft die Anforderungs Routingregel mit dem Namen Rule01 aus dem Anwendungs Gateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5b014-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="5b014-111">Beispiel 2: Abrufen einer Liste mit Anforderungs Routingregeln</span><span class="sxs-lookup"><span data-stu-id="5b014-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="5b014-112">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5b014-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5b014-113">Der zweite Befehl ruft eine Liste der Anforderungs Routingregeln aus dem Anwendungs Gateway ab, die in der Variablen mit dem Namen $AppGW gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="5b014-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="5b014-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b014-114">PARAMETERS</span></span>

### <span data-ttu-id="5b014-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b014-115">-ApplicationGateway</span></span>
<span data-ttu-id="5b014-116">Gibt das Application Gateway-Objekt an, das die Anforderungs Routingregel enthält.</span><span class="sxs-lookup"><span data-stu-id="5b014-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="5b014-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b014-117">-DefaultProfile</span></span>
<span data-ttu-id="5b014-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b014-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b014-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5b014-119">-Name</span></span>
<span data-ttu-id="5b014-120">Gibt den Namen der Anforderungs Routingregel an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5b014-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b014-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b014-121">CommonParameters</span></span>
<span data-ttu-id="5b014-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b014-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b014-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b014-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b014-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b014-124">INPUTS</span></span>

### <span data-ttu-id="5b014-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5b014-125">System.String</span></span>

## <span data-ttu-id="5b014-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b014-126">OUTPUTS</span></span>

### <span data-ttu-id="5b014-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b014-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="5b014-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b014-128">NOTES</span></span>

## <span data-ttu-id="5b014-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b014-129">RELATED LINKS</span></span>

[<span data-ttu-id="5b014-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b014-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5b014-131">Neu – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b014-131">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5b014-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b014-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5b014-133">Satz-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b014-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


