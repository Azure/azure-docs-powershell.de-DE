---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003576"
---
# <span data-ttu-id="6a421-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6a421-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="6a421-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a421-102">SYNOPSIS</span></span>
<span data-ttu-id="6a421-103">Ruft eine Routingtabelle aus einer Express Route-Querverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="6a421-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="6a421-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a421-104">SYNTAX</span></span>

### <span data-ttu-id="6a421-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="6a421-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a421-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="6a421-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a421-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a421-107">DESCRIPTION</span></span>
<span data-ttu-id="6a421-108">Das Cmdlet " **Get-AzExpressRouteCrossConnectionRouteTable** " Ruft eine detaillierte Route-Tabelle eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="6a421-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="6a421-109">Die Route-Tabelle zeigt alle Routen an oder kann gefiltert werden, um Routen für einen bestimmten Peering-Typ anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6a421-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="6a421-110">Sie können die Tabelle Route verwenden, um Ihre Peering-Konfiguration und-Konnektivität zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6a421-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="6a421-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a421-111">EXAMPLES</span></span>

### <span data-ttu-id="6a421-112">Beispiel 1: Anzeigen der Route-Tabelle für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="6a421-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="6a421-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a421-113">PARAMETERS</span></span>

### <span data-ttu-id="6a421-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="6a421-114">-CrossConnectionName</span></span>
<span data-ttu-id="6a421-115">Der Name der Express-Route-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="6a421-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="6a421-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a421-116">-DefaultProfile</span></span>
<span data-ttu-id="6a421-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a421-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a421-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="6a421-118">-DevicePath</span></span>
<span data-ttu-id="6a421-119">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="6a421-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="6a421-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6a421-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="6a421-121">Die Express-Route-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="6a421-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="6a421-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="6a421-122">-PeeringType</span></span>
<span data-ttu-id="6a421-123">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="6a421-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="6a421-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a421-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a421-125">Der Name der Ressourcengruppe, die die Express Route-Querverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="6a421-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="6a421-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a421-126">CommonParameters</span></span>
<span data-ttu-id="6a421-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a421-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a421-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a421-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a421-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a421-129">INPUTS</span></span>

### <span data-ttu-id="6a421-130">Keine</span><span class="sxs-lookup"><span data-stu-id="6a421-130">None</span></span>
<span data-ttu-id="6a421-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6a421-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a421-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a421-132">OUTPUTS</span></span>

### <span data-ttu-id="6a421-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="6a421-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="6a421-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a421-134">NOTES</span></span>

## <span data-ttu-id="6a421-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a421-135">RELATED LINKS</span></span>

[<span data-ttu-id="6a421-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="6a421-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="6a421-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6a421-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
