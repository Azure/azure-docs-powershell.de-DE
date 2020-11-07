---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: bb6ffb1537a5beb6a845bbad742b864360da55d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822383"
---
# <span data-ttu-id="f30cb-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f30cb-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="f30cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f30cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f30cb-103">Ruft eine Routentabelle aus einem Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="f30cb-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f30cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f30cb-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f30cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f30cb-105">DESCRIPTION</span></span>
<span data-ttu-id="f30cb-106">Das Cmdlet " **Get-AzExpressRouteCircuitRouteTable** " Ruft eine detaillierte Route-Tabelle eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="f30cb-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="f30cb-107">Die Route-Tabelle zeigt alle Routen an oder kann gefiltert werden, um Routen für einen bestimmten Peering-Typ anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f30cb-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="f30cb-108">Sie können die Tabelle Route verwenden, um Ihre Peering-Konfiguration und-Konnektivität zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f30cb-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="f30cb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f30cb-109">EXAMPLES</span></span>

### <span data-ttu-id="f30cb-110">Beispiel 1: Anzeigen der Route-Tabelle für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="f30cb-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="f30cb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f30cb-111">PARAMETERS</span></span>

### <span data-ttu-id="f30cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30cb-112">-DefaultProfile</span></span>
<span data-ttu-id="f30cb-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f30cb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f30cb-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f30cb-114">-DevicePath</span></span>
<span data-ttu-id="f30cb-115">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="f30cb-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="f30cb-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="f30cb-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="f30cb-117">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="f30cb-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="f30cb-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f30cb-118">-PeeringType</span></span>
<span data-ttu-id="f30cb-119">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f30cb-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f30cb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30cb-120">-ResourceGroupName</span></span>
<span data-ttu-id="f30cb-121">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="f30cb-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="f30cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30cb-122">CommonParameters</span></span>
<span data-ttu-id="f30cb-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f30cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30cb-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f30cb-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30cb-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f30cb-125">INPUTS</span></span>

### <span data-ttu-id="f30cb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f30cb-126">System.String</span></span>

## <span data-ttu-id="f30cb-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f30cb-127">OUTPUTS</span></span>

### <span data-ttu-id="f30cb-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="f30cb-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="f30cb-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f30cb-129">NOTES</span></span>

## <span data-ttu-id="f30cb-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f30cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="f30cb-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f30cb-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f30cb-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f30cb-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="f30cb-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="f30cb-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
