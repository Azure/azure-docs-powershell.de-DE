---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzExpressRouteCircuitStat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 48136f033a75cfb49d05f5af76b1688ac6f68463
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841644"
---
# <span data-ttu-id="18349-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="18349-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="18349-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18349-102">SYNOPSIS</span></span>
<span data-ttu-id="18349-103">Ruft Nutzungsstatistiken eines Express Route-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="18349-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="18349-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18349-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18349-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18349-105">DESCRIPTION</span></span>
<span data-ttu-id="18349-106">Das Cmdlet " **Get-AzExpressRouteCircuitStat** " ruft Datenverkehrsstatistiken für einen Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="18349-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="18349-107">Die Statistik enthält die Anzahl der Bytes, die über die primären und sekundären Routen gesendet und empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="18349-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="18349-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18349-108">EXAMPLES</span></span>

### <span data-ttu-id="18349-109">Beispiel 1: Anzeigen der Datenverkehrsstatistiken für einen Express Route-Peer</span><span class="sxs-lookup"><span data-stu-id="18349-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="18349-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="18349-110">PARAMETERS</span></span>

### <span data-ttu-id="18349-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18349-111">-DefaultProfile</span></span>
<span data-ttu-id="18349-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18349-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18349-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="18349-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="18349-114">Der Name des Express Route-Schaltkreises, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="18349-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="18349-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="18349-115">-PeeringType</span></span>
<span data-ttu-id="18349-116">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="18349-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="18349-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18349-117">-ResourceGroupName</span></span>
<span data-ttu-id="18349-118">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="18349-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="18349-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18349-119">CommonParameters</span></span>
<span data-ttu-id="18349-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18349-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18349-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18349-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18349-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18349-122">INPUTS</span></span>

## <span data-ttu-id="18349-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18349-123">OUTPUTS</span></span>

### <span data-ttu-id="18349-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="18349-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="18349-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="18349-125">NOTES</span></span>

## <span data-ttu-id="18349-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18349-126">RELATED LINKS</span></span>

[<span data-ttu-id="18349-127">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="18349-127">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="18349-128">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="18349-128">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="18349-129">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="18349-129">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
