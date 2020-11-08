---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176436"
---
# <span data-ttu-id="dfe40-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dfe40-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="dfe40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dfe40-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe40-103">Ruft eine Zusammenfassung der Arbeitsplan Tabelle eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="dfe40-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="dfe40-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfe40-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfe40-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfe40-105">DESCRIPTION</span></span>
<span data-ttu-id="dfe40-106">Das Cmdlet " **Get-AzExpressRouteCircuitRouteTableSummary** " Ruft eine Zusammenfassung der BGP-Nachbar Informationen für einen bestimmten Routingkontext ab.</span><span class="sxs-lookup"><span data-stu-id="dfe40-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="dfe40-107">Diese Informationen sind hilfreich, um zu ermitteln, wie lange ein Routingkontext hergestellt wurde und wie viele Routen Präfixe vom Peering-Router angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="dfe40-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="dfe40-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfe40-108">EXAMPLES</span></span>

### <span data-ttu-id="dfe40-109">Beispiel 1: Anzeigen der Routenzusammenfassung für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="dfe40-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="dfe40-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfe40-110">PARAMETERS</span></span>

### <span data-ttu-id="dfe40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe40-111">-DefaultProfile</span></span>
<span data-ttu-id="dfe40-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dfe40-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe40-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="dfe40-113">-DevicePath</span></span>
<span data-ttu-id="dfe40-114">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="dfe40-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="dfe40-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="dfe40-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="dfe40-116">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="dfe40-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="dfe40-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="dfe40-117">-PeeringType</span></span>
<span data-ttu-id="dfe40-118">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="dfe40-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="dfe40-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe40-119">-ResourceGroupName</span></span>
<span data-ttu-id="dfe40-120">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="dfe40-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="dfe40-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe40-121">CommonParameters</span></span>
<span data-ttu-id="dfe40-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe40-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe40-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfe40-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe40-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dfe40-124">INPUTS</span></span>

### <span data-ttu-id="dfe40-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe40-125">System.String</span></span>

## <span data-ttu-id="dfe40-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dfe40-126">OUTPUTS</span></span>

### <span data-ttu-id="dfe40-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="dfe40-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="dfe40-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="dfe40-128">NOTES</span></span>

## <span data-ttu-id="dfe40-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dfe40-129">RELATED LINKS</span></span>

[<span data-ttu-id="dfe40-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="dfe40-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="dfe40-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="dfe40-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="dfe40-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="dfe40-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
