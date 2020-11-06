---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 90814e90b4d4951a9e899fd8cf50f365b646f497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481901"
---
# <span data-ttu-id="d5bbf-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5bbf-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="d5bbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="d5bbf-103">Ruft eine Azure Express Route-Schaltkreis aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="d5bbf-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5bbf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5bbf-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5bbf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5bbf-105">DESCRIPTION</span></span>
<span data-ttu-id="d5bbf-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuit** " wird verwendet, um ein Express Route-Schaltkreis Objekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d5bbf-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="d5bbf-107">Das zurückgegebene Circuit-Objekt kann als Eingabe für andere Cmdlets verwendet werden, die auf Express Route-Schaltkreisen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d5bbf-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="d5bbf-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5bbf-108">EXAMPLES</span></span>

### <span data-ttu-id="d5bbf-109">Beispiel 1: Abrufen des zu löschenden Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="d5bbf-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="d5bbf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5bbf-110">PARAMETERS</span></span>

### <span data-ttu-id="d5bbf-111">-Name</span><span class="sxs-lookup"><span data-stu-id="d5bbf-111">-Name</span></span>
<span data-ttu-id="d5bbf-112">Der Name des Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="d5bbf-112">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5bbf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5bbf-113">-ResourceGroupName</span></span>
<span data-ttu-id="d5bbf-114">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="d5bbf-114">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5bbf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5bbf-115">-DefaultProfile</span></span>
<span data-ttu-id="d5bbf-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5bbf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5bbf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5bbf-117">CommonParameters</span></span>
<span data-ttu-id="d5bbf-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5bbf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5bbf-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5bbf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5bbf-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5bbf-120">INPUTS</span></span>

## <span data-ttu-id="d5bbf-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5bbf-121">OUTPUTS</span></span>

### <span data-ttu-id="d5bbf-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5bbf-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d5bbf-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5bbf-123">NOTES</span></span>

## <span data-ttu-id="d5bbf-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5bbf-124">RELATED LINKS</span></span>

[<span data-ttu-id="d5bbf-125">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5bbf-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d5bbf-126">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5bbf-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d5bbf-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5bbf-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d5bbf-128">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5bbf-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
