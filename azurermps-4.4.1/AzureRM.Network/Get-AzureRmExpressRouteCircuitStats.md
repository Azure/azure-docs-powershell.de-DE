---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: 3230a9e9d8bb70cc80125258cca7d2eaef973e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500806"
---
# <span data-ttu-id="2531d-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="2531d-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="2531d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2531d-102">SYNOPSIS</span></span>
<span data-ttu-id="2531d-103">Ruft Nutzungsstatistiken eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="2531d-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2531d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2531d-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2531d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2531d-105">DESCRIPTION</span></span>
<span data-ttu-id="2531d-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitStats** " ruft Datenverkehrsstatistiken für einen Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="2531d-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="2531d-107">Die Statistik enthält die Anzahl der Bytes, die über die primären und sekundären Routen gesendet und empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="2531d-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="2531d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2531d-108">EXAMPLES</span></span>

### <span data-ttu-id="2531d-109">Beispiel 1: Anzeigen der Datenverkehrsstatistiken für einen Express Route-Peer</span><span class="sxs-lookup"><span data-stu-id="2531d-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="2531d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2531d-110">PARAMETERS</span></span>

### <span data-ttu-id="2531d-111">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="2531d-111">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="2531d-112">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="2531d-112">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2531d-113">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2531d-113">-PeeringType</span></span>
<span data-ttu-id="2531d-114">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2531d-114">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2531d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2531d-115">-ResourceGroupName</span></span>
<span data-ttu-id="2531d-116">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="2531d-116">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2531d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2531d-117">-DefaultProfile</span></span>
<span data-ttu-id="2531d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2531d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2531d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2531d-119">CommonParameters</span></span>
<span data-ttu-id="2531d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2531d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2531d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2531d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2531d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2531d-122">INPUTS</span></span>

## <span data-ttu-id="2531d-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2531d-123">OUTPUTS</span></span>

### <span data-ttu-id="2531d-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="2531d-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="2531d-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="2531d-125">NOTES</span></span>

## <span data-ttu-id="2531d-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2531d-126">RELATED LINKS</span></span>

[<span data-ttu-id="2531d-127">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2531d-127">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="2531d-128">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2531d-128">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="2531d-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2531d-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
