---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151369"
---
# <span data-ttu-id="992fa-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="992fa-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="992fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="992fa-102">SYNOPSIS</span></span>
<span data-ttu-id="992fa-103">Startet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="992fa-103">Starts an application gateway.</span></span>

## <span data-ttu-id="992fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="992fa-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="992fa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="992fa-105">DESCRIPTION</span></span>
<span data-ttu-id="992fa-106">Das **Cmdlet "Start-AzApplicationGateway"** startet ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="992fa-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="992fa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="992fa-107">EXAMPLES</span></span>

### <span data-ttu-id="992fa-108">Beispiel1: Starten eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="992fa-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="992fa-109">Mit diesem Befehl wird das Anwendungsgateway gestartet, das in der Variablen $AppGw ist.</span><span class="sxs-lookup"><span data-stu-id="992fa-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="992fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="992fa-110">PARAMETERS</span></span>

### <span data-ttu-id="992fa-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="992fa-111">-ApplicationGateway</span></span>
<span data-ttu-id="992fa-112">Gibt das Anwendungsgateway an, das dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="992fa-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="992fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992fa-113">-DefaultProfile</span></span>
<span data-ttu-id="992fa-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="992fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="992fa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992fa-115">CommonParameters</span></span>
<span data-ttu-id="992fa-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992fa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992fa-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="992fa-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992fa-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="992fa-118">INPUTS</span></span>

### <span data-ttu-id="992fa-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="992fa-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="992fa-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="992fa-120">OUTPUTS</span></span>

### <span data-ttu-id="992fa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="992fa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="992fa-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="992fa-122">NOTES</span></span>

## <span data-ttu-id="992fa-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="992fa-123">RELATED LINKS</span></span>

[<span data-ttu-id="992fa-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="992fa-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


