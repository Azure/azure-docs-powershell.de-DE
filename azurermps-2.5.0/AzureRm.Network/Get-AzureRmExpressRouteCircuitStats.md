---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
ms.openlocfilehash: 68579ea2adecbf7ad6a97fd11f4f32da9adeb48f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850408"
---
# <span data-ttu-id="18566-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="18566-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="18566-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18566-102">SYNOPSIS</span></span>
<span data-ttu-id="18566-103">Ruft Nutzungsstatistiken eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="18566-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18566-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18566-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18566-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18566-105">DESCRIPTION</span></span>
<span data-ttu-id="18566-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitStats** " ruft Datenverkehrsstatistiken für einen Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="18566-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="18566-107">Die Statistik enthält die Anzahl der Bytes, die über die primären und sekundären Routen gesendet und empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="18566-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="18566-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18566-108">EXAMPLES</span></span>

### <span data-ttu-id="18566-109">Beispiel 1: Anzeigen der Datenverkehrsstatistiken für einen Express Route-Peer</span><span class="sxs-lookup"><span data-stu-id="18566-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="18566-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="18566-110">PARAMETERS</span></span>

### <span data-ttu-id="18566-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18566-111">-DefaultProfile</span></span>
<span data-ttu-id="18566-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18566-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18566-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="18566-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="18566-114">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="18566-114">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18566-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="18566-115">-PeeringType</span></span>
<span data-ttu-id="18566-116">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="18566-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18566-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18566-117">-ResourceGroupName</span></span>
<span data-ttu-id="18566-118">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="18566-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18566-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18566-119">CommonParameters</span></span>
<span data-ttu-id="18566-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18566-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18566-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18566-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18566-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18566-122">INPUTS</span></span>

## <span data-ttu-id="18566-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18566-123">OUTPUTS</span></span>

### <span data-ttu-id="18566-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="18566-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="18566-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="18566-125">NOTES</span></span>

## <span data-ttu-id="18566-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18566-126">RELATED LINKS</span></span>

[<span data-ttu-id="18566-127">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="18566-127">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="18566-128">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="18566-128">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="18566-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="18566-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
