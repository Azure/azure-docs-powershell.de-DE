---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 14d1aea928923d9da4eee089ae1e95c75289eb3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664909"
---
# <span data-ttu-id="bb6d8-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb6d8-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="bb6d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6d8-103">Entfernt einen Integritäts Prüf Punkt aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb6d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb6d8-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb6d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb6d8-105">DESCRIPTION</span></span>
<span data-ttu-id="bb6d8-106">Das Remove-AzureRmApplicationGatewayProbeConfig-Cmdlet entfernt eine Heath-Sonde aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="bb6d8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb6d8-107">EXAMPLES</span></span>

### <span data-ttu-id="bb6d8-108">Beispiel 1: Entfernen einer Integritätsprüfung von einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="bb6d8-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="bb6d8-109">Mit diesem Befehl wird der Integritätstest mit dem Namen Probe04 aus dem Application Gateway mit dem Namen Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="bb6d8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb6d8-110">PARAMETERS</span></span>

### <span data-ttu-id="bb6d8-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb6d8-111">-ApplicationGateway</span></span>
<span data-ttu-id="bb6d8-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet einen Prüfpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="bb6d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6d8-113">-DefaultProfile</span></span>
<span data-ttu-id="bb6d8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb6d8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bb6d8-115">-Name</span></span>
<span data-ttu-id="bb6d8-116">Gibt den Namen des Prüfpunkts an, für den dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb6d8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6d8-117">CommonParameters</span></span>
<span data-ttu-id="bb6d8-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6d8-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb6d8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6d8-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb6d8-120">INPUTS</span></span>

### <span data-ttu-id="bb6d8-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb6d8-121">PSApplicationGateway</span></span>
<span data-ttu-id="bb6d8-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="bb6d8-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb6d8-123">OUTPUTS</span></span>

### <span data-ttu-id="bb6d8-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb6d8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bb6d8-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb6d8-125">NOTES</span></span>

## <span data-ttu-id="bb6d8-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb6d8-126">RELATED LINKS</span></span>

[<span data-ttu-id="bb6d8-127">Entfernen eines Prüfpunkts aus einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="bb6d8-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="bb6d8-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb6d8-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bb6d8-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb6d8-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bb6d8-130">Neu – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb6d8-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bb6d8-131">Satz-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb6d8-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

