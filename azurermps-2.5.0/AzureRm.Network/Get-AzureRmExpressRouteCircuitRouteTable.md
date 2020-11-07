---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
ms.openlocfilehash: 883d2ae51046f3dc1ee6c8350d996fedbfff083e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849615"
---
# <span data-ttu-id="eb730-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb730-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="eb730-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb730-102">SYNOPSIS</span></span>
<span data-ttu-id="eb730-103">Ruft eine Routentabelle aus einem Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="eb730-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb730-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb730-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb730-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb730-105">DESCRIPTION</span></span>
<span data-ttu-id="eb730-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitRouteTable** " Ruft eine detaillierte Route-Tabelle eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="eb730-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="eb730-107">Die Route-Tabelle zeigt alle Routen an oder kann gefiltert werden, um Routen für einen bestimmten Peering-Typ anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="eb730-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="eb730-108">Sie können die Tabelle Route verwenden, um Ihre Peering-Konfiguration und-Konnektivität zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="eb730-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="eb730-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb730-109">EXAMPLES</span></span>

### <span data-ttu-id="eb730-110">Beispiel 1: Anzeigen der Route-Tabelle für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="eb730-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="eb730-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb730-111">PARAMETERS</span></span>

### <span data-ttu-id="eb730-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb730-112">-DefaultProfile</span></span>
<span data-ttu-id="eb730-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb730-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb730-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="eb730-114">-DevicePath</span></span>
<span data-ttu-id="eb730-115">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="eb730-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="eb730-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="eb730-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="eb730-117">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="eb730-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="eb730-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="eb730-118">-PeeringType</span></span>
<span data-ttu-id="eb730-119">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="eb730-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="eb730-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb730-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb730-121">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="eb730-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="eb730-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb730-122">CommonParameters</span></span>
<span data-ttu-id="eb730-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb730-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb730-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb730-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb730-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb730-125">INPUTS</span></span>

## <span data-ttu-id="eb730-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb730-126">OUTPUTS</span></span>

### <span data-ttu-id="eb730-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="eb730-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="eb730-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb730-128">NOTES</span></span>

## <span data-ttu-id="eb730-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb730-129">RELATED LINKS</span></span>

[<span data-ttu-id="eb730-130">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="eb730-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="eb730-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eb730-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="eb730-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="eb730-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
