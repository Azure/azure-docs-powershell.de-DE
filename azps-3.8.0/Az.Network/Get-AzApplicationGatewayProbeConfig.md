---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846212"
---
# <span data-ttu-id="1e750-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e750-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="1e750-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e750-102">SYNOPSIS</span></span>
<span data-ttu-id="1e750-103">Ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="1e750-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1e750-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e750-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e750-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e750-105">DESCRIPTION</span></span>
<span data-ttu-id="1e750-106">Das Get-AzApplicationGatewayProbeConfig-Cmdlet ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="1e750-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1e750-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e750-107">EXAMPLES</span></span>

### <span data-ttu-id="1e750-108">Beispiel 1: Abrufen einer vorhandenen Sonde von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="1e750-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="1e750-109">Dieser Befehl ruft den Integritätstest mit dem Namen "Probe02" aus dem Application Gateway mit dem Namen Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="1e750-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="1e750-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e750-110">PARAMETERS</span></span>

### <span data-ttu-id="1e750-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e750-111">-ApplicationGateway</span></span>
<span data-ttu-id="1e750-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine Prüf Punkt Konfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="1e750-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="1e750-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e750-113">-DefaultProfile</span></span>
<span data-ttu-id="1e750-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e750-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e750-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1e750-115">-Name</span></span>
<span data-ttu-id="1e750-116">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="1e750-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="1e750-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e750-117">CommonParameters</span></span>
<span data-ttu-id="1e750-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e750-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e750-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e750-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e750-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e750-120">INPUTS</span></span>

### <span data-ttu-id="1e750-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e750-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e750-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e750-122">OUTPUTS</span></span>

### <span data-ttu-id="1e750-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="1e750-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="1e750-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e750-124">NOTES</span></span>

## <span data-ttu-id="1e750-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e750-125">RELATED LINKS</span></span>

[<span data-ttu-id="1e750-126">Hinzufügen einer Sonde zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="1e750-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="1e750-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e750-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1e750-128">Neu – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e750-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1e750-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e750-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1e750-130">Satz-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e750-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

