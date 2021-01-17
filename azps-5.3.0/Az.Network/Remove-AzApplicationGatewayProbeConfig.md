---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472213"
---
# <span data-ttu-id="3b5aa-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3b5aa-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="3b5aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5aa-103">Entfernt einen Integritätstest aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="3b5aa-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="3b5aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b5aa-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b5aa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b5aa-105">DESCRIPTION</span></span>
<span data-ttu-id="3b5aa-106">Das Remove-AzApplicationGatewayProbeConfig cmdlet entfernt eine Wärmeprobe von einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="3b5aa-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="3b5aa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b5aa-107">EXAMPLES</span></span>

### <span data-ttu-id="3b5aa-108">Beispiel 1: Entfernen einer Integritätsprobe von einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="3b5aa-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="3b5aa-109">Mit diesem Befehl wird der Integritätstest namens "Probe04" aus dem Anwendungsgateway namens "Gateway" entfernt.</span><span class="sxs-lookup"><span data-stu-id="3b5aa-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="3b5aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b5aa-110">PARAMETERS</span></span>

### <span data-ttu-id="3b5aa-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b5aa-111">-ApplicationGateway</span></span>
<span data-ttu-id="3b5aa-112">Gibt das Anwendungsgateway an, zu dem dieses Cmdlet eine Sonde entfernt.</span><span class="sxs-lookup"><span data-stu-id="3b5aa-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="3b5aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5aa-113">-DefaultProfile</span></span>
<span data-ttu-id="3b5aa-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b5aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b5aa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3b5aa-115">-Name</span></span>
<span data-ttu-id="3b5aa-116">Gibt den Namen der Sonde an, für die dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3b5aa-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5aa-117">CommonParameters</span></span>
<span data-ttu-id="3b5aa-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b5aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5aa-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b5aa-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5aa-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b5aa-120">INPUTS</span></span>

### <span data-ttu-id="3b5aa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b5aa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3b5aa-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b5aa-122">OUTPUTS</span></span>

### <span data-ttu-id="3b5aa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b5aa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3b5aa-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3b5aa-124">NOTES</span></span>

## <span data-ttu-id="3b5aa-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3b5aa-125">RELATED LINKS</span></span>

[<span data-ttu-id="3b5aa-126">Entfernen eines Prüfpunkts von einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="3b5aa-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="3b5aa-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3b5aa-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="3b5aa-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3b5aa-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="3b5aa-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3b5aa-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="3b5aa-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3b5aa-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

