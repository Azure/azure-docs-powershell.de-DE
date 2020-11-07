---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 5e0d9140e11ead75a1abbf43d520d44cffaf5463
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660787"
---
# <span data-ttu-id="52fc7-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="52fc7-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="52fc7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="52fc7-103">Ruft eine Zusammenfassung der Routentabelle einer Express Route-Querverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="52fc7-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="52fc7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52fc7-104">SYNTAX</span></span>

### <span data-ttu-id="52fc7-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="52fc7-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52fc7-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="52fc7-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52fc7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52fc7-107">DESCRIPTION</span></span>
<span data-ttu-id="52fc7-108">Das Cmdlet " **Get-AzExpressRouteCrossConnectionRouteTableSummary** " Ruft eine Zusammenfassung der BGP-Nachbar Informationen für einen bestimmten Routingkontext ab.</span><span class="sxs-lookup"><span data-stu-id="52fc7-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="52fc7-109">Diese Informationen sind hilfreich, um zu ermitteln, wie lange ein Routingkontext hergestellt wurde und wie viele Routen Präfixe vom Peering-Router angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="52fc7-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="52fc7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52fc7-110">EXAMPLES</span></span>

### <span data-ttu-id="52fc7-111">Beispiel 1: Anzeigen der Routenzusammenfassung für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="52fc7-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="52fc7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="52fc7-112">PARAMETERS</span></span>

### <span data-ttu-id="52fc7-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="52fc7-113">-CrossConnectionName</span></span>
<span data-ttu-id="52fc7-114">Der Name der Express-Route-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="52fc7-114">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52fc7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fc7-115">-DefaultProfile</span></span>
<span data-ttu-id="52fc7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52fc7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52fc7-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="52fc7-117">-DevicePath</span></span>
<span data-ttu-id="52fc7-118">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="52fc7-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="52fc7-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="52fc7-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="52fc7-120">Die Express-Route-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="52fc7-120">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52fc7-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="52fc7-121">-PeeringType</span></span>
<span data-ttu-id="52fc7-122">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="52fc7-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="52fc7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52fc7-123">-ResourceGroupName</span></span>
<span data-ttu-id="52fc7-124">Der Name der Ressourcengruppe, die die Express Route-Querverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="52fc7-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52fc7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fc7-125">CommonParameters</span></span>
<span data-ttu-id="52fc7-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fc7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fc7-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52fc7-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fc7-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52fc7-128">INPUTS</span></span>

### <span data-ttu-id="52fc7-129">Keine</span><span class="sxs-lookup"><span data-stu-id="52fc7-129">None</span></span>
<span data-ttu-id="52fc7-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="52fc7-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52fc7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52fc7-131">OUTPUTS</span></span>

### <span data-ttu-id="52fc7-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="52fc7-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="52fc7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="52fc7-133">NOTES</span></span>

## <span data-ttu-id="52fc7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52fc7-134">RELATED LINKS</span></span>

[<span data-ttu-id="52fc7-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="52fc7-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="52fc7-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="52fc7-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
