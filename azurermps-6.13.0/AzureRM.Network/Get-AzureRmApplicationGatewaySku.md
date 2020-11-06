---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 5d0409ae5be910f2e4480ac61f36d907e7736f0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501145"
---
# <span data-ttu-id="ddfb4-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ddfb4-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="ddfb4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ddfb4-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfb4-103">Ruft die SKU eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="ddfb4-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddfb4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddfb4-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddfb4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ddfb4-105">DESCRIPTION</span></span>
<span data-ttu-id="ddfb4-106">Das Cmdlet " **Get-AzureRmApplicationGatewaySku** " Ruft die Lagerhaltungs Einheit (SKU) eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="ddfb4-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="ddfb4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddfb4-107">EXAMPLES</span></span>

### <span data-ttu-id="ddfb4-108">Beispiel 1: Abrufen einer SKU für das Anwendungs-Gateway</span><span class="sxs-lookup"><span data-stu-id="ddfb4-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="ddfb4-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="ddfb4-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="ddfb4-110">Der zweite Befehl ruft die SKU eines Anwendungs Gateways mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $SKU.</span><span class="sxs-lookup"><span data-stu-id="ddfb4-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="ddfb4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddfb4-111">PARAMETERS</span></span>

### <span data-ttu-id="ddfb4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddfb4-112">-ApplicationGateway</span></span>
<span data-ttu-id="ddfb4-113">Gibt das Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ddfb4-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="ddfb4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfb4-114">-DefaultProfile</span></span>
<span data-ttu-id="ddfb4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ddfb4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddfb4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfb4-116">CommonParameters</span></span>
<span data-ttu-id="ddfb4-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddfb4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfb4-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddfb4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfb4-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ddfb4-119">INPUTS</span></span>

### <span data-ttu-id="ddfb4-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddfb4-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="ddfb4-121">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ddfb4-121">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="ddfb4-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ddfb4-122">OUTPUTS</span></span>

### <span data-ttu-id="ddfb4-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ddfb4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="ddfb4-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="ddfb4-124">NOTES</span></span>

## <span data-ttu-id="ddfb4-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ddfb4-125">RELATED LINKS</span></span>

[<span data-ttu-id="ddfb4-126">Neu – AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ddfb4-126">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="ddfb4-127">Satz-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ddfb4-127">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


