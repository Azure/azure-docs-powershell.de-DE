---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: cf15d39a8c1ec320b45e488ccaac7903c82e30f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848812"
---
# <span data-ttu-id="127f1-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="127f1-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="127f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="127f1-102">SYNOPSIS</span></span>
<span data-ttu-id="127f1-103">Ruft eine Azure Express Route-Schaltkreis aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="127f1-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="127f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="127f1-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="127f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="127f1-105">DESCRIPTION</span></span>
<span data-ttu-id="127f1-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuit** " wird verwendet, um ein Express Route-Schaltkreis Objekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="127f1-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="127f1-107">Das zurückgegebene Circuit-Objekt kann als Eingabe für andere Cmdlets verwendet werden, die auf Express Route-Schaltkreisen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="127f1-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="127f1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="127f1-108">EXAMPLES</span></span>

### <span data-ttu-id="127f1-109">Beispiel 1: Abrufen des zu löschenden Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="127f1-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="127f1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="127f1-110">PARAMETERS</span></span>

### <span data-ttu-id="127f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127f1-111">-DefaultProfile</span></span>
<span data-ttu-id="127f1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="127f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="127f1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="127f1-113">-Name</span></span>
<span data-ttu-id="127f1-114">Der Name des Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="127f1-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="127f1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="127f1-115">-ResourceGroupName</span></span>
<span data-ttu-id="127f1-116">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="127f1-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="127f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127f1-117">CommonParameters</span></span>
<span data-ttu-id="127f1-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="127f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127f1-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="127f1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127f1-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="127f1-120">INPUTS</span></span>

## <span data-ttu-id="127f1-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="127f1-121">OUTPUTS</span></span>

### <span data-ttu-id="127f1-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="127f1-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="127f1-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="127f1-123">NOTES</span></span>

## <span data-ttu-id="127f1-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="127f1-124">RELATED LINKS</span></span>

[<span data-ttu-id="127f1-125">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="127f1-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="127f1-126">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="127f1-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="127f1-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="127f1-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="127f1-128">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="127f1-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
