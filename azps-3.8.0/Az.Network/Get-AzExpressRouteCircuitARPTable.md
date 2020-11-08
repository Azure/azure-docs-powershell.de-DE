---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 12c920d0bacc6bd214e6ebe8d374a80d2b50a072
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996083"
---
# <span data-ttu-id="9a944-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="9a944-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="9a944-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a944-102">SYNOPSIS</span></span>
<span data-ttu-id="9a944-103">Ruft die ARP-Tabelle aus einem Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="9a944-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="9a944-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a944-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a944-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a944-105">DESCRIPTION</span></span>
<span data-ttu-id="9a944-106">Das Cmdlet " **Get-AzExpressRouteCircuitARPTable** " Ruft die ARP-Tabelle von beiden Schnittstellen eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="9a944-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="9a944-107">Die ARP-Tabelle enthält eine Zuordnung der IPv4-Adresse zu Mac-Adresse für einen bestimmten Peering.</span><span class="sxs-lookup"><span data-stu-id="9a944-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="9a944-108">Sie können die ARP-Tabelle verwenden, um die Konfiguration und Konnektivität von Layer 2 zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9a944-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="9a944-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a944-109">EXAMPLES</span></span>

### <span data-ttu-id="9a944-110">Beispiel 1: Anzeigen der ARP-Tabelle für einen Express Route-Peer</span><span class="sxs-lookup"><span data-stu-id="9a944-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="9a944-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a944-111">PARAMETERS</span></span>

### <span data-ttu-id="9a944-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a944-112">-DefaultProfile</span></span>
<span data-ttu-id="9a944-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a944-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a944-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="9a944-114">-DevicePath</span></span>
<span data-ttu-id="9a944-115">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="9a944-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="9a944-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="9a944-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="9a944-117">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="9a944-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="9a944-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="9a944-118">-PeeringType</span></span>
<span data-ttu-id="9a944-119">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="9a944-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="9a944-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a944-120">-ResourceGroupName</span></span>
<span data-ttu-id="9a944-121">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="9a944-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="9a944-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a944-122">CommonParameters</span></span>
<span data-ttu-id="9a944-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a944-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a944-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a944-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a944-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a944-125">INPUTS</span></span>

### <span data-ttu-id="9a944-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9a944-126">System.String</span></span>

## <span data-ttu-id="9a944-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a944-127">OUTPUTS</span></span>

### <span data-ttu-id="9a944-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="9a944-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="9a944-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a944-129">NOTES</span></span>

## <span data-ttu-id="9a944-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a944-130">RELATED LINKS</span></span>

[<span data-ttu-id="9a944-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="9a944-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="9a944-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9a944-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="9a944-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="9a944-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
