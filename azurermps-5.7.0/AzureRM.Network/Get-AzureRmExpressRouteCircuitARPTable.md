---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: e007f220b827db144a4c10b1adb5732e110ddf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497569"
---
# <span data-ttu-id="add29-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="add29-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="add29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="add29-102">SYNOPSIS</span></span>
<span data-ttu-id="add29-103">Ruft die ARP-Tabelle aus einem Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="add29-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="add29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="add29-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="add29-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="add29-105">DESCRIPTION</span></span>
<span data-ttu-id="add29-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitARPTable** " Ruft die ARP-Tabelle von beiden Schnittstellen eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="add29-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="add29-107">Die ARP-Tabelle enthält eine Zuordnung der IPv4-Adresse zu Mac-Adresse für einen bestimmten Peering.</span><span class="sxs-lookup"><span data-stu-id="add29-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="add29-108">Sie können die ARP-Tabelle verwenden, um die Konfiguration und Konnektivität von Layer 2 zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="add29-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="add29-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="add29-109">EXAMPLES</span></span>

### <span data-ttu-id="add29-110">Beispiel 1: Anzeigen der ARP-Tabelle für einen Express Route-Peer</span><span class="sxs-lookup"><span data-stu-id="add29-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="add29-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="add29-111">PARAMETERS</span></span>

### <span data-ttu-id="add29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add29-112">-DefaultProfile</span></span>
<span data-ttu-id="add29-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="add29-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="add29-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="add29-114">-DevicePath</span></span>
<span data-ttu-id="add29-115">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="add29-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="add29-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="add29-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="add29-117">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="add29-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="add29-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="add29-118">-PeeringType</span></span>
<span data-ttu-id="add29-119">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="add29-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="add29-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add29-120">-ResourceGroupName</span></span>
<span data-ttu-id="add29-121">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="add29-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="add29-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add29-122">CommonParameters</span></span>
<span data-ttu-id="add29-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add29-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add29-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add29-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add29-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="add29-125">INPUTS</span></span>

### <span data-ttu-id="add29-126">Keine</span><span class="sxs-lookup"><span data-stu-id="add29-126">None</span></span>
<span data-ttu-id="add29-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="add29-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="add29-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="add29-128">OUTPUTS</span></span>

### <span data-ttu-id="add29-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="add29-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="add29-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="add29-130">NOTES</span></span>

## <span data-ttu-id="add29-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="add29-131">RELATED LINKS</span></span>

[<span data-ttu-id="add29-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="add29-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="add29-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="add29-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="add29-134">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="add29-134">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
