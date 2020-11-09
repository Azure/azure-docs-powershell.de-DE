---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301492"
---
# <span data-ttu-id="87d67-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="87d67-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="87d67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87d67-102">SYNOPSIS</span></span>
<span data-ttu-id="87d67-103">Ruft die ARP-Tabelle aus einer Express Route-Querverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="87d67-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="87d67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87d67-104">SYNTAX</span></span>

### <span data-ttu-id="87d67-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="87d67-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87d67-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="87d67-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87d67-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87d67-107">DESCRIPTION</span></span>
<span data-ttu-id="87d67-108">Das Cmdlet " **Get-AzExpressRouteCrossConnectionARPTable** " Ruft die ARP-Tabelle von beiden Schnittstellen einer Express Route-Querverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="87d67-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="87d67-109">Die ARP-Tabelle enthält eine Zuordnung der IPv4-Adresse zu Mac-Adresse für einen bestimmten Peering.</span><span class="sxs-lookup"><span data-stu-id="87d67-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="87d67-110">Sie können die ARP-Tabelle verwenden, um die Konfiguration und Konnektivität von Layer 2 zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="87d67-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="87d67-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87d67-111">EXAMPLES</span></span>

### <span data-ttu-id="87d67-112">Beispiel 1: Anzeigen der ARP-Tabelle für einen Express Route-Peer</span><span class="sxs-lookup"><span data-stu-id="87d67-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="87d67-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="87d67-113">PARAMETERS</span></span>

### <span data-ttu-id="87d67-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="87d67-114">-CrossConnectionName</span></span>
<span data-ttu-id="87d67-115">Der Name der Express-Route-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="87d67-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="87d67-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d67-116">-DefaultProfile</span></span>
<span data-ttu-id="87d67-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87d67-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87d67-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="87d67-118">-DevicePath</span></span>
<span data-ttu-id="87d67-119">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="87d67-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="87d67-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="87d67-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="87d67-121">Die Express-Route-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="87d67-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="87d67-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="87d67-122">-PeeringType</span></span>
<span data-ttu-id="87d67-123">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="87d67-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="87d67-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d67-124">-ResourceGroupName</span></span>
<span data-ttu-id="87d67-125">Der Name der Ressourcengruppe, die die Express Route-Querverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="87d67-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="87d67-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d67-126">CommonParameters</span></span>
<span data-ttu-id="87d67-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d67-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d67-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87d67-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d67-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87d67-129">INPUTS</span></span>

### <span data-ttu-id="87d67-130">Keine</span><span class="sxs-lookup"><span data-stu-id="87d67-130">None</span></span>
<span data-ttu-id="87d67-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="87d67-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87d67-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87d67-132">OUTPUTS</span></span>

### <span data-ttu-id="87d67-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="87d67-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="87d67-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="87d67-134">NOTES</span></span>

## <span data-ttu-id="87d67-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87d67-135">RELATED LINKS</span></span>

[<span data-ttu-id="87d67-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="87d67-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="87d67-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="87d67-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
