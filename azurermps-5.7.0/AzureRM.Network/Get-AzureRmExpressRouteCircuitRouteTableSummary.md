---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 849fb653308537a3d37740a21ba8b488903406ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497565"
---
# <span data-ttu-id="3852f-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3852f-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="3852f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3852f-102">SYNOPSIS</span></span>
<span data-ttu-id="3852f-103">Ruft eine Zusammenfassung der Arbeitsplan Tabelle eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="3852f-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3852f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3852f-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3852f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3852f-105">DESCRIPTION</span></span>
<span data-ttu-id="3852f-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitRouteTableSummary** " Ruft eine Zusammenfassung der BGP-Nachbar Informationen für einen bestimmten Routingkontext ab.</span><span class="sxs-lookup"><span data-stu-id="3852f-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="3852f-107">Diese Informationen sind hilfreich, um zu ermitteln, wie lange ein Routingkontext hergestellt wurde und wie viele Routen Präfixe vom Peering-Router angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="3852f-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="3852f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3852f-108">EXAMPLES</span></span>

### <span data-ttu-id="3852f-109">Beispiel 1: Anzeigen der Routenzusammenfassung für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="3852f-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="3852f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3852f-110">PARAMETERS</span></span>

### <span data-ttu-id="3852f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3852f-111">-DefaultProfile</span></span>
<span data-ttu-id="3852f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3852f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3852f-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="3852f-113">-DevicePath</span></span>
<span data-ttu-id="3852f-114">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="3852f-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3852f-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="3852f-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="3852f-116">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="3852f-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="3852f-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="3852f-117">-PeeringType</span></span>
<span data-ttu-id="3852f-118">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="3852f-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="3852f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3852f-119">-ResourceGroupName</span></span>
<span data-ttu-id="3852f-120">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="3852f-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="3852f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3852f-121">CommonParameters</span></span>
<span data-ttu-id="3852f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3852f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3852f-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3852f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3852f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3852f-124">INPUTS</span></span>

### <span data-ttu-id="3852f-125">Keine</span><span class="sxs-lookup"><span data-stu-id="3852f-125">None</span></span>
<span data-ttu-id="3852f-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3852f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3852f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3852f-127">OUTPUTS</span></span>

### <span data-ttu-id="3852f-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="3852f-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="3852f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3852f-129">NOTES</span></span>

## <span data-ttu-id="3852f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3852f-130">RELATED LINKS</span></span>

[<span data-ttu-id="3852f-131">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3852f-131">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="3852f-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3852f-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="3852f-133">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="3852f-133">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
