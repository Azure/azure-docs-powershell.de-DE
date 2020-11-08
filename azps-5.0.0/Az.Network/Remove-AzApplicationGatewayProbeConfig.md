---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176176"
---
# <span data-ttu-id="0de2a-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0de2a-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0de2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0de2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0de2a-103">Entfernt einen Integritäts Prüf Punkt aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="0de2a-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="0de2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0de2a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0de2a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0de2a-105">DESCRIPTION</span></span>
<span data-ttu-id="0de2a-106">Das Remove-AzApplicationGatewayProbeConfig-Cmdlet entfernt eine Heath-Sonde aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="0de2a-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="0de2a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0de2a-107">EXAMPLES</span></span>

### <span data-ttu-id="0de2a-108">Beispiel 1: Entfernen einer Integritätsprüfung von einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0de2a-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="0de2a-109">Mit diesem Befehl wird der Integritätstest mit dem Namen Probe04 aus dem Application Gateway mit dem Namen Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="0de2a-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="0de2a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0de2a-110">PARAMETERS</span></span>

### <span data-ttu-id="0de2a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0de2a-111">-ApplicationGateway</span></span>
<span data-ttu-id="0de2a-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet einen Prüfpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="0de2a-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="0de2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de2a-113">-DefaultProfile</span></span>
<span data-ttu-id="0de2a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0de2a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0de2a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0de2a-115">-Name</span></span>
<span data-ttu-id="0de2a-116">Gibt den Namen des Prüfpunkts an, für den dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="0de2a-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="0de2a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de2a-117">CommonParameters</span></span>
<span data-ttu-id="0de2a-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de2a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de2a-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0de2a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de2a-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0de2a-120">INPUTS</span></span>

### <span data-ttu-id="0de2a-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0de2a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0de2a-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0de2a-122">OUTPUTS</span></span>

### <span data-ttu-id="0de2a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0de2a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0de2a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="0de2a-124">NOTES</span></span>

## <span data-ttu-id="0de2a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0de2a-125">RELATED LINKS</span></span>

[<span data-ttu-id="0de2a-126">Entfernen eines Prüfpunkts aus einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0de2a-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="0de2a-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0de2a-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0de2a-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0de2a-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0de2a-129">Neu – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0de2a-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0de2a-130">Satz-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0de2a-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

