---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849919"
---
# <span data-ttu-id="1bed3-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bed3-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="1bed3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bed3-102">SYNOPSIS</span></span>
<span data-ttu-id="1bed3-103">Startet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="1bed3-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bed3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bed3-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bed3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bed3-105">DESCRIPTION</span></span>
<span data-ttu-id="1bed3-106">Das **Start-AzureRmApplicationGateway-** Cmdlet startet ein Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1bed3-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="1bed3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bed3-107">EXAMPLES</span></span>

### <span data-ttu-id="1bed3-108">Beispiel1: Starten eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="1bed3-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="1bed3-109">Mit diesem Befehl wird das in der $AppGw-Variable gespeicherte Anwendungsgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="1bed3-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="1bed3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bed3-110">PARAMETERS</span></span>

### <span data-ttu-id="1bed3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bed3-111">-ApplicationGateway</span></span>
<span data-ttu-id="1bed3-112">Gibt das Anwendungsgateway an, das mit diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1bed3-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="1bed3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bed3-113">-DefaultProfile</span></span>
<span data-ttu-id="1bed3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1bed3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bed3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bed3-115">CommonParameters</span></span>
<span data-ttu-id="1bed3-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bed3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bed3-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bed3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bed3-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bed3-118">INPUTS</span></span>

### <span data-ttu-id="1bed3-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1bed3-119">System.String</span></span>

## <span data-ttu-id="1bed3-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bed3-120">OUTPUTS</span></span>

### <span data-ttu-id="1bed3-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bed3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1bed3-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bed3-122">NOTES</span></span>

## <span data-ttu-id="1bed3-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bed3-123">RELATED LINKS</span></span>

[<span data-ttu-id="1bed3-124">Stopp-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bed3-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


