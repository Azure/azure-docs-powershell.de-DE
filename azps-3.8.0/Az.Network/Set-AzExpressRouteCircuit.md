---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003309"
---
# <span data-ttu-id="1995f-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1995f-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="1995f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1995f-102">SYNOPSIS</span></span>
<span data-ttu-id="1995f-103">Ändert einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="1995f-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1995f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1995f-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1995f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1995f-105">DESCRIPTION</span></span>
<span data-ttu-id="1995f-106">Das Cmdlet " **Satz-AzExpressRouteCircuit** " speichert den geänderten Express Route-Schaltkreis in Azure.</span><span class="sxs-lookup"><span data-stu-id="1995f-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="1995f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1995f-107">EXAMPLES</span></span>

### <span data-ttu-id="1995f-108">Beispiel 1: Ändern des serviceKey verwenden eines Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="1995f-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="1995f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1995f-109">PARAMETERS</span></span>

### <span data-ttu-id="1995f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1995f-110">-AsJob</span></span>
<span data-ttu-id="1995f-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1995f-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1995f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1995f-112">-DefaultProfile</span></span>
<span data-ttu-id="1995f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1995f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1995f-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1995f-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1995f-115">Gibt das **ExpressRouteCircuit** -Objekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1995f-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1995f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1995f-116">CommonParameters</span></span>
<span data-ttu-id="1995f-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1995f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1995f-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1995f-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1995f-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1995f-119">INPUTS</span></span>

### <span data-ttu-id="1995f-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1995f-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1995f-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1995f-121">OUTPUTS</span></span>

### <span data-ttu-id="1995f-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1995f-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1995f-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="1995f-123">NOTES</span></span>

## <span data-ttu-id="1995f-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1995f-124">RELATED LINKS</span></span>

[<span data-ttu-id="1995f-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1995f-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="1995f-126">Verschieben-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1995f-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="1995f-127">Neu – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1995f-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="1995f-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1995f-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
