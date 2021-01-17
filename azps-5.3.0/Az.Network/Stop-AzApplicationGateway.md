---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472126"
---
# <span data-ttu-id="b5fd5-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="b5fd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fd5-103">Beendet ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-103">Stops an application gateway</span></span>

## <span data-ttu-id="b5fd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5fd5-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5fd5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5fd5-105">DESCRIPTION</span></span>
<span data-ttu-id="b5fd5-106">Das **Cmdlet "Stop-AzApplicationGateway"** beendet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="b5fd5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5fd5-107">EXAMPLES</span></span>

### <span data-ttu-id="b5fd5-108">Beispiel 1: Beenden eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="b5fd5-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="b5fd5-109">Mit diesem Befehl wird das Anwendungsgateway beendet, das in der Variablen $AppGw ist.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="b5fd5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5fd5-110">PARAMETERS</span></span>

### <span data-ttu-id="b5fd5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-111">-ApplicationGateway</span></span>
<span data-ttu-id="b5fd5-112">Gibt das Anwendungsgateway an, das dieses Cmdlet beendet.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b5fd5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5fd5-113">-AsJob</span></span>
<span data-ttu-id="b5fd5-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b5fd5-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fd5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fd5-115">-DefaultProfile</span></span>
<span data-ttu-id="b5fd5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5fd5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fd5-117">CommonParameters</span></span>
<span data-ttu-id="b5fd5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fd5-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5fd5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fd5-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5fd5-120">INPUTS</span></span>

### <span data-ttu-id="b5fd5-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b5fd5-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5fd5-122">OUTPUTS</span></span>

### <span data-ttu-id="b5fd5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b5fd5-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b5fd5-124">NOTES</span></span>

## <span data-ttu-id="b5fd5-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b5fd5-125">RELATED LINKS</span></span>

[<span data-ttu-id="b5fd5-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="b5fd5-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="b5fd5-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="b5fd5-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="b5fd5-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5fd5-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


