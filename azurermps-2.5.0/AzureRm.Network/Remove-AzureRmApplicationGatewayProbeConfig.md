---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 39ce61f4a1e973dfdac8104a6364bdd3d8b9151a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850356"
---
# <span data-ttu-id="fdf00-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fdf00-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="fdf00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdf00-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf00-103">Entfernt einen Integritäts Prüf Punkt aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fdf00-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdf00-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdf00-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf00-106">Das Remove-AzureRmApplicationGatewayProbeConfig-Cmdlet entfernt eine Heath-Sonde aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fdf00-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="fdf00-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdf00-107">EXAMPLES</span></span>

### <span data-ttu-id="fdf00-108">Beispiel 1: Entfernen einer Integritätsprüfung von einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="fdf00-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="fdf00-109">Mit diesem Befehl wird der Integritätstest mit dem Namen Probe04 aus dem Application Gateway mit dem Namen Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="fdf00-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="fdf00-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdf00-110">PARAMETERS</span></span>

### <span data-ttu-id="fdf00-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fdf00-111">-ApplicationGateway</span></span>
<span data-ttu-id="fdf00-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet einen Prüfpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="fdf00-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf00-113">-DefaultProfile</span></span>
<span data-ttu-id="fdf00-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fdf00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf00-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fdf00-115">-Name</span></span>
<span data-ttu-id="fdf00-116">Gibt den Namen des Prüfpunkts an, für den dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="fdf00-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf00-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf00-117">CommonParameters</span></span>
<span data-ttu-id="fdf00-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf00-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf00-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf00-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf00-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdf00-120">INPUTS</span></span>

### <span data-ttu-id="fdf00-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fdf00-121">PSApplicationGateway</span></span>
<span data-ttu-id="fdf00-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fdf00-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="fdf00-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdf00-123">OUTPUTS</span></span>

### <span data-ttu-id="fdf00-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fdf00-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fdf00-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdf00-125">NOTES</span></span>

## <span data-ttu-id="fdf00-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdf00-126">RELATED LINKS</span></span>

[<span data-ttu-id="fdf00-127">Entfernen eines Prüfpunkts aus einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="fdf00-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="fdf00-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fdf00-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fdf00-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fdf00-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fdf00-130">Neu – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fdf00-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fdf00-131">Satz-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fdf00-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

