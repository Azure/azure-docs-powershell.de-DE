---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: b223cf62b536479b4c39d5852974698f2f38becf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664466"
---
# <span data-ttu-id="efb45-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efb45-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="efb45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="efb45-102">SYNOPSIS</span></span>
<span data-ttu-id="efb45-103">Ändert einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="efb45-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efb45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="efb45-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efb45-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="efb45-105">DESCRIPTION</span></span>
<span data-ttu-id="efb45-106">Das Cmdlet " **Satz-AzureRmExpressRouteCircuit** " speichert den geänderten Express Route-Schaltkreis in Azure.</span><span class="sxs-lookup"><span data-stu-id="efb45-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="efb45-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="efb45-107">EXAMPLES</span></span>

### <span data-ttu-id="efb45-108">Beispiel 1: Ändern des serviceKey verwenden eines Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="efb45-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="efb45-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="efb45-109">PARAMETERS</span></span>

### <span data-ttu-id="efb45-110">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efb45-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="efb45-111">Gibt das **ExpressRouteCircuit** -Objekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="efb45-111">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efb45-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb45-112">-DefaultProfile</span></span>
<span data-ttu-id="efb45-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="efb45-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb45-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb45-114">CommonParameters</span></span>
<span data-ttu-id="efb45-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb45-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb45-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efb45-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb45-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="efb45-117">INPUTS</span></span>

### <span data-ttu-id="efb45-118">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efb45-118">PSExpressRouteCircuit</span></span>
<span data-ttu-id="efb45-119">Der Parameter "ExpressRouteCircuit" akzeptiert den Wert vom Typ "PSExpressRouteCircuit" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="efb45-119">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="efb45-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="efb45-120">OUTPUTS</span></span>

### <span data-ttu-id="efb45-121">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efb45-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="efb45-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="efb45-122">NOTES</span></span>

## <span data-ttu-id="efb45-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="efb45-123">RELATED LINKS</span></span>

[<span data-ttu-id="efb45-124">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efb45-124">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="efb45-125">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efb45-125">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="efb45-126">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efb45-126">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="efb45-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efb45-127">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
