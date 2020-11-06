---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 8ef7121e057759a6fbdb341d9d6bc137692a36cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505290"
---
# <span data-ttu-id="3fd1a-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fd1a-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="3fd1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fd1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd1a-103">Ändert einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fd1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fd1a-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fd1a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fd1a-105">DESCRIPTION</span></span>
<span data-ttu-id="3fd1a-106">Das Cmdlet " **Satz-AzureRmExpressRouteCircuit** " speichert den geänderten Express Route-Schaltkreis in Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="3fd1a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fd1a-107">EXAMPLES</span></span>

### <span data-ttu-id="3fd1a-108">Beispiel 1: Ändern des serviceKey verwenden eines Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="3fd1a-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="3fd1a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fd1a-109">PARAMETERS</span></span>

### <span data-ttu-id="3fd1a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fd1a-110">-AsJob</span></span>
<span data-ttu-id="3fd1a-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3fd1a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fd1a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd1a-112">-DefaultProfile</span></span>
<span data-ttu-id="3fd1a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fd1a-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fd1a-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3fd1a-115">Gibt das **ExpressRouteCircuit** -Objekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3fd1a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd1a-116">CommonParameters</span></span>
<span data-ttu-id="3fd1a-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd1a-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fd1a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd1a-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fd1a-119">INPUTS</span></span>

### <span data-ttu-id="3fd1a-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fd1a-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="3fd1a-121">Parameter: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3fd1a-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="3fd1a-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fd1a-122">OUTPUTS</span></span>

### <span data-ttu-id="3fd1a-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fd1a-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3fd1a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fd1a-124">NOTES</span></span>

## <span data-ttu-id="3fd1a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fd1a-125">RELATED LINKS</span></span>

[<span data-ttu-id="3fd1a-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fd1a-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3fd1a-127">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fd1a-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3fd1a-128">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fd1a-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3fd1a-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fd1a-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
