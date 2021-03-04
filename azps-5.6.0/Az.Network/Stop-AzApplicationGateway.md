---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 0cf179bf02c8590bd5c5e30277c7299c7b13b06b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918547"
---
# <span data-ttu-id="99888-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99888-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="99888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99888-102">SYNOPSIS</span></span>
<span data-ttu-id="99888-103">Stoppt ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="99888-103">Stops an application gateway</span></span>

## <span data-ttu-id="99888-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99888-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99888-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99888-105">DESCRIPTION</span></span>
<span data-ttu-id="99888-106">Das **Cmdlet Stop-AzApplicationGateway** beendet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="99888-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="99888-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99888-107">EXAMPLES</span></span>

### <span data-ttu-id="99888-108">Beispiel 1: Beenden eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="99888-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="99888-109">Mit diesem Befehl wird das In-App-Gateway beendet, das in der $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="99888-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="99888-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="99888-110">PARAMETERS</span></span>

### <span data-ttu-id="99888-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99888-111">-ApplicationGateway</span></span>
<span data-ttu-id="99888-112">Gibt das Anwendungsgateway an, das dieses Cmdlet beendet.</span><span class="sxs-lookup"><span data-stu-id="99888-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="99888-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99888-113">-AsJob</span></span>
<span data-ttu-id="99888-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="99888-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99888-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99888-115">-DefaultProfile</span></span>
<span data-ttu-id="99888-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99888-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99888-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99888-117">CommonParameters</span></span>
<span data-ttu-id="99888-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99888-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99888-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99888-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99888-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99888-120">INPUTS</span></span>

### <span data-ttu-id="99888-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99888-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99888-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99888-122">OUTPUTS</span></span>

### <span data-ttu-id="99888-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99888-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99888-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="99888-124">NOTES</span></span>

## <span data-ttu-id="99888-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="99888-125">RELATED LINKS</span></span>

[<span data-ttu-id="99888-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99888-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="99888-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99888-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="99888-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99888-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="99888-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99888-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="99888-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99888-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


