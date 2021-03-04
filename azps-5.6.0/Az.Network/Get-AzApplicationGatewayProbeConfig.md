---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 1bdee7a9ffb35085f8194d86dc9a9486f5dd7fb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940355"
---
# <span data-ttu-id="0d5cc-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cc-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0d5cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5cc-103">Ruft eine vorhandene Integritätstestkonfiguration aus einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="0d5cc-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="0d5cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d5cc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d5cc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d5cc-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5cc-106">Das Get-AzApplicationGatewayProbeConfig-Cmdlet ruft eine vorhandene Integritätstestkonfiguration aus einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="0d5cc-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="0d5cc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d5cc-107">EXAMPLES</span></span>

### <span data-ttu-id="0d5cc-108">Beispiel 1: Erhalten eines vorhandenen Prüfpunkts aus einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0d5cc-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="0d5cc-109">Dieser Befehl ruft den Integritätstest mit dem Namen Probe02 aus dem Anwendungsgateway mit dem Namen Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="0d5cc-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="0d5cc-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0d5cc-110">PARAMETERS</span></span>

### <span data-ttu-id="0d5cc-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d5cc-111">-ApplicationGateway</span></span>
<span data-ttu-id="0d5cc-112">Gibt das Anwendungsgateway an, zu dem dieses Cmdlet eine Prüfpunktkonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="0d5cc-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="0d5cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5cc-113">-DefaultProfile</span></span>
<span data-ttu-id="0d5cc-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d5cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d5cc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0d5cc-115">-Name</span></span>
<span data-ttu-id="0d5cc-116">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="0d5cc-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="0d5cc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5cc-117">CommonParameters</span></span>
<span data-ttu-id="0d5cc-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d5cc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5cc-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d5cc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5cc-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d5cc-120">INPUTS</span></span>

### <span data-ttu-id="0d5cc-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d5cc-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0d5cc-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d5cc-122">OUTPUTS</span></span>

### <span data-ttu-id="0d5cc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="0d5cc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="0d5cc-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0d5cc-124">NOTES</span></span>

## <span data-ttu-id="0d5cc-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0d5cc-125">RELATED LINKS</span></span>

[<span data-ttu-id="0d5cc-126">Hinzufügen eines Prüfpunkts zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0d5cc-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="0d5cc-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cc-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0d5cc-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cc-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0d5cc-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cc-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0d5cc-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cc-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

