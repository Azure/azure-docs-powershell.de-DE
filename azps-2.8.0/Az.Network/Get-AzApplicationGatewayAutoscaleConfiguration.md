---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 7eb80c50674eeea374dcffbe2d6838d46bf2643e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822464"
---
# <span data-ttu-id="60e45-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="60e45-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="60e45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60e45-102">SYNOPSIS</span></span>
<span data-ttu-id="60e45-103">Ruft die AutoScale-Konfiguration des Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="60e45-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="60e45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60e45-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60e45-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60e45-105">DESCRIPTION</span></span>
<span data-ttu-id="60e45-106">Das Cmdlet " **Get-AzApplicationGatewayAutoscaleConfiguration** " Ruft die Konfiguration des Anwendungs Gateways mit einer AutoScale-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="60e45-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="60e45-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60e45-107">EXAMPLES</span></span>

### <span data-ttu-id="60e45-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60e45-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="60e45-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $GW Variablen.</span><span class="sxs-lookup"><span data-stu-id="60e45-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="60e45-110">Der zweite Befehl extrahiert die AutoScale-Konfiguration aus dem Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="60e45-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="60e45-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="60e45-111">PARAMETERS</span></span>

### <span data-ttu-id="60e45-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60e45-112">-ApplicationGateway</span></span>
<span data-ttu-id="60e45-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="60e45-113">The applicationGateway</span></span>

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

### <span data-ttu-id="60e45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e45-114">-DefaultProfile</span></span>
<span data-ttu-id="60e45-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60e45-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e45-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e45-116">CommonParameters</span></span>
<span data-ttu-id="60e45-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e45-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e45-118">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60e45-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e45-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60e45-119">INPUTS</span></span>

### <span data-ttu-id="60e45-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60e45-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="60e45-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60e45-121">OUTPUTS</span></span>

### <span data-ttu-id="60e45-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="60e45-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="60e45-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="60e45-123">NOTES</span></span>

## <span data-ttu-id="60e45-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60e45-124">RELATED LINKS</span></span>

[<span data-ttu-id="60e45-125">Neu – AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="60e45-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="60e45-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="60e45-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="60e45-127">Satz-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="60e45-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
