---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 380a5f52a520f487e625663f7d84cbbc55564db5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663221"
---
# <span data-ttu-id="51ed2-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51ed2-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="51ed2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="51ed2-103">Ruft eine Azure Express Route-Schaltkreis aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="51ed2-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51ed2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51ed2-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ed2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51ed2-105">DESCRIPTION</span></span>
<span data-ttu-id="51ed2-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuit** " wird verwendet, um ein Express Route-Schaltkreis Objekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="51ed2-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="51ed2-107">Das zurückgegebene Circuit-Objekt kann als Eingabe für andere Cmdlets verwendet werden, die auf Express Route-Schaltkreisen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="51ed2-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="51ed2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51ed2-108">EXAMPLES</span></span>

### <span data-ttu-id="51ed2-109">Beispiel 1: Abrufen des zu löschenden Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="51ed2-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="51ed2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="51ed2-110">PARAMETERS</span></span>

### <span data-ttu-id="51ed2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ed2-111">-DefaultProfile</span></span>
<span data-ttu-id="51ed2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51ed2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51ed2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="51ed2-113">-Name</span></span>
<span data-ttu-id="51ed2-114">Der Name des Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="51ed2-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="51ed2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51ed2-115">-ResourceGroupName</span></span>
<span data-ttu-id="51ed2-116">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="51ed2-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="51ed2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ed2-117">CommonParameters</span></span>
<span data-ttu-id="51ed2-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51ed2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ed2-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51ed2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ed2-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51ed2-120">INPUTS</span></span>

### <span data-ttu-id="51ed2-121">Keine</span><span class="sxs-lookup"><span data-stu-id="51ed2-121">None</span></span>
<span data-ttu-id="51ed2-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="51ed2-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51ed2-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51ed2-123">OUTPUTS</span></span>

### <span data-ttu-id="51ed2-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51ed2-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="51ed2-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="51ed2-125">NOTES</span></span>

## <span data-ttu-id="51ed2-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51ed2-126">RELATED LINKS</span></span>

[<span data-ttu-id="51ed2-127">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51ed2-127">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="51ed2-128">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51ed2-128">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="51ed2-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51ed2-129">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="51ed2-130">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51ed2-130">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
