---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 9d221f5ff25e43a750f939f80eae7a7878eacc44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496441"
---
# <span data-ttu-id="5e531-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e531-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="5e531-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e531-102">SYNOPSIS</span></span>
<span data-ttu-id="5e531-103">Ruft eine Routentabelle aus einem Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="5e531-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e531-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e531-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e531-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e531-105">DESCRIPTION</span></span>
<span data-ttu-id="5e531-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitRouteTable** " Ruft eine detaillierte Route-Tabelle eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="5e531-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="5e531-107">Die Route-Tabelle zeigt alle Routen an oder kann gefiltert werden, um Routen für einen bestimmten Peering-Typ anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e531-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="5e531-108">Sie können die Tabelle Route verwenden, um Ihre Peering-Konfiguration und-Konnektivität zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e531-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="5e531-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e531-109">EXAMPLES</span></span>

### <span data-ttu-id="5e531-110">Beispiel 1: Anzeigen der Route-Tabelle für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="5e531-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="5e531-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e531-111">PARAMETERS</span></span>

### <span data-ttu-id="5e531-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e531-112">-DefaultProfile</span></span>
<span data-ttu-id="5e531-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e531-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e531-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="5e531-114">-DevicePath</span></span>
<span data-ttu-id="5e531-115">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="5e531-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="5e531-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="5e531-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="5e531-117">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="5e531-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="5e531-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="5e531-118">-PeeringType</span></span>
<span data-ttu-id="5e531-119">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="5e531-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="5e531-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e531-120">-ResourceGroupName</span></span>
<span data-ttu-id="5e531-121">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="5e531-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="5e531-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e531-122">CommonParameters</span></span>
<span data-ttu-id="5e531-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e531-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e531-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e531-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e531-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e531-125">INPUTS</span></span>

### <span data-ttu-id="5e531-126">Keine</span><span class="sxs-lookup"><span data-stu-id="5e531-126">None</span></span>
<span data-ttu-id="5e531-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5e531-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e531-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e531-128">OUTPUTS</span></span>

### <span data-ttu-id="5e531-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="5e531-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="5e531-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e531-130">NOTES</span></span>

## <span data-ttu-id="5e531-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e531-131">RELATED LINKS</span></span>

[<span data-ttu-id="5e531-132">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5e531-132">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="5e531-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5e531-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="5e531-134">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="5e531-134">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
