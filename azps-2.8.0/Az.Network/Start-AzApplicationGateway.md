---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: f90e35e0b8a88d7fa7b5089adf205bf6fe14e18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823763"
---
# <span data-ttu-id="8b088-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b088-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="8b088-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b088-102">SYNOPSIS</span></span>
<span data-ttu-id="8b088-103">Startet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8b088-103">Starts an application gateway.</span></span>

## <span data-ttu-id="8b088-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b088-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b088-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b088-105">DESCRIPTION</span></span>
<span data-ttu-id="8b088-106">Das **Start-AzApplicationGateway-** Cmdlet startet ein Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8b088-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="8b088-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b088-107">EXAMPLES</span></span>

### <span data-ttu-id="8b088-108">Beispiel1: Starten eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="8b088-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="8b088-109">Mit diesem Befehl wird das in der $AppGw-Variable gespeicherte Anwendungsgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="8b088-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="8b088-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b088-110">PARAMETERS</span></span>

### <span data-ttu-id="8b088-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b088-111">-ApplicationGateway</span></span>
<span data-ttu-id="8b088-112">Gibt das Anwendungsgateway an, das mit diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8b088-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8b088-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b088-113">-DefaultProfile</span></span>
<span data-ttu-id="8b088-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b088-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b088-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b088-115">CommonParameters</span></span>
<span data-ttu-id="8b088-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b088-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b088-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b088-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b088-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b088-118">INPUTS</span></span>

### <span data-ttu-id="8b088-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b088-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b088-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b088-120">OUTPUTS</span></span>

### <span data-ttu-id="8b088-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b088-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b088-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b088-122">NOTES</span></span>

## <span data-ttu-id="8b088-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b088-123">RELATED LINKS</span></span>

[<span data-ttu-id="8b088-124">Stopp-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b088-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


