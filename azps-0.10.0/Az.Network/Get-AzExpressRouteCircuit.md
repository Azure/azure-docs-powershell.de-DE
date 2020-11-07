---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841676"
---
# <span data-ttu-id="faf4c-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="faf4c-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="faf4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="faf4c-102">SYNOPSIS</span></span>
<span data-ttu-id="faf4c-103">Ruft eine Azure Express Route-Schaltkreis aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="faf4c-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="faf4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="faf4c-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faf4c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faf4c-105">DESCRIPTION</span></span>
<span data-ttu-id="faf4c-106">Das Cmdlet " **Get-AzExpressRouteCircuit** " wird verwendet, um ein Express Route-Schaltkreis Objekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="faf4c-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="faf4c-107">Das zurückgegebene Circuit-Objekt kann als Eingabe für andere Cmdlets verwendet werden, die auf Express Route-Schaltkreisen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="faf4c-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="faf4c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="faf4c-108">EXAMPLES</span></span>

### <span data-ttu-id="faf4c-109">Beispiel 1: Abrufen des zu löschenden Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="faf4c-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="faf4c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="faf4c-110">PARAMETERS</span></span>

### <span data-ttu-id="faf4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf4c-111">-DefaultProfile</span></span>
<span data-ttu-id="faf4c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="faf4c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faf4c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="faf4c-113">-Name</span></span>
<span data-ttu-id="faf4c-114">Der Name des Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="faf4c-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="faf4c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf4c-115">-ResourceGroupName</span></span>
<span data-ttu-id="faf4c-116">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="faf4c-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="faf4c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf4c-117">CommonParameters</span></span>
<span data-ttu-id="faf4c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf4c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf4c-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf4c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf4c-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="faf4c-120">INPUTS</span></span>

## <span data-ttu-id="faf4c-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="faf4c-121">OUTPUTS</span></span>

### <span data-ttu-id="faf4c-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="faf4c-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="faf4c-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="faf4c-123">NOTES</span></span>

## <span data-ttu-id="faf4c-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="faf4c-124">RELATED LINKS</span></span>

[<span data-ttu-id="faf4c-125">Verschieben-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="faf4c-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="faf4c-126">Neu – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="faf4c-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="faf4c-127">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="faf4c-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="faf4c-128">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="faf4c-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
