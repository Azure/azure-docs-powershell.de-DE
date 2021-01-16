---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468200"
---
# <span data-ttu-id="0e962-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e962-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0e962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e962-102">SYNOPSIS</span></span>
<span data-ttu-id="0e962-103">Ruft eine vorhandene Integritätstestkonfiguration von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="0e962-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="0e962-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e962-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e962-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e962-105">DESCRIPTION</span></span>
<span data-ttu-id="0e962-106">Das Get-AzApplicationGatewayProbeConfig cmdlet ruft eine vorhandene Integritätstestkonfiguration von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="0e962-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="0e962-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e962-107">EXAMPLES</span></span>

### <span data-ttu-id="0e962-108">Beispiel 1: Erhalten einer vorhandenen Probe von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0e962-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="0e962-109">Dieser Befehl ruft den Integritätstest namens "Probe02" vom Anwendungsgateway namens "Gateway" ab.</span><span class="sxs-lookup"><span data-stu-id="0e962-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="0e962-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e962-110">PARAMETERS</span></span>

### <span data-ttu-id="0e962-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e962-111">-ApplicationGateway</span></span>
<span data-ttu-id="0e962-112">Gibt das Anwendungsgateway an, an das dieses Cmdlet eine Probekonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="0e962-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="0e962-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e962-113">-DefaultProfile</span></span>
<span data-ttu-id="0e962-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e962-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e962-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0e962-115">-Name</span></span>
<span data-ttu-id="0e962-116">Gibt den Namen der Sonde an.</span><span class="sxs-lookup"><span data-stu-id="0e962-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="0e962-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e962-117">CommonParameters</span></span>
<span data-ttu-id="0e962-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e962-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e962-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e962-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e962-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e962-120">INPUTS</span></span>

### <span data-ttu-id="0e962-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e962-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e962-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e962-122">OUTPUTS</span></span>

### <span data-ttu-id="0e962-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="0e962-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="0e962-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0e962-124">NOTES</span></span>

## <span data-ttu-id="0e962-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0e962-125">RELATED LINKS</span></span>

[<span data-ttu-id="0e962-126">Hinzufügen einer Probe zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0e962-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="0e962-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e962-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0e962-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e962-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0e962-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e962-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0e962-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e962-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

