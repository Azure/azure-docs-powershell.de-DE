---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: 4577eb4f105bca235e7b5e9feb0b0ef308298881
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662465"
---
# <span data-ttu-id="268f8-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="268f8-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="268f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="268f8-102">SYNOPSIS</span></span>
<span data-ttu-id="268f8-103">Ruft Nutzungsstatistiken eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="268f8-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="268f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="268f8-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="268f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="268f8-105">DESCRIPTION</span></span>
<span data-ttu-id="268f8-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitStats** " ruft Datenverkehrsstatistiken für einen Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="268f8-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="268f8-107">Die Statistik enthält die Anzahl der Bytes, die über die primären und sekundären Routen gesendet und empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="268f8-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="268f8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="268f8-108">EXAMPLES</span></span>

### <span data-ttu-id="268f8-109">Beispiel 1: Anzeigen der Datenverkehrsstatistiken für einen Express Route-Peer</span><span class="sxs-lookup"><span data-stu-id="268f8-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="268f8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="268f8-110">PARAMETERS</span></span>

### <span data-ttu-id="268f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268f8-111">-DefaultProfile</span></span>
<span data-ttu-id="268f8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="268f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="268f8-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="268f8-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="268f8-114">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="268f8-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="268f8-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="268f8-115">-PeeringType</span></span>
<span data-ttu-id="268f8-116">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="268f8-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="268f8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="268f8-117">-ResourceGroupName</span></span>
<span data-ttu-id="268f8-118">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="268f8-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="268f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268f8-119">CommonParameters</span></span>
<span data-ttu-id="268f8-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268f8-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268f8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268f8-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="268f8-122">INPUTS</span></span>

### <span data-ttu-id="268f8-123">Keine</span><span class="sxs-lookup"><span data-stu-id="268f8-123">None</span></span>
<span data-ttu-id="268f8-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="268f8-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="268f8-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="268f8-125">OUTPUTS</span></span>

### <span data-ttu-id="268f8-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="268f8-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="268f8-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="268f8-127">NOTES</span></span>

## <span data-ttu-id="268f8-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="268f8-128">RELATED LINKS</span></span>

[<span data-ttu-id="268f8-129">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="268f8-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="268f8-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="268f8-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="268f8-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="268f8-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
