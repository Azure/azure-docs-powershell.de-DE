---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165806"
---
# <span data-ttu-id="baab9-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="baab9-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="baab9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="baab9-102">SYNOPSIS</span></span>
<span data-ttu-id="baab9-103">Ruft eine Zusammenfassung der Arbeitsplan Tabelle eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="baab9-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="baab9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="baab9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="baab9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="baab9-105">DESCRIPTION</span></span>
<span data-ttu-id="baab9-106">Das Cmdlet " **Get-AzExpressRouteCircuitRouteTableSummary** " Ruft eine Zusammenfassung der BGP-Nachbar Informationen für einen bestimmten Routingkontext ab.</span><span class="sxs-lookup"><span data-stu-id="baab9-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="baab9-107">Diese Informationen sind hilfreich, um zu ermitteln, wie lange ein Routingkontext hergestellt wurde und wie viele Routen Präfixe vom Peering-Router angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="baab9-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="baab9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="baab9-108">EXAMPLES</span></span>

### <span data-ttu-id="baab9-109">Beispiel 1: Anzeigen der Routenzusammenfassung für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="baab9-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="baab9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="baab9-110">PARAMETERS</span></span>

### <span data-ttu-id="baab9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baab9-111">-DefaultProfile</span></span>
<span data-ttu-id="baab9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="baab9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baab9-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="baab9-113">-DevicePath</span></span>
<span data-ttu-id="baab9-114">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="baab9-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baab9-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="baab9-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="baab9-116">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="baab9-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="baab9-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="baab9-117">-PeeringType</span></span>
<span data-ttu-id="baab9-118">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="baab9-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baab9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baab9-119">-ResourceGroupName</span></span>
<span data-ttu-id="baab9-120">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="baab9-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="baab9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baab9-121">CommonParameters</span></span>
<span data-ttu-id="baab9-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baab9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baab9-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baab9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baab9-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="baab9-124">INPUTS</span></span>

### <span data-ttu-id="baab9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="baab9-125">System.String</span></span>

## <span data-ttu-id="baab9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="baab9-126">OUTPUTS</span></span>

### <span data-ttu-id="baab9-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="baab9-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="baab9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="baab9-128">NOTES</span></span>

## <span data-ttu-id="baab9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="baab9-129">RELATED LINKS</span></span>

[<span data-ttu-id="baab9-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="baab9-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="baab9-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="baab9-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="baab9-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="baab9-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
