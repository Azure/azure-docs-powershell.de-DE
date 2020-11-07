---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 88ca18eca50f1e68eab8599ad79f902ff1fd2551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662996"
---
# <span data-ttu-id="89b68-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89b68-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="89b68-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89b68-102">SYNOPSIS</span></span>
<span data-ttu-id="89b68-103">Startet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="89b68-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89b68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89b68-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89b68-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89b68-105">DESCRIPTION</span></span>
<span data-ttu-id="89b68-106">Das **Start-AzureRmApplicationGateway-** Cmdlet startet ein Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="89b68-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="89b68-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89b68-107">EXAMPLES</span></span>

### <span data-ttu-id="89b68-108">Beispiel1: Starten eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="89b68-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="89b68-109">Mit diesem Befehl wird das in der $AppGw-Variable gespeicherte Anwendungsgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="89b68-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="89b68-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="89b68-110">PARAMETERS</span></span>

### <span data-ttu-id="89b68-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89b68-111">-ApplicationGateway</span></span>
<span data-ttu-id="89b68-112">Gibt das Anwendungsgateway an, das mit diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="89b68-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="89b68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b68-113">-DefaultProfile</span></span>
<span data-ttu-id="89b68-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89b68-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89b68-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b68-115">CommonParameters</span></span>
<span data-ttu-id="89b68-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b68-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b68-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89b68-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b68-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89b68-118">INPUTS</span></span>

### <span data-ttu-id="89b68-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89b68-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="89b68-120">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89b68-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="89b68-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89b68-121">OUTPUTS</span></span>

### <span data-ttu-id="89b68-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89b68-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="89b68-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="89b68-123">NOTES</span></span>

## <span data-ttu-id="89b68-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89b68-124">RELATED LINKS</span></span>

[<span data-ttu-id="89b68-125">Stopp-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89b68-125">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


