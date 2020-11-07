---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 43bf5a0a551840d03ac19e9ea78b26135dde5493
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841675"
---
# <span data-ttu-id="be350-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="be350-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="be350-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be350-102">SYNOPSIS</span></span>
<span data-ttu-id="be350-103">Ruft die ARP-Tabelle aus einem Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="be350-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="be350-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be350-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be350-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be350-105">DESCRIPTION</span></span>
<span data-ttu-id="be350-106">Das Cmdlet " **Get-AzExpressRouteCircuitARPTable** " Ruft die ARP-Tabelle von beiden Schnittstellen eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="be350-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="be350-107">Die ARP-Tabelle enthält eine Zuordnung der IPv4-Adresse zu Mac-Adresse für einen bestimmten Peering.</span><span class="sxs-lookup"><span data-stu-id="be350-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="be350-108">Sie können die ARP-Tabelle verwenden, um die Konfiguration und Konnektivität von Layer 2 zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="be350-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="be350-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be350-109">EXAMPLES</span></span>

### <span data-ttu-id="be350-110">Beispiel 1: Anzeigen der ARP-Tabelle für einen Express Route-Peer</span><span class="sxs-lookup"><span data-stu-id="be350-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="be350-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="be350-111">PARAMETERS</span></span>

### <span data-ttu-id="be350-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be350-112">-DefaultProfile</span></span>
<span data-ttu-id="be350-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be350-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be350-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="be350-114">-DevicePath</span></span>
<span data-ttu-id="be350-115">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="be350-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="be350-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="be350-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="be350-117">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="be350-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="be350-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="be350-118">-PeeringType</span></span>
<span data-ttu-id="be350-119">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="be350-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="be350-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be350-120">-ResourceGroupName</span></span>
<span data-ttu-id="be350-121">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="be350-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="be350-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be350-122">CommonParameters</span></span>
<span data-ttu-id="be350-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be350-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be350-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be350-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be350-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be350-125">INPUTS</span></span>

## <span data-ttu-id="be350-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be350-126">OUTPUTS</span></span>

### <span data-ttu-id="be350-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="be350-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="be350-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="be350-128">NOTES</span></span>

## <span data-ttu-id="be350-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be350-129">RELATED LINKS</span></span>

[<span data-ttu-id="be350-130">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="be350-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="be350-131">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="be350-131">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="be350-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="be350-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
