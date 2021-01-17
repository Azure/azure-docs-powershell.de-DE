---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291304"
---
# <span data-ttu-id="8319c-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8319c-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="8319c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8319c-102">SYNOPSIS</span></span>
<span data-ttu-id="8319c-103">Ruft eine vorhandene Integritätstestkonfiguration von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="8319c-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="8319c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8319c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8319c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8319c-105">DESCRIPTION</span></span>
<span data-ttu-id="8319c-106">Das Get-AzApplicationGatewayProbeConfig ruft eine vorhandene Integritätstestkonfiguration von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="8319c-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="8319c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8319c-107">EXAMPLES</span></span>

### <span data-ttu-id="8319c-108">Beispiel 1: Erhalten eines vorhandenen Prüfpunkts von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="8319c-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="8319c-109">Dieser Befehl ruft den Integritätstest namens "Probe02" vom Anwendungsgateway namens "Gateway" ab.</span><span class="sxs-lookup"><span data-stu-id="8319c-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="8319c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8319c-110">PARAMETERS</span></span>

### <span data-ttu-id="8319c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8319c-111">-ApplicationGateway</span></span>
<span data-ttu-id="8319c-112">Gibt das Anwendungsgateway an, an das dieses Cmdlet eine Probekonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="8319c-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="8319c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8319c-113">-DefaultProfile</span></span>
<span data-ttu-id="8319c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8319c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8319c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8319c-115">-Name</span></span>
<span data-ttu-id="8319c-116">Gibt den Namen der Sonde an.</span><span class="sxs-lookup"><span data-stu-id="8319c-116">Specifies the name of the probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8319c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8319c-117">CommonParameters</span></span>
<span data-ttu-id="8319c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8319c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8319c-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8319c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8319c-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8319c-120">INPUTS</span></span>

### <span data-ttu-id="8319c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8319c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8319c-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8319c-122">OUTPUTS</span></span>

### <span data-ttu-id="8319c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="8319c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="8319c-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8319c-124">NOTES</span></span>

## <span data-ttu-id="8319c-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8319c-125">RELATED LINKS</span></span>

[<span data-ttu-id="8319c-126">Hinzufügen einer Probe zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="8319c-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="8319c-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8319c-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="8319c-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8319c-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="8319c-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8319c-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="8319c-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8319c-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

